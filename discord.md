Discord-stuff
=

Securing your server with an airlock (people have to ask moderators to be let in)
-
1. Create a trusted role, from now on referred to as "@member".
2. Create any number of categories for your channels. Select that you're creating a private category, find @member in the list, click on the toggle next to it and then create category.
3. Create whatever new channels you need.
4. If you have an existing server, drag your old channels into this category. If you've set special permissions on any of your old channels, right-click on them, edit, go to the permissions-tab, click the "Sync Now"-button.
5. Create a role for moderators, from now on referred to as "@moderator".
6. Grant @moderator the permission to at least "Manage Roles", "Manage Messages", "View Audit Log", and also "Kick/Ban Users". Make sure to check the "Allow anyone to @mention this role" and "Display role members separately from online members".
7. Create a separate non-private category for where people start out. Put a channel like "#say-hi" there. Disallow @member from seeing it to prevent easy spam-opportunities. Allow @moderator to see it.

General warnings/notes regarding Discord
-
* Always put roles for administrators and moderators on the top.
* Do not create a role with any potentially destructive permissions (such as "Administrator, "Ban Members") low in the hierarchy of roles.
* Anyone with "Administrator", "Manage Server", "Manage Channels" or "Manage Roles" can seriously mess things up for you as well, but it will be noted in the audit log who did it.
* Make sure to tag adult content channels (and please call it adult content, not NSFW, as it frames certain occupations as not work) using the NSFW channel toggle in the settings for the given channel.
* Do not assign pronoun roles etc. manually. Make a bot do that job.
* Do not give bots permissions they shouldn't have. Dyno and MEE6 are notorious for asking for all the permissions, give them only the minimum they need and modify them as you see fit later.
* Do not give bots @member. Instead create a separate role ("@bots") and channel that @member, and bots can see.
* When creating a new non-functional role (pingable things), make sure to clear perms.


Horrible things about Discord
-

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
15. New roles inherit from @everyone. This means that if you forgot to remove the ability to ping @everyone before you remove that permission from @everyone, you'll have to go through every role individually and do it for every single one of them.
16. Granting someone read messages permissions in a channel doesn't update what they see. They'll have to restart the client to see what they're now allowed to see.

