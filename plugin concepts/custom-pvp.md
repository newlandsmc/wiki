# Custom PVP

## Overview

"A custom PvP system means that whenever you are killed, there is a 10 second respawn cooldown. You will respawn where you died and receive a large skills buff that gives you the advantage over the killer in case you want to get revenge."

~~"Your items are protected when you die, so only you can pick them up"~~ (GriefPrevention handles this)

## Behavior

When a player is killed by PvP, if they click "respawn" within 10 seconds, they will enter spectator mode watching the player that killed them. 10 seconds after they were killed, they will respawn exactly where they died. (If they waited 10 seconds to click the button, they respawn immediately. If they waited 5 seconds to click the button, then they only spectate for 5 seconds).

Their items are protected (by GriefPrevention) so they can pick them back up.

We want to buff the player for the next 60 seconds after they respawn - higher damage against players and higher health. We also want to nerf the player that did the killing for 70 seconds after they did the killing (10 seconds respawn cooldown + 60 seconds buff) - they cannot teleport during this time and they cannot become buffed if killed during this time.

## Commands

TBD

## Messages

TBD

## Config

TBD

## Notes

Rewards?:

Should players get rewards when they kill somebody? This could make the "player tracker" items PTW. If we implement this, there will be a 12 hour cooldown between getting a reward from the same player.

How to limit the back and forth?

If a player gets killed 3 times then it will ask the player being killed if they would like to /report the player for harassment. If they do /report then it will disable pvp between those 2 players for 1 hour. The /reports are logged for staff to review and staff can take action if a pattern is noticed.
