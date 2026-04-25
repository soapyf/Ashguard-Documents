# [Ash] - Mortar v2.0.0
## Specs
| Name                | Value        |
|---------------------|--------------|
| Layer               | 3            |
| Stats               | See Below    |

## Commands
All Commands Are On Channel 1. Default keybinds are listed below.

| KeyBind      | Chat Command | Description                                                 
|--------------|--------------|-------------------------------------------------------------
| Shift + 3    | d3           | Draws weapon                                                
| —            | s3           | Sling weapon
| R            | r            | Cycle Through Round Selection
| Q            | aux          | Fire while in deployed mode
| 1            | fm           | Toggle High/Low angle mode
| 2            | fm2          | Toggle deploy/hip-fire mode

> Reload times are doubled when in hip fire mode.
> Between Kill Radius and Falloff Radius damage reduces at a linear rate the farther beyond Kill Radius a detected object is.

### Explosive Round
| Stat                | Value        |
|---------------------|--------------|
| Kill Radius         |   7 Meters   |
| Falloff Radius      |  14 Meters   |
| Reload Time         |   3 Seconds  |
| Avatar Damage       | 100          |
| Anti-Armor Damage   |   5          |

### Anti-Armor Round
| Stat                | Value        |
|---------------------|--------------|
| Kill Radius         |  5 Meters    |
| Falloff Radius      | 10 Meters    |
| Reload Time         | 3 Seconds    |
| Avatar Damage       | 100          |
| Anti-Armor Splash   |  25          |
| Anti-Armor Direct   |  30          |

### Cluster Round
Detonates 30m above ground. Disperses 16 Cluster Rounds

| Stat (Main)         | Value        |
|---------------------|--------------|
| Kill Radius         |   5 Meters   |
| Falloff Radius      |  10 Meters   |
| Reload Time         |   4 Seconds  |
| Avatar Damage       | 100          |
| Anti-Armor Damage   |   5          |

| Stat (Clusters)     | Value        |
|---------------------|--------------|
| Kill Radius         |   5 Meters   |
| Falloff Radius      |   7 Meters   |
| Avatar Damage       | 100          |
| Anti-Armor Damage   |   1          |

### Flame Round
Detonates 30m above ground. Disperses 16 Flame Sources

| Stat (Main)         | Value        |
|---------------------|--------------|
| Kill Radius         |   5 Meters   |
| Falloff Radius      |  10 Meters   |
| Reload Time         |   7 Seconds  |
| Avatar Damage       | 100          |
| Anti-Armor Damage   |   5          |

| Stat (Flames)       | Value        |
|---------------------|--------------|
| Kill Radius         | 2.5 Meters   |
| Falloff Radius      |   5 Meters   |
| Avatar Damage       | 100          |
| Anti-Armor Damage   |   1 (per tick)|
| Lifespan            |  15 Seconds  |

### Static Round
| Stat (Main)         | Value        |
|---------------------|--------------|
| Reload Time         |   7 Seconds  |

| Stat (Static)       | Value        |
|---------------------|--------------|
| Falloff Radius      |   5 Meters   |
| Tick Rate           | 0.5 Seconds   |
| Avatar Damage       |   5 (per tick)|
| Anti-Armor Damage   |   2 (per tick)|
| Lifespan            |  30 Seconds  |


### Chaff Round
| Stat (Main)         | Value        |
|---------------------|--------------|
| Reload Time         |   5 Seconds  |