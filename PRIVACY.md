# Privacy Policy — Green Machine

_Last updated: July 26, 2026_

Green Machine (the "Bot") is a Discord bot that manages Club Penguin 
formations for the Army of Club Penguins community. This policy explains what
data the Bot accesses, how it is used, and what is (and isn't) stored.

We keep this short because the Bot stores almost no data.

## Who this applies to

This policy covers the **Green Machine** bot only. It does not cover Discord
itself, or any other bot.

## What the Bot accesses

To function, the Bot processes the following through Discord's API:

- **Message content** — read only to detect its command prefix (`f`) and the
  command arguments (for example `froom stadium` or `fbattle 15:30`). The Bot
  only acts on messages from users who hold specific authorized staff roles;
  all other messages are ignored.
- **User IDs** — used momentarily to know who issued a command (for example, to
  run a personal practice session or mention the user in a reply).
- **Channel IDs** — used momentarily to know where to post formation images and
  to track active drills/battles per channel.
- **Role membership** — checked to confirm a user is authorized to use commands.

## What the Bot stores

- **Nothing personal.** The Bot does **not** log, save, or transmit message
  content, user IDs, usernames, or any other personal information.
- The only data the Bot keeps on disk is a static configuration file mapping
  formation names to formation-diagram image URLs. It contains no user data.
- Message content, user IDs, and channel IDs are used **transiently in memory**
  to respond to a command, and are then discarded. Any short-lived session state
  (such as an in-progress practice quiz or a scheduled battle) is cleared when
  the session ends or the Bot restarts.

## How the data is used

Solely to provide the Bot's features: posting formation images, running drills,
scheduling battles, and running practice quizzes in response to authorized
commands. It is never used for advertising, profiling, or analytics.

## Sharing

The Bot does **not** sell, share, or disclose any data to third parties. Data is
processed only as needed to respond to Discord commands and is subject to
[Discord's Privacy Policy](https://discord.com/privacy).

## Data retention and requests

Because the Bot stores no personal data, there is nothing to export or delete on
request. If you have questions about the Bot's data practices, contact us (below).

## Age

The Bot operates within Discord and is intended for users who meet
[Discord's minimum age requirements](https://support.discord.com/hc/en-us/articles/360040724612).

## Changes to this policy

We may update this policy from time to time. Material changes will be reflected
by updating the "Last updated" date above.

## Contact

Questions about this policy or the Bot's data practices:

- **Discord:** fatchicken88
