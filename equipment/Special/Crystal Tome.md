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
| Shift + 1 | d            | Switch to Fire Mode 0 — Crystal Burst / Crystal Shards |
| Shift + 2 | d2           | Switch to Fire Mode 1 — Homing Mote / Homing Crystal Mass |
| Shift + 3 | d3           | Switch to Fire Mode 2 — Crystal Spike |
| F       | melee        | Trigger book melee strike |
| Q       | aux          | Encampment / secondary fire (mode-dependent) |
| —       | reset        | Reset script |

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
