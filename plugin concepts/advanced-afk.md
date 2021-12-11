# Advanced AFK

## Overview

Plugin adds AFK behavior similar to the Essentials plugin, but with additional features around AFK detection. Specifically, a player should be automatically flagged as "AFK" after they've been still for a configurable amount of time, and then the plugin should kick said player after another configurable amount of time if they are still "AFK".

## Behavior

The plugin will track player activity and mark a player as "AFK" if they do not talk or move more than X blocks within a certain amount of time.

The plugin should be able to keep a player marked as "AFK" if they only move a small amount, this is to discourage AFK pools. A player should be taken out of AFK status if: they talk, or they move more than X blocks.

When a player has been AFK for long enough, they should be kicked. Prior to being kicked, the player should be given a warning that they will be kicked. I'd like to give them the warning 60 seconds before they are kicked, 30 seconds before they are kicked, and 10 seconds befor they are kicked.

## Commands

NA

## Messages

- "You will be kicked for inactivity in 60 seconds!"
- "You will be kicked for inactivity in 30 seconds!"
- "You will be kicked for inactivity in 10 seconds!"

## Config

- afk-after: 5m
- kick-after: 15m
- movement-threshold: 3 (blocks)
- cancel-on-talk: true
- cancel-on-command: true
- cancel-on-interact: false

## Notes

This might have room for improvement:

I'd like to get more heads on this concept and figure out if there's room for improvement, such as additional actions that should cancel the AFK status, or more advanced ways to detect if someone is actually AFK but duping the system.

Should AFK be visible to others?:

Currently, this plugin will only track player's AFK status silently, for the specific purpose of kicking people who are AFK. We could look into whether it would be useful to players to see announcements when someone goes AFK, or show AFK status in /list or in TAB? 
