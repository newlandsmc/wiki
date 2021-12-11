# Rejoin Rewards

## Overview
Plugin tracks how long a player has been offline and rewards them when with "random" items when they return. The reward gets larger the longer they've been gone.

The idea is to make it feel like when a player logs off, their character is actually going on an expedition and will eventually return with a bounty, which varies in size depending on how long they were gone.

## Behavior
Plugin will log what time each player logs off in a redis database. When they return, it will subtract that time from the current time to determine how long they have been gone.

The config contains "tiers" of time-away that will result in a reward. (E.G., 2h = small reward, 6h = medium reward, etc.) The plugin will find the largest "tier" that the player is eligible for and will give them a random award from that tier. The tiers do not stack.

Each tier has a configurable "weight". Additionally, the config has a section that lists all eligible reward items and their respective weight. When a player returns and qualifies for a reward tier, the plugin will compile a random assortment of reward items that total to the "weight" of the reward tier. (E.G. 2h = 6 weight. apple = 1 weight, orange = 3 weight. Possible rewards: 6 apples, or 2 oranges, or 3 apples and 1 orange, etc.)

When a player has a reward they need to collect, they must use a command to open a GUI that contains their items. They can interact with the GUI like a normal chest and move the items to their inventory however/whenever they want.

If a player doesn't take all of their items, they will remain in the "virtual chest" until they take them. Also, if they earn additional rewards from  leaving and re-joining again, their additional rewards will just be added to the same "virtual chest". If the "virtual chest" fills up, they will get an error in chat that they must claim their current rewards before they can be granted any new rewards.

## Commands

- /jrewards claim (permission: jrewards.claim)
- /jrewards view \<player\> (permission: jrewards.view)
- /jrewards clear \<player\> (permission: jrewards.clear)

## Messages

- "You found treasure while you were away! Use \/jrewards claim to claim your treasure." (3 second delay after joining?)

## Config
Tiers:
- 2h:
    - weight: 6
- 4h:
    - weight: 12
- 12h:
    - weight: 18

Rewards:
- apple:
    - weight: 1
- orange:
    - weight: 3

## Notes

Future addition:

Possibly make the plugin place a physical chest near the player when they join, if they have rewards to claim. The chest must replace an air block. If the chest fails to safely place, then they will instead get a message in chat that says "You have rewards to claim! Use \<command\> to claim your rewards!". If they leave, the chest disappears. If they re-join, the chest is attempted to be placed again near them. This continues as long as they have rewards to claim. Once they have taken all the items from the chest, the chest disappears. They cannot add items to the chest.

This shouldn't feel like 'rewards':

This should not feel like a 'rewards' system, even though it is titled as so for easy understanding by developers. We want players to really understand and feel like they are leaving on expeditions and returning with bounties. (Terminology might need to change to make this concept better communicated)