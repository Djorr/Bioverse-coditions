# Discord intents request — answers

Copy these answers into **Developer Portal → Bioverse → Request Intents**.

## What does your application do?

Bioverse is a private community bot for one 18+ social Discord server, "Bioverse", plus its two helper servers (Appeals and Verify). It is not a public bot and is not listed anywhere.

What it does:

- **Registration:** new members open a private thread and answer a few questions there: pronouns, birthday (18+ check), bio, region and languages. They also create a pixel-art avatar. Staff then review the bio and accept or reject it.
- **Bios channel:** accepted bios are posted as drawn cards. Members can greet, favorite and bump bios.
- **Levels and economy:** members earn XP and BioCoins by chatting, with leaderboards and a /card profile.
- **Wardrobe:** members spend BioCoins on clothing, hair and name colours for their avatar.
- **Social:** best friend bonds, plus wave, poke and pat interactions.
- **Chat games:** word scramble and quiz games in the chat channel.
- **Moderation:**
  - members can flag messages and open report tickets;
  - staff can time out, ban and quarantine members;
  - punished members can appeal in the Appeals server;
  - members can do selfie and age-group verification in private threads;
  - staff get log channels: member, role, message, voice, invite and moderation logs.

## Privacy Policy

Yes: https://github.com/Djorr/Bioverse-coditions/blob/main/privacy-policy.md

## Intents

Select **Server Members Intent** and **Message Content Intent**. Do **not** select Presence Intent.

### Server Members Intent — why

- **New members joining:** when someone joins, the bot starts their registration, gives the starting roles and checks for an earlier ban or quarantine.
- **Roles:** the bot gives and removes roles during registration (pronouns, avatar icon role, member role), verification, the wardrobe (name colours), and moderation (quarantine, age quarantine).
- **Member logs:** joins, leaves, nickname changes and role changes are posted to a private staff log channel.
- **Member data on cards:** names and avatars on bios, leaderboards and moderation cards come from the member list.

### Storing API data off-platform

**Yes.** The bot keeps a small private database with:

- Discord user IDs;
- the registration answers members give on purpose (pronouns, birthday, region, languages, bio, avatar choices);
- levels and BioCoins, best friend bonds, and moderation records (flags, tickets, punishments, appeals).

The database is only used by the bot itself and is never shared or sold. Members can ask staff to delete their data. See the privacy policy.

### Message Content Intent — opt-out

**No.** The bot only works in our own private community server. Message content is needed for the core features listed below, and members agree to the server rules and privacy policy when they register. Normal chat messages are only checked in memory and are not stored.

### Storing message content off-platform

**Yes, but only the registration answers and bios that members type to the bot on purpose.**

- Normal chat messages are **not** stored.
- When a message is edited or deleted, the old text is posted to a private staff log channel on Discord. It is not saved in our database.

### Used to train ML / AI models

**No.**

### Message Content Intent — why

- **Registration:** members type their answers in their private registration thread (pronouns, birthday, bio, region, languages) and type "agree" to submit. The bot checks the answers, for example the date format, the bio length and blocked words.
- **Verification:** members type "verify" in the Verify server to finish age-group verification.
- **Chat games:** the bot reads answers in the chat channel to find the first correct one.
- **Best friends:** a bond stays active when two best friends chat in the same minute.
- **Message logs:** the old text of edited and deleted messages goes to a private staff log channel, so moderators can handle reports.

### Screenshots / videos

The Discord form needs a link for each intent. Upload screenshots of the following and paste the links:

- **Server Members:** the registration thread after a member joins, and an entry in the member or role log channel.
- **Message Content:** a typed answer with the confirm card in a registration thread, a chat game being won, and an edited message in the message log.
