# Custom MOTD

## Overview
Plugin allows staff to easily manage the MOTD displayed for the server in users' server list. Should set the MOTD on server startup to a default MOTD, and have commands staff can use to change the MOTD to something else while the server is live. MOTDs should support color codes and preferably be auto-centered.

## Behavior
The config contains a list of MOTDs that can be set as the active MOTD at any time. This list can have any number of MOTDs in it, and each one must have a unique name. There is also a default MOTD at the top of the config.

Staff can use a command to list all available MOTDs (by name) and then another command to set any of them as the active MOTD at any time. This should update in user's server lists immediately (when the user refreshes the list, of course).

Preferably, this plugin would make writing MOTDs easier by providing 2 lines that can be configured for each MOTD, auto-centering the text, and supporting color codes.

The plugin stores which MOTD is active and applies that MOTD on startup automatically every time. It does NOT always revert back to default.

**NEW**: Counter based MOTDs let us sell mcMMO perks in the store and update the MOTD to show when they are active. Each time a boost is purchased, the store will execute the command to increase the MOTD counter by 1, and each time one expires it will reduce the counter by 1. This way, when they all expire, the MOTD returns back to normal. The ability to have multiple counter-based MOTDs is preferable - a weight system can be used to determine which one to show.

## Commands

- /custommotd list (permission: custommotd.list)
- /custommotd check (permission: custommotd.list)
- /custommotd apply \<motd name\> (permission: custommotd.apply)
- /custommotd default (permission: custommotd.apply)
- /custommotd counter up
- /custommotd counter down
- /custommotd counter check

## Messages

- "Custom MOTD has been set to \<motd name\>"
- "Custom MOTD is \<motd name\>"

## Config

Default:
- "This is line one"
- "&aThis is line 2"

Custom:
- Custom1
    - "This is line one again"
    - "This is line &l2&r again"
- SomeEvent
    - "Join us!"
    - "For an awesome event!"

Counter:
- CustomCounter1
    - "This is line one again"
    - "This is line &l2&r again"
    - Weight: 1

## Notes

NA
