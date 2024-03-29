# Admin's/Mod's Guide to Discord

These are instructions + tips and tricks I've learned from years of moderating online spaces with a few thousand users. Some of it specific to Discord, but a lot of these tips will probably apply to other platforms.

## General notes regarding Discord

* As a mod/admin/owner, you want developer mode on at all times (user settings -> advanced).
* Always enable "Display role members separately from online members" for administrators and moderators in bigger servers, also give bots a separate role.
* Do not create a role with any potentially destructive permissions (such as "Administrator, "Ban Members") low in the hierarchy of roles.
* Anyone with "Administrator", "Manage Server", "Manage Channels" or "Manage Roles" can seriously mess up the server, but it will be noted in the audit log who did it.
* Make sure to tag NSFW channels using the NSFW channel toggle in the settings for the given channel.
* Do not assign pronoun roles, game roles, and other utility/descriptive roles manually - make a bot do that job.
* Do not give bots permissions they shouldn't have. Dyno and MEE6 are notorious for asking for all the permissions, give them only the minimum they need and modify them as you see fit later.
* When creating a new non-functional role (such as pingable game roles), make sure to clear permissions.
* For privacy, restrict what channels bots can see. Give them the minimum needed access. If the bot relies on commands then there's no need to give it the permission to read the chat. Server deafen bots that join voice chats (such as music bots).
* Create a text channel for linking/chatting next to voice chats.
* Remember to turn off `@everyone` before starting to add roles. If you didn't, make sure to go through all the roles and remove that permission (especially in community servers).
* Mention in the rules that you'd like message links if someone is reporting bad behaviour (shows up in the right-click menu if you've enabled developer mode).
* If you want a bigger version of someone's pfp, try [discord.id](https://discord.id/) and paste in the user's unique ID (dev mode, copy ID).
* If you'd like to mention someone that isn't in the channel/in DMs, copy their ID and write `<@ID>`.
* If discussing violations, do mention the user's unique ID at least once for easy indexing for later searches.
* When creating a new voice chat, remember to turn up the bitrate.
* Unless you're banning an obvious reactionary or spammer, make sure to not delete the person's messages. It is important that your fellow mods (and yourself, later) are able to verify that the ban was in fact justifiable.
* Make sure to test your role colours in dark and light mode and that they have decent contrast in all situations, including in the list of offline users. Anything else can be hard to read and/or uncomfortable to look at.

### Roles you probably want in most servers

* Voice Chat Anyone? - pingable role for when people want to talk
* Pronoun roles - makes the space a bit more welcoming in general to trans and gender non-conforming folks. Put these at the end of the list of roles so they're always last and thus in a consistent place for ease of checking.

## General notes about interactions in digital spaces

* Writing down some rules is a must when the server hits anything beyond 20 users, preferably even earlier. If you start creating rules after an incident, the rules will feel as a permanent reminder for the offender and will lead to more negative tension. Rules are in my opinion more about shaping the environment than using the banhammer to enforce them.
* Make sure to have a suggestions-channel to avoid mods having to handle suggestions in DMs.
* In larger servers it is necessary to make an internal #moderation-notes-channel. It should contain information that every mod needs to know such as:
  * When to use `@everyone` and `@here`
  * How bans are handled (when to ban, when to delete messages when banning, etc.)
  * Important bot functionality, links to bot dashboards if applicable
  * Any non-intuitive technical intricacies relating to the server
* Once your server hits more than 1000 users, you're going to start needing the following (perhaps you need these things even earlier):
  * Modmail. Carl-bot has one. If there are tasks that just need to be done sooner or later but aren't critical, then modmail is the place. It should be used to handle pronoun role requests, signal boosts if your server does those, and new channel requests. Use reacts in the modmail channel to denote what has been handled.
  * Instructions for users on when to contact moderators in DMs in a channel detailing things they might get contacted about. You can't avoid DMs regarding certain things such as reports of harassment, but there needs to be some effort in avoiding DMs being sent to moderators/admins as sooner or later you'll be getting too many (or maybe one particular mod is getting too many and no one knows about it). Specify that users are requested to read the channel before contacting moderators.

