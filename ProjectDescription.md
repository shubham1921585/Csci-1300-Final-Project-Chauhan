# Project Description: The Hyperdrice Protocol

## Theme 
A Sci-fi open survival game. You are a captain of a stranded ship. Your goal is to gather missing ship parts (the "bundle") to repair your hyperdrive before a hostile alien fleet arrives. 

## Planned Classes 
**Item:** Represents collectibles (scrap, rations, parts). Stores 'name', 'type', and 'value' 
**Player:** Tracks the user's 'name', 'oxygenlevel', 'credits', and 'inventory' (array of Items).
**Character:** Represents crew and aliens. Stores 'name', 'currentlocation', and quest status. 
**Game:** Manages the main game loop, map, time progression, and terminal dashboard. 

## Planned Limited Resources
1. **Oxygen:** Consumed when traveling or scavenging. If it hits 0, you pass out. Restored by eating rations.
2. **Credits;** Used to buy iems from traders. Earned by selling scrap or helping crew members.

## Plan for Handling Time
Time is tracked in **Cycles** (days). The player has 7 cycles. Moving around the ship is free, but major actions cost Oxygen. The player selects "Enter Cyro-Sleep" to end the current Cycle, reset Oxygen, and advance time.

## Extra Credit
I plan to implement **Option 4: Weather System**. The game will randomize space weather ( Clear or Asteroid Storm) each cycle. Storms make scavenging yield rarer parts, but temporarily lock travel to certain map locations.

## Tradeoff System
The **Black Market Smuggler** acts as the JojaMart equivalent. 
* **Benefit:** You can buy mssing hyperdrive parts instantly.
* **Drawback:** Buying from the smuggler increases 'pirateNoteriety'. If this gets too high, you repair the ship but are arrested by the Galactic Federation at the end of the game.

 ## Mapping Style
A text based **Connected-Location Map** shown on the terminal dashboard. An asterisk '*' marks the player's current location.
```text
        [Asteroid Belt]
               |
[*Bridge] -- [Cargo Bay] -- [Engine Room]
               |
       [Trading Post]
```
## Goal (Win/lose Condition)

The main objective of the game is to repair your starship's broken hyperdrive before you are intercepted by a hostile alien fleet. 

**Win Condition:** Successfully scavange, purchase, or trade for all 5 required hyperdrive parts and install them on your ship before the end of Cycle 7.

**Lose Condition:** The time limit expires (reaching Cycle 8) before all 5 parts are colleccted, resulting in your ship being captured by the enemy fleet.




