# Player Flow
What should a player's day-to-day experience on the server be?

## First Join
When a player first joins the server, they spawn somewhere random within the survival overworld. A campfire is spawned near them, with a chest containing starter items. The campfire remains there until they log off. After that, only the chest remains.

Note: If they don't take down their campfire, it will indicate to other players who find it that a new player spawned there recently.

Chat will be disabled when they first join so they don't get distracted by the chat and can be immersed in the story more. Messages will be sent when they first join to establish the story. The story is broken up into a queue of messages to be sent, with a delay between each one. The player is told they can do /skip to skip the story. Each time they run the command it prints the next line in the queue until they reach the end of the story and then it unmutes chat.

## Second Join

On their first reward-eligible join the chat is muted again and they are provided more story messages that explain what the "expedition spoils" are. Again, they can use /skip to skip the story and unmute the chat.

They can use /jreward claim to claim their rejoin rewards. 

## Subsequent Joins

Any time they join and qualify for a reward, we will just send them a single message in chat telling them to use /jreward claim to claim their rewards. We won't interrupt their game/chat anymore.

The message should say something like "You just completed a __ hour expedition! Claim your spoils with /jreward claim" where the time matches how long they were offline.

## While Online

A custom leveling system like mcMMO tracks their experience in things like PvP and let's them level up for small buffs. Like more max damage with certain weapons.

Random mob spawns are turned into "bosses" - they glow, they are harder to kill, and they drop better rewards. Their difficulty scales depending on who it spawned near (based on their PvE level)

A custom PvP system means that whenever you are killed, there is a 10 second respawn cooldown. You will respawn where you died and receive a large skills buff that gives you the advantage over the killer in case you want to get revenge. Your items are also protected so you will get your items back.

If you die normally, you respawn at your home (Essentials home).

A land protection plugin let's you claim your land and protect it. These claims expire after 6 months of being offline.

A sleep plugin gives sleeping a purpose on large servers (reduced max # required to sleep? Other side affects of not sleeping - like reduced health?)

A vote system allows you to vote for the server and instantly finish an "expedition" and get a rejoin reward. The message after voting could be "You just completed an instant expedition! Claim your spoils with /jreward claim"