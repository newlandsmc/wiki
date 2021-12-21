# Disable Advancements

## Overview

This plugin sets the announce-advancements gamerule to FALSE for every world on server startup, every time. This is needed because advancement announcements can only be disabled via a gamerule, which is somewhat volatile and can be reset under the right conditions. We want to make sure this is ALWAYS set to false.

**NEW**: We want to rename this to "GameruleManager" and add a config so we can configure any gamerule and it's desired state.

## Behavior

On server startup, plugin sets ~~announce-advancements gamerule to FALSE for every world.~~ all configured gamerules.

## Commands

NA

## Messages

NA

## Config

- Global:#rules to apply to all worlds
  - list of rules
- World:
  - World1:
    - list of rules for world one.
  - World2: 
    - list of rules for world2.

## Notes

NA
