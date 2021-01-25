# Admin's/Mod's Guide to Discord

These are instructions + tips and tricks I've learned from years of moderating online spaces with a few thousand users. Some of it specific to Discord, but a lot of these tips will probably apply to other platforms.

## General notes regarding Discord

* As a mod/admin/owner, you want developer mode on at all times (user settings -> appearance).
* Always enable "Display role members separately from online members" for administrators and moderators in bigger servers.
* Do not create a role with any potentially destructive permissions (such as "Administrator, "Ban Members") low in the hierarchy of roles.
* Anyone with "Administrator", "Manage Server", "Manage Channels" or "Manage Roles" can seriously mess up the server, but it will be noted in the audit log who did it.
* Make sure to tag adult content channels (and please call it adult content, not NSFW, as it frames certain occupations as not work) using the NSFW channel toggle in the settings for the given channel.
* Do not assign, pronoun roles, game roles, and other utility/descriptive roles manually - make a bot do that job.
* Do not give bots permissions they shouldn't have. Dyno and MEE6 are notorious for asking for all the permissions, give them only the minimum they need and modify them as you see fit later.
* When creating a new non-functional role (such as pingable game roles), make sure to clear permissions.
* For privacy, restrict what channels bots can see. Give them the minimum needed access.
* Create a text channel for linking/chatting next to voice chats.
* Remember to turn off `@everyone` before starting to add roles. If you didn't, make sure to go through all the roles and remove that permission (especially in community servers).
* Mention in the rules that you'd like message links if someone is reporting bad behaviour (shows up in the right-click menu if you've enabled developer mode).
* If you want a bigger version of someone's pfp, try [discord.id](https://discord.id/) and paste in the user's unique ID (dev mode, copy ID).
* If you'd like to mention someone that isn't in the channel/in DMs, copy their ID and write `<@ID>`.
* When creating a new voice chat, remember to turn up the bitrate.

### Roles you probably want in most servers

* Voice Chat Anyone? - pingable role for when people want to talk
* Pronoun roles - makes the space a bit more welcoming in general to trans and gender non-conforming folks.

## General notes about interactions in digital spaces

* Writing down some rules is a must when the server hits anything beyond 20 users, preferably even earlier. If you start creating rules after an incident, the rules will feel as a permanent reminder for the offender and will lead to more negative tension. Rules are in my opinion more about shaping the environment than using the banhammer to enforce them.
* Make sure to have a suggestions-channel to avoid mods having to handle suggestions in DMs.


## Making sure that users do not mute `@everyone`/`@here` mentions

The general tip is to not make your server noisy in this regard. Generally, if you're pinging once per day you might already be doing it too much.

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

## Securing your server with an airlock

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

It allows for faster handling of users coming through the airlock.

The way it works is that people must mention one of the trigger words such as "accept", "read", or "rules" and if they do, you can have the bot scan their message and let them in.

Check `!help` once you've added the bot. The bot by default requests Manage Messages, but it only really needs the permission in the welcome channel. Change this at your earliest convenience.

It has cut down technical moderation tasks by an incredible amount, especially when three or more people show up at the same time.

## Useful bots

- [Carl Bot](https://carl.gg/) - Has custom commands and a way to set up react roles. The react roles are a bit fiddly to deal with for mods, but are a great solution for the users.
- [YAGPDB.xyz](https://YAGPDB.xyz) - Same as carlbot, but with other nifty features such as mod-made scripts.
- [MEE6](https://mee6.xyz) - Custom commands, has feature to post Youtube-feeds, some role options. Starting to get premiumfied (more and more restricted features for non-paying users)
- [Rythm](https://rythmbot.co/) + [Groovy](https://groovy.bot/) - two music bots that use different prefixes. You might want one or both.
- [Roleypoly](https://roleypoly.com/) - *Note: currently broken! Bot is currently not able to see users properly due to changes on Discord. Roles will not appear as assigned.* Web-based interface for configuring roles. The good: no complex commands, the bad: requires login and can be a handful on mobile.


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
14. If you don't have admin (but have mod), you can't click the clear permissions button for a role even if you are able to turn off each of them individually.
15. New roles inherit from `@everyone`. This means that if you forgot to remove the ability to ping `@everyone` before you made new roles, you'll have to go through every role individually and do it for every single one of them.
16. Granting someone read messages history permission in a channel doesn't update what they see. They'll have to restart the client to see what they're now allowed to see.
17. MessageDeleteEvent doesn't contain information about who deleted a given message.
18. You can't mute @everyone/@here from a webhook, not possible on an individual webhook nor all webhooks together.

#### Contributors
- TZer0
