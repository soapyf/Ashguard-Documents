# [Ash] - Bonebiter Bow v1.0.0

## Arrow Characteristics

| Arrow Type | Velocity | Nocking Time | Velocity | Used per Shot | LBA Damage |
|------------|----------|--------------|--------------|----------------|-------------|
| Standard Arrow | 175.0 | 0.3s | 50.0 | 1 | 0 |
| Marker Arrow | 150.0 | 1.0s | 25.0 | 4 | 0 |
| Multi Arrow | 125.0 | 1.0s | 12.0 | 5 | 0 |
| Dispersion Arrow | 100.0 | 1.0s | 50.0 | 4 | 0 |
| Flash Arrow | 125.0 | 1.0s | 25.0 | 3 | 0 |
| Magic Arrow | 125.0 | 1.0s | 50.0 | 2 | 10 |
| Airburst Arrow | 60.0 | 2.5s | 20.0 | 10 | 5x6* |
| Satchel Arrow | 50.0 | 1.0s | 15.0 | 5 | 10 |

*deals 5LBA per arrow in a spread pattern

## Arrow Details

** Arrows per shot are not always the number of arrows fired, but the amount they use from the quiver.

### Standard Arrow
- **Purpose**: Basic combat arrow with full damage
- **Velocity**: 175.0 
- **Nocking Time**: 0.3s 
- **Arrows Per Shot**: 1
- **Damage**: 100 
- **Best For**: Direct combat, fast firing

### Marker Arrow
- **Purpose**: Marking/utility arrow with no damage
- **Velocity**: 150.0
- **Nocking Time**: 1.0s
- **Arrows Per Shot**: 4
- **Damage**: 0 

### Multi Arrow
- **Purpose**: Multiple projectile attack
- **Velocity**: 125.0
- **Nocking Time**: 1.0s
- **Arrows Per Shot**: 5 (spread)
- **Damage**: 100 per arrow

### Dispersion Arrow
- **Purpose**: Chaff arrow for dealing with interceptors
- **Velocity**: 100.0
- **Nocking Time**: 1.0s
- **Arrows Per Shot**: 4 
- **Damage**: 0

### Flash Arrow
- **Purpose**: Utility/blinding arrow
- **Velocity**: 125.0
- **Nocking Time**: 1.0s
- **Arrows Per Shot**: 3
- **Damage**: 0 

### Magic Arrow
- **Purpose**: Special AOE arrow
- **Velocity**: 125.0
- **Nocking Time**: 1.0s  
- **Arrows Per Shot**: 2
- **Damage**: 100, with falloff

### Airburst Arrow
- **Purpose**: Area effect arrow with delayed detonation // mortar style trajectory
- **Velocity**: 60.0 
- **Nocking Time**: 2.5s 
- **Arrows Per Shot**: 10 
- **Damage**: 0 
- **Special**: +15 base acceleration bonus, CTRL X for midair detonation // rains down

### Satchel Arrow
- **Purpose**: Deployable payload arrow
- **Velocity**: 50.0 
- **Nocking Time**: 1.0s
- **Arrows Per Shot**: 5
- **Damage**: 0 
- **Special**: +15 base acceleration bonus, CTRL X for detonation


## Quiver System

| Parameter | Value |
|-----------|-------|
| Quiver Capacity | 20 arrows |
| Reload Time | 0.35s |
| Arrows Per Reload | 2 |
| Auto-reload | Yes (when empty or half-empty) |

## Commands

| KeyBind | Chat Command | Description |
|---------|--------------|-------------|
| Touch Bow | — | Open favorites menu |
| 1 | fm | Cycle arrow type backward |
| 2 | fm2 | Cycle arrow type forward |
| Q | aux | Toggle between favorite arrows (requires setup) |
| R | r | Manual reload |
| Shift + 3 | d3 | Draw bow (Layer 3) |
| — | s3 | Sling bow (Layer 3) |
| Crouch | — | Cancel draw |
| Ctrl + X | — | Manual Detonation |
