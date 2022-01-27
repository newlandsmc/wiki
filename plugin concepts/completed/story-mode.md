# Story Mode

## Overview

This plugin handles sending players the story messages by muting chat and working through a queue of messages. This is a plugin that other plugins hook into to leverage this functionality.

## Behavior

Admin can configure a list of messsages to be sent, and a cooldown between each one. When these are triggered for a player, this plugin clears the chat, mutes the chat, and starts printing the messages. After the first message, it prints a line that informs the player they can skip this (or unmute chat?) by typing /skip. Each time they type /skip it prints the next message. If they skip the final message, it unmutes the chat.

## Commands

- /skip

## Messages

- "You can unmute chat by typing /skip."

## Config

Messages:
- 1:
  - message: "this is the first message"
  - delay: 1
- 2:
  - message: "this is the second message"
  - delay: 4

## Notes

Logical separation of plugins:

Cookie is working on determining how all of these plugins (story-mode, rejoin-rewards, join-handler) will be split up so they can reference each other and be easy to manage/maintain.
