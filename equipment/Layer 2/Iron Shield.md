# [Ash] - Iron Shield v1.12.0

## Specs

| Name         | Value |
|--------------|-------|
| Layer        | L2L   |
| Shield HP    | 50    |
| Block Arc    | ~63°  |
| Recharge Rate | 1 HP / 2.5s (idle), 2 HP / 2.5s (broken) |

> The shield occupies the left-hand Layer 2 slot. Equipping any L2 weapon will detach it.

## Commands

All Commands Are On Channel 1. Default keybinds are listed below.

| KeyBind   | Chat Command | Description          |
|-----------|--------------|----------------------|
| Shift + 2 | d2 / draw2   | Draw shield          |
| Shift + 4 | s2           | Sling shield         |
| Crouch (held)  | —            | Enter block stance   |
| Crouch (release) | —          | Exit block stance    |

## Blocking

Holding the crouch key (C) raises the shield into a block stance, absorbing incoming damage for attacks within a ~26° frontal arc.

| Damage Type | Reduction  |
|-------------|------------|
| All others  | 100%       |
| Explosive   | 35%        |

> Arc is determined by a dot-product threshold of `0.45` between the shield's forward vector and the direction to the attacker — approximately **±63°**.

## Shield HP

The shield has a separate HP pool tracked by its collider prim. When HP reaches 0 the shield **breaks**: it becomes invisible, drops a cosmetic "Iron Buckler Dropped" object, and cannot block until repaired. HP is restored automatically on teleport.

| Event        | Effect                                         |
|--------------|------------------------------------------------|
| HP > 0       | Shield active, HP displayed on shield face     |
| HP = 0       | Shield breaks, block disabled                  |
| Teleport     | HP reset to 50, shield restored                |

The collider prim becomes phantom while not blocking, triggering passive regeneration every 2.5 seconds (scaled by region time dilation). A broken shield recharges at **2 HP per tick** instead of 1, and automatically revives once HP is fully restored.
