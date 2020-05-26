# Space-Pirates

A 3rd Person space themed Action-Adventure Shooter made in UE4 for CS3247.

## Overview
* 3rd Person (Pilot a ship)
* Action-Adventure Shooter
* Space themed
* Main Components
  * Inventory/Crafting
  * Procedurally generated levels
  * Advanced enemy AI
  
### Demo 
<i>(Click on the photo for a YouTube video)</i>
 <a href="https://www.youtube.com/watch?v=DKVqgNOoBbg&feature=youtu.be&fbclid=IwAR0O3zAqjMPAVMuxeKsmwqJQhmeAkprAe_v9s42tifbSYmxOEI8P2REf28">
  <img src="http://i3.ytimg.com/vi/DKVqgNOoBbg/maxresdefault.jpg">
  </a>
  
  
### Progress 
[report](https://docs.google.com/presentation/d/1eGcTbFQlsOf9wjRUjX8DOPPf3GZ66VDgOXNdJ98zz2Q/edit?usp=sharing)

### Authors
* Yip Seng Yeun
* Daniel Elias
* Zhang Chenxi
* Marin Tinnirello
* Mateusz Nowak

# Components

## Aesthetics - Daniel Elias

<img src="https://github.com/Futuramistic/Space-Pirates/blob/master/Promo/Images/Planet1.png" width="270" height="150" align="right">

We decided to mix three game themes to make an unique game:
Space + Cyberpunk + Pirates

<img src="https://github.com/Futuramistic/Space-Pirates/blob/master/Promo/Images/Planet2.png" width="270" height="170" align="right">

Special features:
* Planet Materials
* Atmospheric Scattering
* Skyboxes
* Unique 3D Models

## Movement - Yip Seng Yeun
We implemented a simple contorls schemas to steer our spacecraft.

WASD - Control spacecraft position

QE - Roll

Left Shift - Thrust

Player's spacecraft can pitch and roll. Max speed is dependent on the player’s equipping thruster


## Inventory and equipment - Mateusz Nowak

<img src="https://github.com/Futuramistic/Space-Pirates/blob/master/Promo/Images/Inventory.PNG" width="430" height="255" align="right">

The player collects resources and parts to be used in crafting
The player has limited space to store cargo
We have a large number of item types:
* Equippable
  * Armor, gun and thruster
* Consumable
  * Materials and healing item
  
 TAB - open inventory in game


## Crafting - Mateusz Nowak

<img src="https://github.com/Futuramistic/Space-Pirates/blob/master/Promo/Images/Crafting.PNG" width="430" height="255" align="left">

One of the core mechanics of the game is crafting modules for weapons and ship using collected resources. Rather than a linear upgrade progression, the different modules offer trade-offs, such as more armor at the cost of slower turning.
We designed the game around a high degree of customization of the player's ship, allowing the player to design any kind of ship, from a light and agile fighter for hit and run tactics, to large and chunky battleships with tons of firepower.

Crafting system uses Box-Muller Transform to uniformly distribute statistics based on specific rarity of an item.

## Enemies and AI - Zhang Chenxi
We designed the enemy AI to use a commander - soldier hierarchy to coordinate movements. This adds a level of tactical depth to the player, incentivizing players to plan their attacks and defenses in response. 

Enemies are generated with randomized stats (HP, speed, attack, weapon type etc).

<img src="https://github.com/Futuramistic/Space-Pirates/blob/master/Promo/Images/Models.PNG" align="right">

We plan to implement a level difficulty scoring system based on a function of each enemy and their stats. This allows us to have varied level design but still maintaining the same difficulty curve, generating replay value.

1. Enemy AI
  * Soldier Enemy
    * Each soldier will be assigned a commander
    * Soldiers can updates their enemy according to commander’s command.
    * Soldiers can report enemy to their commander
  * Commander Enemy
    * Commander can updates their enemy according to soldiers’ report
    * Commander can send commands of new enemies to soldiers
2. Friendly AI (Future Improvement)
  * Player’s Assistant
    * Will follow (and be close enough to) the player all the time
    * Will attack the enemy which player is shooting at
    
## Level Design - Daniel Elias and Marin Tinnirello
We have 3 main levels with bosses at the end of each level. The bosses will require the player to carefully choose their loadout and learn the attack patterns of the boss. Progression is linear but the player may choose to travel freely between cleared levels (e.g. to farm an old boss). The player may choose to visit procedurally generated levels while progressing through the main levels at any time to collect more resources/explore.

The background is mainly cosmetic elements that do not interact with the player e.g. celestial bodies that appear in the background that cannot be landed on.

Level design includes procedurally generated:
* Enemies
* Structures
* Background

## Shooting mechanics - Yip Seng Yeun
Player can equip three kinds of weapons:
* Shotgun
  + Great damage
  - Slow
* Machine gun
  + Fast
  - Small damage
* Laser
  + Automaticaly focuses on nearby enemies
  - The weakest DPS
  
With each weapon, player can defeat different enemies and gain different stats to match his play style.  
LMB - Shoot

## Main menu, pause and save/load game - Mateusz Nowak

![](https://github.com/Futuramistic/Space-Pirates/blob/master/Promo/Videos/MainMenu.gif)

We designed our main menu screen with special font effects, unique animations and atmospeheric music. Player can load their previous progress, start a new game or quit the game from this menu.

The player can also stop the game and save their progress or quit at any moment in game.

Escape - pause game

Pause|Save|Load
 :-------------------------:|:-------------------------:|:-------------------------:
<img src="https://github.com/Futuramistic/Space-Pirates/blob/master/Promo/Images/Pause.PNG">|<img src="https://github.com/Futuramistic/Space-Pirates/blob/master/Promo/Images/Save.PNG">|<img src="https://github.com/Futuramistic/Space-Pirates/blob/master/Promo/Images/Load.PNG">
 </div>


## Special effects - Daniel Elias and Marin Tinnirello
* Blur effect and special sound effect when the player’s speed is high.
* Special star gates to change levels

## Sound - Daniel Elias
The game sounds were designed to portray each level uniquley. They create specific emotions and impressions of actual objects and phenomenons.
