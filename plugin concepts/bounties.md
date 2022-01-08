# Bounties

## Overview

When someone kills another player, they "get a bounty on their head". The bounty lasts for a configurable amount of time (default 24 hours.)

If someone kills a bounty they get a configurable amount of vanilla XP as a reward (default 500xp.) They do NOT get marked as a bounty for killing a bounty. The bounty status is also removed from a bounty if they get killed.

A bounty should be marked in 4 ways:

1. When they do the killing configurable messages are sent out (i want this as 2 separate messages with a 0.5 second delay between them)
* \<Victim\> was slain...
* \<Killer\> has a bounty on their head!
  
2. A configurable suffix should be added to their name in TAB (default: "- bounty" in gold)
  
3. Their name above their head should have the same suffix applied

4. Squaremap support (see next section)

Note: All configurable messages should support minimessage for formatting.

The SquaremapPlayers plugin should be modified to make the color and fill-color of the marker a different color if a player is a bounty. It should somehow hook into the bounty plugin to get a list of players with bounties.

## Behavior

TBD

## Commands

- \/bounty <add/remove> <name> - bounties.modify - add/remove the bounty from any player.

## Messages

TBD

## Config

TBD

## Notes

TBD
