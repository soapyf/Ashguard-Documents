# [Ash] - Kagrenac bolt-caster v1.0.2
## Specs
| Name                | Value        |
|---------------------|--------------|
| Layer               | 1            |
| Magazine Size       | 42           |
| Reload Time(seconds)| 2.45         |
| Rounds Per Minute   | 900          |
| Spread Min          | 0.20°        |
| Spread Max          | 2.00°        |
| Shots to Max Spread | 15           |
| Normal Damage       | 100          |
| Partial Damage      | 25           |

### Secondary fire
Alt fire [Q]. 
Fires a collection of spikes into the ground that deal damage to colliding avatars.
Forces a reload after 3 consecutive uses without reloading.
Number of deployed spikes is limited and deploying more than Max listed below will delete the oldest currently deployed.


| Name                | Value        |
|---------------------|--------------|
| Tick Rate(seconds)  | 0.5          |
| Damage per tick     | 10           |
| Ammo per use        | 14           |
| Max # deployed      | 5            |
| HP (LBA)            | 5            |
  
## Commands
All Commands Are On Channel 1. Default keybinds are listed below.

| KeyBind      | Chat Command | Description                                                 
|--------------|--------------|-------------------------------------------------------------
| —            | help1        | Opens link to this page                                     
| Shift + 2    | d2           | Draws weapon                                                
| —            | s2           | Sling weapon                                                
| R            | r            | Reload                                                      
| —            | pd           | Toggle partial damage                                       
| —            | kc           | Toggle hitmarker rounds (requires hitmarker HUD)            
| —            | anim         | Toggle between animation sets for narrow and wide shoulders
| —            | pos          | Cycle through Avpos, Campos, Velpos bullet rezzing         
| F            | melee        | Triggers melee attack                                     
| Q            | aux          | Secondary fire / Nail Trap
