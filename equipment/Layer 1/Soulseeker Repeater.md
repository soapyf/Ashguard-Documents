# [Ash] - Soulseeker Repeater v2.22.0

## Specs

| Name                 | Value    |
|----------------------|----------|
| Layer                | L1       |
| Firemode             | Auto     |
| Magazine Size        | 50       |
| Reload Time(seconds) | 2.55     |
| Rounds Per Minute    | 700      |
| Fire Cores           | 2        |
| Spread Min           | 0.10°    |
| Spread Max           | 0.75°    |
| Shots to Max Spread  | 13       |
| Normal Damage        | 100      |
| Partial Damage       | 45       |
| Projectile Speed     | Variable |

## Commands

All Commands Are On Channel 1. Default keybinds are listed below.

| KeyBind        | Chat Command | Description                                      |
|----------------|--------------|--------------------------------------------------|
| ML Left Button | —            | Fire                                             |
| Shift + 1      | d            | Draw weapon                                      |
| Shift + 4      | s            | Sling weapon                                     |
| R              | r            | Reload magazine                                  |
| Q              | aux          | Fire underslung grenade; reload if empty         |
| —              | pd           | Toggle partial damage (100 → 45)                 |
| —              | kc           | Toggle hitmarker rounds                          |
| —              | pos          | Cycle rez position (AvPos → CamPos → VelPos)     |
| —              | ao           | Toggle Full AO / Simple AO                       |
| —              | vel.XXX      | Set bullet velocity (minimum 100)                |

## Underslung Grenade

A single-shot grenade launcher mounted beneath the barrel, fired from mouselook. The grenade is lobbed with 2× gravity and detonates on contact, dealing area damage.

| Name                 | Value  |
|----------------------|--------|
| Ammo                 | 1      |
| Reload Time(seconds) | 3.00   |
| Launch Velocity      | 80 m/s |
| Gravity              | 2.00×  |
| Full Damage Radius   | 5 m    |
| Max Damage Radius    | 10 m   |
| Avatar Damage (full) | 100    |
| LBA Damage (full)    | 5      |

### Damage Falloff

Damage scales linearly from full to zero between the full damage radius and the max damage radius.

| Distance | Avatar Damage | LBA Damage |
|----------|---------------|------------|
| 0 – 5 m  | 100           | 5          |
| 7.5 m    | ~50           | ~2.5       |
| 10 m     | 0             | 0          |

> Avatar damage falls off from **5 m → 10 m**. LBA damage falls off from **5 m → 10 m**.
