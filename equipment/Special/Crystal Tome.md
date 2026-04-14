# [Ash] - Crystal Tome v0.1

## Specs

| Name    | Value     |
|---------|-----------|
| Layer   | L1,L2,L3  |
| Channel | 1         |

---

## Commands
All Commands Are On Channel 1. Default keybinds are listed below.

| KeyBind | Chat Command | Description |
|---------|--------------|-------------|
| —       | d            | Switch to Fire Mode 0 — Crystal Burst / Crystal Shards |
| —       | d2           | Switch to Fire Mode 1 — Homing Mote / Homing Crystal Mass |
| —       | d3           | Switch to Fire Mode 2 — Crystal Spike |
| —       | s / s2 / s3  | Sling / holster the weapon |
| —       | melee        | Trigger book melee strike |
| —       | aux          | Encampment / secondary fire (mode-dependent) |
| —       | r            | Reload |
| —       | reset        | Reset script |
| —       | L1 / L2 / L3 / L2R / L2L | Detach corresponding layer |

---

## Fire Modes

### Mode 0 — Crystal Burst / Crystal Shards

**Quick Fire (tap < 0.5s):** Fires a 5-shot burst of crystals that embed in surfaces they hit.
- Mana Cost: 0

**Charged (hold > 0.5s):** Fires a close-range double shotgun crystal spread; crystals also embed in surfaces.
- Mana Cost: 2 per cast

**Encampment / Aux:** Returns all active crystals in sight back to your position, dealing damage to anything they pass through on the way back.
- Mana Cost: 5 flat
- Note: Crystals expire after ~15 seconds or on your next shot. Encampment only affects the last spread fired.

---

### Mode 1 — Homing Mote / Homing Crystal Mass

**Quick Fire (tap < 1s):** Fires a single homing projectile that deals 5 LBA damage; syncs direction to your mouselook pointer.
- Mana Cost: 24 flat

**Charged (hold > 1s):** Summons 5 floating crystals above your head, each dealing 60 damage on hit; crystals home in on targets within sight.
- Mana Cost: 10 flat
- Cooldown: 1s between charged casts

**Encampment / Aux:** Arranges 5 crystals into a ring pointing in all directions; crystals home in and shoot targets within 30m for full damage.
- Mana Cost: 5 flat
- Requires charged crystals to be active; replaces previous encampment if re-used.
- Expires after 1 minute.

---

### Mode 2 — Crystal Spike

**Charged (press):** Summons a crystal trail that moves at a set pace, stays on flat surfaces, and creeps up to 30m or until released — then erupts into a crystal spike.
- Mana Cost: 10 flat (on initial press)

**Encampment / Aux:** While the crystal trail is active, halts it and hides it in place; activates and triggers if an enemy steps over it.
- Mana Cost: 5 flat
- Up to 3 spikes can exist at once; the oldest is deleted when a 4th is placed.
- Expires after 1 minute.

---

## Melee

| Name          | Value       |
|---------------|-------------|
| Command       | `melee`     |
| Melee Range   | 5m          |
| Melee Arc     | 45°         |
| Melee Speed   | ~0.5s       |
| Melee Cooldown | 0.8s       |
| Avatar Damage | 100 (falloff applies) |
| LBA Damage    | 5           |
| Damage Type   | Explosive   |

The tome is swung in a melee strike using one of three randomized slash animations. The crystal gem is hidden during the swing and restored afterward.

---

## Damage Falloff (Melee & Sensor-based attacks)

Damage scales linearly from full to zero between the full-damage range and the explosion radius.

| Distance   | Avatar Damage | LBA Damage |
|------------|---------------|------------|
| 0 – 5m     | 100           | 5          |
| ~5.5m      | ~50           | 5          |
| 6m+        | 0             | 5          |

> Avatar damage falls off from **5m → 6m**. LBA damage is fixed at **5** and does not fall off.

---

## Detection

Sensor-based hit detection runs in 3 sequential passes:

| Pass | Type       | Range | Cone |
|------|------------|-------|------|
| 0    | AGENT      | 5m    | 45°  |
| 1    | SCRIPTED   | 5m    | 45°  |
| 2    | DAMAGEABLE | 5m    | 45°  |

- A raycast is used per target to validate line of sight before applying damage.
- Agents are hit if the raycast returns fewer than 1 blocking object.
- Scripted/Damageable objects are hit if the raycast root key matches the target, or the target has scripts and no blocking geometry.
- C2.0 DAMAGEABLE targets receive `llDamage()` directly; legacy LBA targets are messaged via MD5 channel.