## When to delete messages when banning/kicking
Generally, you want to be able to verify that bans are justified.
* The longer a user has been present, the less likely it is a good idea to delete the messages.
* Ban obvious reactionaries, delete messages.
* Do delete outright hateful messages.
* Don't delete longer discussions, do delete the end of it if it happens to turn more hateful there.
* Screencap if in doubt.

## Making sure that users do not mute `@everyone`/`@here` mentions

The general tip is to not make your server noisy in this regard. If you're pinging once per day you might already be doing it too much.

* First of all: do not let regular users ping. People will make mistakes and it'll be grating. It also reduces easy spam opportunities.
* The more you ping, the less attention people will pay.
* Rather than pinging `@everyone`/`@here` for an event, create roles that can be pinged instead and let people pick those if they wish to be pinged. Tip: as an admin you can ping roles that are otherwise not pingable.
* Know the difference between `@everyone` and `@here`. `@everyone` will ping everyone in the channel. `@here` will only ping people who are in the channel, online, and not idle.

### Things for which you might ping `@everyone`/`@here`

* Critical fundraisers for members/groups - especially if time is of the essence.
* Important information that all the users need to know about right now.
* Complete server reworks.

### Things for which you shouldn't ping `@everyone`/`@here`

* In any major server: birthdays.
* That you're high/drunk.
* That you want to hang out in voice chat.
* That you made a channel, exception: it is on a topic that keeps derailing other chats/is upsetting to certain members of the community and it needs to be contained now.

## Other Discord tips (that you might want to mention in your server)

