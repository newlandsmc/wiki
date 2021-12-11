# Join Handler

## Overview

This plugin will send announcements when players join and leave. A separate message should be used when a player first joins vs every other time they join.

## Behavior

When a player joins for the first time, it should send an announcement to the chat for everyone to see. When they leave it should also send an announcement. Then when they rejoin, a third type of announcement should be sent. These should REPLACE the default Minecraft join/leave messages.

The messages will need a variable for the player name. It should use their actual username and NOT their nickname from Essentials, if they have one set.

## Commands

NA

## Messages

NA

## Config

- first-join-message: "&a* {USERNAME} has awoken in a strange place..."
- join-message: "&a* {USERNAME} has returned from their expedition!"
- leave-message: "&c* {USERNAME} left on an expedition..."

## Notes

Potential overlap of projects:

It might make sense to merge this project with the rejoin-rewards plugin?

Additional features:

If we decide to mute the chat on join to display story-related messages, this might be the plugin to add that functionality to.