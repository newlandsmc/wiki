# PvP Ghosts

## Overview

When a player is killed, they enter a "ghost state" for 60 seconds to track down their killer and get revenge. After the 60 seconds, they respawn at their bed. If they succeeded in getting revenge, they can return to their death spot to collect the dropped items. If they didn't they respawn with nothing.

## Behavior

When a player enters ghost state, the death screen is disabled and they respawn immediately (or cancel the death event?). After the 60 seconds, they die like normal and see the death screen.

If a player wasn't killed by PVP, they do not enter ghost state.

A player can use /respawn to skip the ghost state at any time during the ghost state.

When a player is a ghost, their killer is highlighted and the killer sees them as highlighted.

A player in ghost state:
- Can harm their killer
- Can NOT harm anyone/anything else
- Can NOT place blocks or break blocks
- Can travel through blocks?
- Can break blocks placed by their killer? (Coreprotect API)


## Commands

- /respawn - skip ghost state

## Messages

- "You're haunting <playername> and cannot do this!"
- Action Bar: "Haunting <playername> (/respawn to skip)"

## Config

TBD

## Notes

Questions:

What is the ghosts weapon?
