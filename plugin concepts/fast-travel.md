# Fast Travel

## Overview

Staff can set locations around the world as "waypoints" Players must visit a waypoint to unlock it, and then they can teleport there in the future.

## Behavior

Waypoints title, description, and icon should be configurable - including using minimessage for formatting. Waypoints can be defined in a config. A command in-game can be included for creating a waypoint template, but I do NOT need or want a full in-game editor. The in-game command should let staff do "/fasttravel create <name>" and then a config entry will be created with a default icon and description, so we can go into the config later, find the new entry, and customize it to our liking.

Waypoints are "locked" by default and cannot be used by players. They must first visit the location to unlock the waypoint. (Being within a configurable radius of the waypoint's coordinates, including height/Y, should unlock waypoints). After a player has visited a waypoint, then they can teleport there in the future.

Players can open a GUI to see all waypoints. Locked waypoints will be represented by gray dye and cannot be clicked on. Unlocked waypoints will be represented by a configurable icon, unique to each waypoint. Players can click on these to teleport to it. There should be a configurable delay before teleporting (default 5 seconds) and should cancel if they move or take damage (looking around doesn't count as moving).


## Commands

\/fasttravel create <name> - fasttravel.create - create new waypoint
\/fasttravel - fasttravel.use - open GUI

Please have configurable aliases for plugin, so we can optionally add "warp" and "waypoint" in the future. (For now I don't want any aliases).

## Messages

All messages should be configurable
  
- Message for teleport delay starting ("\<gray\>Teleporting in 5 seconds, don't move...")
- Message for teleport commencing ("\<gray\>Teleporting...")
- Message for waypoint created ("\<green\>New waypoint <name> created. Open config to modify.")
- Message for access denied to command ("\<red\>You do not have permission to do this") - _preferably, players will not see commands they don't have access to in /help or tab complete, and running them will return the default unknown-command message._

## Config

TBD

## Notes

References (existing plugins that appear to be what we want):

https://www.spigotmc.org/resources/fasttravel.13231/

https://www.spigotmc.org/resources/cybertravel-%E2%9C%A8-discover-regions-%E2%9A%A1-teleport-back-%E2%9A%A1-fast-travel-%E2%9A%A1%E3%80%8C1-8-1-17%E3%80%8D.94603/
