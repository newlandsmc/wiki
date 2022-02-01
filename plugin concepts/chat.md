# Chat

## Overview

Chat plugin allows us to create a format for chat. It should be: `&f[%Luckperms-prefix%&f] &7%name%&f: %message%` where %name% is either the user's actual username, or their nickname if they have one.

Must have built in nickname functionality. Allow staff to set a user's nickname with `/nickname [user] [nick]`

Entire plugin must have HEX support. Luckperms groups are in HEX color and nicknames will be too.

Must also provide private messaging functionality with `/msg` (alias: tell, message) and `/reply` (alias: r). Reply should reply to last person use received a message from OR sent a message to.

Must also provide staff chat functionality with `/sc [message]` (alias: ac). Does NOT need to be toggeable. Probably should NOT be toggeable.

Finally, must support ChatFilter plugin and BetterCommandSpy, or have command spy built in. If built in - must have a blacklist of commands to ignore. ChatFilter should not be built in, the plugin has lots of functionality and I use ALL of it.

## Behavior

Nicknames should only be used in public chat. PMs and Staff Chat should use actual usernames.

## Commands

- \/msg
- \/reply
- \/sc
- \/nickname

## Messages

Chat: `&f[%Luckperms-prefix%&f] &7%name%&f: %message%`
PM: `&9[Whisper] %from% -> %to%: %message%`
SC: `&e[Staff Chat] %name%: %message%`

## Config

TBD

## Notes

Quick Notes:

- Format chat with RGB
- Support for Luckperms group prefix
- Nicknames (only used in chat)
- Built-in [i] (item) support
- Private messages
- Staff chat
- Support for: https://www.spigotmc.org/resources/chatfilter-chat-signs-books-and-anvils.81652/
- Support for: https://www.spigotmc.org/resources/bettercommandspy.84030/
