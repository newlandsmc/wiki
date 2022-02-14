# Expeditions 2.0

## Overview

Rewards given to players when they rejoin and/or vote. Players should be able to do /expeditions (alias: /spoils) to open a GUI with 4 options:
- "Daily Expeditions"
- "Premium Expeditions"
- "Vote Expeditions"
- "Super Vote Expeditions"

They can click on any of these to open a second GUI page with items to "claim" (move to their inventory) from that particular Expedition.

## Behavior

The description of each GUI icon should inform the player of how to get that particular type of expedition. And, if they have any to claim, add another line to the description saying so.

Attempting to click on an expedition for which you do not have any spoils to claim should change the title and description of the item in the GUI to be red and change the description to say "You do not have any spoils from this Expedition right now! Do XYZ to get one."

**Daily Expeditions:**
- Should be rewarded the first time a player logs in each day. Reset at midnight using the time of the host.
- When they login and receive one, notify them immediately in chat.
- These do NOT stack. If they receive one and already had one pending to claim, they still only have one.

**Premium Expeditions**
- Will be purchaseable in the store. I need a command I can use to give someone a Premium Expedition to claim. I'd like to be able to specify a number in the command for how many "premium expeditions" to give a player.
- Should also automatically be given to a player after they receive a "super vote expedition" 7 days in a row.
- Notify the player in chat as soon as they receive one of these.
- These should stack. Each time they click on the GUI icon they open one of these, until they don't have any left.

**Vote Expeditions**
- Should be rewarded each time the player votes on a single site. The list of sites to listen for should be configurable. Ignore votes received from sites not in the list.
- Notify the player in chat as soon as they receive one of these.
- These should stack. Each time they click on the GUI icon they open one of these, until they don't have any left.

**Super Vote Expeditions***
- Should be rewarded after the player votes on every site. The list of sites to listen for should be configurable. Ignore votes received from sites not in the list.
- Notify the player in chat as soon as they receive one of these.
- These should stack. Each time they click on the GUI icon they open one of these, until they don't have any left.

**Loot Generation**
- Loot should work similar to vanilla loottables. (We should be able to configure infinite number of "pools" for which to generate loot from). It should support randomized enchantments, potions, custom item names and descriptions.
- For each of expedition type, we should be able to specify which "pools" to pull items from.
- I think it makes the most sense to have these pools each be a separate file and have a directory in the plugin directory for "pools". Use the filename as the pool name?
- I also think it makes the most sense to generate what loot to give the player when they click the icon in the GUI.
- It would be awesome to have some sort of animation in the GUI when the loot is being generated, like an animated pattern of stained glass, have it dance for a couple seconds, and then have each item populate on at a time in the GUI while the animation continues in the unused slots.

## Commands

- /expeditions (alias: /spoils)
- /expeditionsadmin give \<player\> \<#\> (not visible to normal players)

## Messages

TBD

## Config

TBD

## Notes

Reusable Code:

You may be able to reuse portions of Expeditions 1.0 (such as the Votifier integration), or the loot generation code from EnderDragonTweaks.
https://github.com/SemiVanilla-MC/Expeditions
https://github.com/SemiVanilla-MC/EnderDragonTweaks
