# Kelp privacy policy

Last updated 5 September 2026.

Kelp is a video app for a server you run yourself. This page says exactly what it sends, where,
and what you can turn off. It is written from the app's source code rather than from a template,
and everything in it is checkable.

## The short version

Kelp has no account, collects nothing about you, and sends nothing to its developer. There is no
analytics, no crash reporting and no tracking of any kind in the app.

## Kelp needs a server that you run

Kelp is a client. It does not work on its own and no server is provided with it. You point it at a
Yattee or Invidious server that you host, and everything you do in the app goes to that server:
what you browse, what you search for, what you watch, and your subscriptions feed. Your server
address, username and password are stored in your device's Keychain.

**What that server does with your requests is between you and it.** It is your server. This policy
covers the app, and it cannot make promises about software you run.

## What the app stores on your device

- Your server address, username and password, in the Keychain.
- Your subscriptions, playlists, watch history, search history and settings.
- A cache of channel pictures and recent server responses, to avoid asking twice.

All of it stays on your device, and Settings, Privacy, Clear All Local Data removes every bit of
it. You can also export it as a single file, which deliberately contains no password.

## Everywhere else Kelp can connect

Four things other than your own server. Two of them are choices you make.

### Images, and this is the one worth reading

Thumbnails and channel pictures are loaded from whatever address your server puts in its replies.
**Kelp does not choose those addresses.** Most Invidious servers hand back addresses at Google, in
which case your device fetches pictures from Google directly and Google can see your IP address
and which pictures you asked for. Some servers proxy images themselves, in which case that does
not happen.

The same is true of the video itself. If your server relays video, playback talks only to your
server. If it hands back direct addresses, playback talks to Google's video hosts.

**This is decided by how your server is configured, not by the app**, and the app has no switch
for it today. If it matters to you, configure your server to proxy.

### SponsorBlock, on by default

Kelp asks the SponsorBlock community database which parts of a video other people have marked as
sponsorship or self-promotion, so it can skip them.

**It is never told which video you are watching.** It is sent the first four characters of a
one-way hash of the video's id, which matches thousands of videos at once, and it returns the
segments for all of them. Kelp picks the right ones on your device.

On by default. One switch in Settings turns it off completely, and no request is made when it is
off. The server it asks can be changed, including to one you host.

### Dislike estimates, off by default

Kelp can show estimated dislike counts from the Return YouTube Dislike project.

**This one does send the video's id**, which is why it is off until you turn it on. If it is on,
that project learns which videos you open.

### Your own server, for search suggestions

Suggestions as you type come from your own server, not from anybody else.

## What Kelp never does

- It sends nothing to its developer. Not usage data, not crashes, not a heartbeat.
- It has no account, no sign-in and nothing to log in to.
- It shows no advertising and contains no advertising or affiliate code.
- It writes no log file. A release build of Kelp does not create one.

## Children

Kelp is a viewer for whatever your own server provides. It has no content of its own and no
sign-up, so it collects nothing from anybody, including children.

## Changes

If a version of Kelp connects somewhere new, this page changes before that version ships.

## Contact

kelpapp@pm.me