* A good push to talk button is numpad 5 while num lock is off. Interacts with very few programs/games. I've tried using F24 which exists as an assignable button in Razer's driver software, but while it doesn't interact with any programs that I've noticed, it also gets stuck on frequently.
* PTT doesn't work when any program running as admin is in focus. This includes task manager. If you were holding down your PTT button while selecting a program running as admin, your PTT will remain active even if you let go of the button. Press it again after unfocusing the window to stop broadcasting.
* Do not ever edit out a ping, be it `@everyone`, `@role`, or `@user`. Do not edit in one either. The former leaves a ghost ping where people can see they got pinged, but won't find the message that did it, the latter doesn't ping the user/role in question.
* To share a time for an event etc, use UNIX time stamps - `<t:TIME:F>`, see [this site](https://r.3v.fi/discord-timestamps/) to make these easily.

## Securing your server with a gate

This system makes it so that users have to say that they accept the rules before they're let in by a moderator. Useful when screening for potential trouble-makers.


1. Create a trusted role, from now on referred to as `@member`.
2. Create any number of categories for your channels. Select that you're creating a private category, find `@member` in the list, click on the toggle next to it and then create category.
3. Create whatever new channels you need in the new categories.
4. If you have an existing channels, drag them into the new categories. If you've set special permissions on any of your old channels, right-click on them, edit, go to the permissions-tab, click the "Sync Now"-button.
5. Create a role for moderators, from now on referred to as `@moderator`.
6. Grant `@moderator` the permission to at least "Manage Roles", "Manage Messages", "View Audit Log", and also "Kick/Ban Users". Make sure to check the "Allow anyone to `@mention` this role" and "Display role members separately from online members".
7. Create a separate non-private category for where people start out. Put a channel like "#say-hi" there. Disallow `@member` from seeing it to prevent easy spam-opportunities. Allow `@moderator` to see it.

### Notes regarding experiences with this system

* Be vary of people who ping the moderator-role to be let in, often this is because they're impatient and want to start trouble. If someone does ping it and you do let them in, make sure to delete their message afterwards so other people don't replicate their behaviour.


### AcceptBot
I have made a bot called AcceptBot ([source code](https://bitbucket.org/TZer0/acceptbot/src)). Click [here](https://discord.com/api/oauth2/authorize?client_id=701052118903029760&permissions=268560448&redirect_uri=https%3A%2F%2Funderhound.eu&scope=bot) to add it.

A very quick demo of setting up AcceptBot and using it can be found [here](https://www.youtube.com/watch?v=S6FX56gEu8k).

It allows for faster handling of users coming through the gate.

The way it works is that people must mention one of the trigger words such as "accept", "read", or "rules" and if they do, you can have the bot scan their message and let them in.

Check `!help` once you've added the bot. The bot by default requests Manage Messages, but it only really needs the permission in the welcome channel. Change this at your earliest convenience.

It has cut down technical moderation tasks by an incredible amount, especially when three or more people show up at the same time.

## Useful bots

- [Carl Bot](https://carl.gg/) - Has custom commands and a way to set up react roles. The react roles are a bit fiddly to deal with for mods, but are a great solution for the users.
- [YAGPDB.xyz](https://YAGPDB.xyz) - Same as carlbot, but with other nifty features such as mod-made scripts.
- [MEE6](https://mee6.xyz) - Custom commands, has feature to post Youtube-feeds, some role options. Starting to get premiumfied (more and more restricted features for non-paying users)


## Tip for adding Carl Bot react roles to an existing react group

This assumes you've already set up reaction roles using `!rr make`.

* Create the role as you usually would
* Get the ID of the message you want to add the react role to
* Run the following commands:
```
!rr add MESSAGEID :emojiname: ROLENAME
```
```
!rr edit MESSAGEID CATEGORYNAME | {roles}
```
* Example:
```
!rr add 730747295406096384 :microphone2: Voice Chat Anyone?
```
```
!rr edit 730747295406096384 Pingable Roles | {roles}
```

## Horrible things about Discord

1. Channel permissions are OR, not AND or TOP. This causes a lot of headaches and you can't effectively have an accept-gate + channel hiding using roles.
2. No rule-board where all mods can edit the rules.
3. No metadata for profiles so you can't just set your pronouns globally in an easy way.
4. The permission to ban is the same as the permission to view the ban list.
5. If you dig around using the js console in the client, you can view the names and description of all channels even if they're hidden to you.
6. No official SDK for any language to make a bot.
7. No one really knows how moderation on Discord works. What gets a server banned is still unknown.
8. You can't easily report a message unless you're a moderator.
9. Porn-spammers do not get banned even if reported.
10. Discord still parses parts of embeds - especially tweets.
11. Discord often crashes when trying to stream or when you stop streaming.
12. A lot of things that ought to have been standard is something you need to do via a bot.
13. No way to avoid having someone on the top of the authority-chain, having a properly democratic server is impossible.
14. New roles inherit from `@everyone`. This means that if you forgot to remove the ability to ping `@everyone` before you made new roles, you'll have to go through every role individually and do it for every single one of them.
15. Granting someone read messages history permission in a channel doesn't update what they see. They'll have to restart the client to see what they're now allowed to see.
16. MessageDeleteEvent doesn't contain information about who deleted a given message nor whose message it was. Audit log does't contain timestamp of messages deleted, only who deleted and whose it was.
17. Minor thing, but tilde and minus are incredibly similar, especially when the font size is reduced.
18. There are so many gifs and videos out there that crash Discord and there's absolutely no detection for this.
19. Default dark purple for roles has a rather low contrast with the dark theme, making it difficult to read.
20. Bios are being added. However: you can't filter what server members are able to see and there's no explicit pronouns field available.
21. If a server you're in gets banned, your user might be taken with it regardless of level of participation.
22. There are still Discord-crashing gifs and videos.
23. 01.07.2021: Discord is embedding videos on linked tweets as jpegs with no indication that there's a video.
24. Hovering a link in an embed doesn't tell you where it leads.
25. Embeds of videos from Twitter often do not play and perform poorly in full-screen, fxtwitter.com exists as a way to mitigate this.

#### Contributors
- TZer0
