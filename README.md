# CSCI 1300 Final Project

## Theme

You awoke from cryo-sleep to screaming alarms and an empty ship. A catastrophic failure scattered five critical hyperdrive parts across the vessel, and a rogue black hole will tear the hull apart in exactly seven cycles. Scavenge the dark sectors, rebuild the engine, and jump us out of this graveyard before it is too late.

## Goal

The goal of this game is to scavange the ship and find all the 5 missing hyperdrive parts before a rogue black hole destroys the vessel in 7 cycles. You must carefully manage your limited oxygen levels to travel between rooms, search for parts, and interact with surviving crew members, utilizing cryo-sleep to restore your oxygen while racing against the clock.

## How to compile and run

To compile the game, open your terminal in the project directory and run the following command:

g++ -Wall -Werror -std=c++17 main.cpp Item.cpp Player.cpp Character.cpp Smuggler.cpp Game.cpp -o hyperdrive

Now to run the compiled game, run:
.\hyperdrive.exe

## How to play

The game is played entirely in the terminal using a number based menu system. Each turn, you will be prompted to make a command choice:
1. Move to a new room: Travel to a different location on the ship.(Cost: 10 Oxygen)
2. Scavange for parts: Search your current room for items. You might find scrap metal, or a critical hyperdrive part.(Cost: 25 Oxygen)
3. Enter Cryo-Sleep: Ends the current cycle and restores your Oxygen to 100%, but pulls the ship one cycle closer to the black hole and triggers random space weather events.
4. Quit Game: Shut down the terminal and exit the program.
5. Search room for survivors: Look for your crew members hiding in your current room.(Cost: 5 Oxygen)

Manage your oxygen carefully. If you run our, you will pass out, forcing an emergency cryo-sleep and wasting a precious cycle. 

## Classes

Item: Represents objects in the game. It stores the item's name and type (such as "scrap" or "hyperdrive_part").

Player: Represents the ship's captain. Manages core stats including oxygen levels, credits, and an array of Item objects that acts as the inventory. 

Character: A parent class representing entities on the ship. It stores basic data like the crew member's name and their current location. 

Smuggler: A child class that inherits from Character. Acts as the game's risk/reqard tradeoff system, aaloowing player to trade a massive amount of oxygen for a guarenteed hyperdrive part.

Game: The main engine class. It handles file I/O by loading the map from rooms.txt, manages the main game loop, controls the passage of cycles, and checks the win/loss conditions. 

## Extra credit

None
