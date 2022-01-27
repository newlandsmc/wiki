# Announcer

## Overview

Sends announcements in chat on a configurable timer and also displays a title (and plays a sound) when players join the server.

## Behavior

Every X minutes the plugin grabs a random announcement from a configurable list of announcements and broadcasts it in chat.

There is a configurable title that is displayed on player login, and a different one is used if the player is new. This title has a configurable fade in time, stay time, and fade out time. It also have a configurable delay after logging out so a player doesn't see it if they quickly reconnect.

There is also a configurable sound that is played, at a configurable login, every time the title is shown.

Must have mimimessage support for everything

## Commands

TBD

## Messages

TBD

## Config

Broadcasts:

```
# The amount of time used for the interval
interval-time-amount=20
# The unit of time used for the interval
#  Can be SECONDS, MINUTES, or HOURS
interval-time-unit=MINUTES
# The list of messages for a config
messages=[
    {
        message-text=[
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
            ""
            "Vote every day to support the server and get rewarded"
            "for it! <gradient:yellow:red>https://semivanilla.com/vote</gradient>"
            ""
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
        ]
    },
    {
        message-text=[
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
            ""
            "Enjoying the server? Please consider donating"
            "at <gradient:yellow:red>https://store.semivanilla.com</gradient>!"
            ""
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
        ]
    },
    {
        message-text=[
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
            ""
            "Join the community! Find us on Discord"
            "at <gradient:yellow:red>https://discord.gg/3WzZ3x6wGp</gradient>!"
            ""
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
        ]
    },
    {
        message-text=[
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
            ""
            "Check the map! All players locations can be"
            "seen at <gradient:yellow:red>https://semivanilla.com/map</gradient>!"
            ""
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
        ]
    },
    {
        message-text=[
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
            ""
            "Want to keep your items when you die? Make them "
            "SoulBound with <gradient:#ac2626:#720a0a>/soulbind</gradient>! <gray>(Coming soon)</gray>"
            ""
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
        ]
    },
    {
        message-text=[
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
            ""
            "Kill a player to get Fighting XP. Kill a bounty to"
            "steal all the Fighting XP they stole from others!"
            ""
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
        ]
    },
    {
        message-text=[
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
            ""
            "Complete Expeditions by spending time offline and "
            "voting every day! Claim rewards with <gradient:yellow:red>/spoils</gradient>."
            ""
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
        ]
    },
    {
        message-text=[
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
            ""
            "Grinding Skills XP? Boost XP earned for the entire"
            "server at <gradient:yellow:red>http://store.semivanilla.com</gradient>."
            ""
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
        ]
    },
    {
        message-text=[
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
            ""
            "Get around faster! Use <gradient:yellow:red>/fasttravel</gradient> to visit"
            "official locations around the map."
            ""
            "<gradient:yellow:red:yellow><strikethrough>                                                                 <reset>"
        ]
    },
]
# Should the messages be sent in order of the config or in random order
random-message-order=true
```

Join Title and Sound:

```
    returning-player {
        title-settings {
            # Seconds of duration for the title to stay on screen
            duration-seconds=4
            # Seconds of duration for the title fade-in animation
            fade-in-seconds=1
            # Seconds of duration for the title fade-out animation
            fade-out-seconds=1
            # Subtitle text. If the title and subtitle are both set to "" (empty string), then this title is disabled
            title="<gradient:yellow:red:yellow:{animate:scroll:0.1}>SemiVanilla MC</gradient>"
            # Title text. If the title and subtitle are both set to "" (empty string), then this title is disabled
            subtitle="The Adventure Continues"
        }
        join-sounds {
            name="minecraft:ui.toast.challenge_complete"
            pitch=1
            source=master
            volume=0.8
        }
    }
    new-player {
        title-settings {
            duration-seconds=4
            fade-in-seconds=1
            fade-out-seconds=1
            title="<gradient:yellow:red:yellow:{animate:scroll:0.1}>SemiVanilla MC</gradient>"
            subtitle="The Adventure Begins"
        }
        join-sounds {
            name="minecraft:ui.toast.challenge_complete"
            pitch=1
            source=master
            volume=0.8
        }
    }
```

## Notes

TBD
