---
title: How the privacy works
permalink: /how-it-works/privacy/
---

This page explains the mechanism: what is encrypted and what is not, who holds
which key, what happens when you sign in on a new phone, and what taking
something back actually does. The [privacy policy](/privacy/) is the authority
on what we hold about you; this page is what sits underneath it, for somebody
who would rather check a claim than take it.

It is written for a careful reader who is not an engineer. Where the claim has
a limit, the limit is here too, in the last section.

## What is sealed, and what is not

Sealed on your phone, with keys we never see:

- photographs, at every size we store them;
- captions;
- comments;
- the titles of albums;
- your display name and your profile picture;
- the blurred placeholder that stands in for a photograph while it loads.

In the clear, because delivering anything at all needs it:

- your handle, and whichever ways in the account holds: an email address, a
  password, or both. For a password we hold a public key your phone made from
  it, and never the password itself;
- the country your phone was set to when you joined, written once and never
  updated;
- who you are connected to and when you connected, along with the add
  requests you send and receive and the blocks you place;
- the names of your groups, and which of your groups a person is in;
- who is in each album you are in;
- for each post: who made it, when, who it was addressed to, how many frames
  it has, how large the encrypted files are, and, for each recipient, whether
  they have seen it and when they first did;
- reactions, which are one emoji each;
- the pointer naming the encrypted file your profile picture sits in, which
  is what lets us sign the link that serves it;
- the push address of each phone you have signed in on, and the moment you
  confirmed you were 18 or older, which is a moment and never a date;
- whatever you type into a report or a bug report, because those are messages
  to us and we have to be able to read them.

That is the short version. The [privacy policy](/privacy/) has the full one,
and it is the authority if the two ever disagree.

Two of those deserve a word, because they are the ones somebody could be
caught out by. **Album titles are sealed; group names are not**, and neither
is the list of who is in one—though nobody is ever told which of your groups
they are in. A group is your own private label for some of your mutuals,
stored as text, and the 60-character bound on it is enforced by the server,
which is only possible because the server can count the characters. And
**reactions are in the clear on purpose**. One emoji out of a set anybody can
enumerate is guessable however it is wrapped, and the server holds the row
saying who reacted to what in any case, so encrypting it would be theatre. It
is listed honestly instead.

### The blurred placeholder is encrypted too

The soft rectangle that appears while a photograph is still arriving is about
25 bytes, and 25 bytes is easy to keep in a plain database column, because it
looks like nothing. It is not nothing: it is a coarse transform of the
picture, and 25 bytes is enough to carry the composition and the colours. So
it is sealed, inside the post's encrypted metadata, which is small and fetched
first. That is why the placeholders appear before the photographs do.

### Location data, and everything else EXIF carries

Nothing is stripped out of your pictures, because nothing survives to be
stripped. The picture is decoded into a bitmap and re-encoded, and a bitmap
has no EXIF at all: GPS, the camera model, serial numbers, the lens, the
software that touched it, all of it is simply absent from what gets sealed.
The usual approach is a filter over a list of tags, and the list is where the
leak lives, because it has to name everything worth removing. Here there is
no filter, so there is nothing for a filter to miss.

The one thing kept is the date the photograph was taken, and it is written
inside the sealed metadata rather than back onto the file. Writing a tag back
onto a JPEG needs a file on disk, and nothing in this pipeline puts a
decrypted photograph anywhere but memory.

## How one photograph travels

Say anna posts four photographs to bruno and carla.

1. Her phone generates a random key for this post, and for this post only.
2. It makes every size of every photograph on the device and seals each file
   under that key. Each file is bound to its own slot as it is sealed: the
   full-size copy of the third photograph carries a label saying exactly that,
   so a store that served one file in place of another would not be believed
   by the phone that opens it.
3. It wraps the post key three times: once for bruno, once for carla, and once
   for anna herself. Each wrap uses that person's public key, which her phone
   has first checked against the one it recorded the first time it was given
   one for them; that check has a section of its own below.
4. It uploads the sealed files over signed links that lapse after fifteen
   minutes and carry the exact byte count in the signature, so storage
   refuses any other length. Then it sends the manifest and the three wrapped
   keys. The server writes the post and the deliveries in a single
   transaction, so a post is never half published.
5. bruno's phone downloads ciphertext, unwraps the post key from its own
   delivery, and decrypts the photographs on the phone.

What we end up holding is a pile of encrypted files, three small wrapped keys
we cannot open, and the note that a post went from anna to bruno and carla at
a particular minute.

anna's own copy of the key is a column on the post rather than a delivery to
herself, and it is what makes it possible to widen the audience afterwards:
her phone unwraps the post key and wraps it again for the new person. There
was never a moment when the server could have done that on her behalf, which
is why [adding somebody to a post](/how-it-works/posting/) is always something
the author does. An audience only ever widens: there is no control anywhere
that un-shares one photograph from one person. What takes a photograph back is
removing or blocking somebody, or deleting the post, and each of those is a
destroyed key rather than a hidden row.

There is no cache anywhere on that path. A signed link is unique to the
request that asked for it, so a cache in front of storage would miss every
time by construction, and every arrangement that does cache would mean
replacing the signature with something of ours. There is no content delivery
network in this product and there is not going to be one.

## The key that is yours

Your identity key is generated in software on your phone, by libsodium, before
the account exists. The server is handed the public half at signup and could
never have had the other one.

At rest the private half is sealed under a key generated inside the Android
Keystore, which will not give that key back to anything, including us. Where
the phone has a separate security chip the app asks for it and uses it; where
it does not, it carries on. A chip is an upgrade and never a requirement,
because requiring one would exclude phones on no security grounds we could
defend. The app's own data is also kept out of Android's cloud backup.

### Why the key is not simply held by the chip

"Stored in the secure enclave" is the strongest-sounding answer, and it is the
wrong one here. A key the secure element holds cannot be exported: that is the
entire point of a secure element, and it is flatly incompatible with the
sentence above it, which is that your key has to be recoverable from six words
onto a replacement phone. A chip-held key would quietly add "lost phone" to
the list of ways to lose your photographs, which is a far more common event
and a much worse promise.

So the key is generated in software and the chip guards it where it sits. A
rooted, unlocked phone in somebody else's hands still wins, and no arrangement
on a general-purpose operating system changes that.

### One key per person, not one per device

There is no device linking here and no code to scan from your first phone.
Each person has one key, and a second phone gets it from the recovery phrase.

Per-device keys are stronger and are deliberately deferred: wrapping would
become recipients multiplied by devices, and adding a device would mean either
re-wrapping your whole history or losing it. One key per person is the right
complexity for a closed beta with a limit of 128 connections.

### A second key, against a computer that does not exist yet

A copy of what we hold, taken today, could be kept until there is a quantum
computer large enough to matter. Nobody has one, and the US standards body
plans to retire today's methods by 2035, but a photograph of a child stays
sensitive for longer than that. Such a computer would not break the encryption
on the photographs themselves. It would break the step that hands each
recipient the key: the older kind of public key can be worked back to its
private half.

So an account made with a current version of the app has two keys where it
used to have one. The second is X-Wing, a method built to survive a quantum
computer, joined to the older kind so that it holds as long as either does.
A current version of the app, sending to such an account, puts the key in two
locks, one inside the other: the older one inside, the new one around it, and
opening it takes both of your private keys. A copy taken today stays closed,
and a server that tried to slip in a new key of its own would find the older
lock still in its way.

Your key's short name covers both keys, and your recovery phrase brings both
back. The second lock is put on by the phone of whoever is sending to you, so
it is there only when that phone runs a current version of the app and we
handed it both of your keys. An account made before this has the older key
alone. The last section says what each of these leaves open.

## The recovery phrase

Six words, drawn by a cryptographic random generator from a list of 7,776, and
shown to you once. Your identity key is sealed under a key stretched from
those words with Argon2id at 128 MiB of memory, and the sealed result is
stored on our servers. We cannot open it.

You cannot choose your own words, and the reason is specific rather than
pedantic. We hold the sealed backup, which makes us the one attacker in the
world who could guess at the phrase offline, at leisure, with no rate limit
anybody could impose on us. Against that, a passphrase a person invented is
not a secret with a bit count: it is a word or two and a number, and no amount
of key stretching that runs on a phone buys more than a small factor against a
search that starts from a dictionary. Six words from that list is about 77
bits. That is not "stronger"; it is a different category of thing, out of
reach whatever the stretching costs.

What the app says on that screen is the whole promise:

> These six words are the only way back to your photos if you lose this phone.
> Write them down and keep them somewhere safe. We cannot show them to you
> again, and we cannot recover them for you—not because we won't, but
> because we never see them.

There is a *copy* link under the words, and the clip is exactly what the
restore field takes. Security apps usually refuse the clipboard for something
like this; refusing it does not keep the phrase off the phone, it only decides
which copy the phone keeps, and the copy people reach for instead is a
screenshot, which lands in the gallery and goes wherever the gallery is backed
up. The clip is marked sensitive, so from Android 13 the system masks it in
its own confirmation and a keyboard with a clipboard history is told what it
is holding. Nothing clears it on a timer, because the app cannot know when you
pasted it.

Copying does not make the phrase retrievable later. In *settings* the
*recovery phrase* row says *saved* or *not saved*, and never the words.
Tapping it makes six new words and shows them once. If a phrase was saved, the
old six words stop working, and an account with an email address gets a
message saying the phrase changed.

### What losing it costs

Losing the phrase and every phone that holds your key means the photographs
are gone, and there is no procedure and no appeal. Be precise about the pair,
though: losing the phrase alone costs nothing while a phone still holds the
key, and losing every phone costs nothing while the phrase survives. It is
both together.

So if you lose the phrase, make a new one while a phone still has the app
signed in: tap *recovery phrase* in *settings*.

What we can do to the sealed backup is refuse to hand it back, or hand back an
older one. Both cost you a restore. Neither reads a photograph.

## Signing in on a new phone

The code proves you control the address it went to, and a password proves you
know the password. Whether this phone can *be* that account
is a separate question, and the key is the answer. Three things
can happen: the key already on the phone matches the account, and you are in;
the phone kept that account's key from an earlier sign-in, adopts it, and you
are in; or neither, and it asks for the six words.

That last screen says: *This phone does not have the key for that account. The
six words you wrote down bring it back.*

Restoring brings back the same key, so your mutuals' phones see nothing
unusual. It also restores the record of everybody's keys that your old phone
had built up—without that, a new phone would treat every person you already
knew as a first contact, and the check described below would have nothing to
check against.

Signing out leaves your key on the phone and deletes nothing you have made.
The push address is deleted by the server in the same transaction that revokes
the session, rather than by the app on its way out, because an app that has to
remember to unregister will forget exactly when it is killed.

## Who hands out the padlocks

This is the joint every end-to-end encrypted system has, and it is worth
saying plainly rather than stopping at "we cannot read your messages".

Your phone seals a photograph with a padlock that only anna's key opens. But
it asked *us* for that padlock. A dishonest server—broken into, or
compelled—could hand your phone its own padlock wearing anna's name. Your
phone seals the photograph with it and uploads. We open it, read it, seal it
again with anna's real padlock, and pass it along. She receives it. Nothing
looks wrong to either of you, and nobody ever finds out.

The defence that is built is this: the first time your phone is given
somebody's key it writes it down. Every time after that it compares. An
unchanged key is silent. A changed key stops you.

It stops you rather than warning you. The function that hands a key to
anything that is about to seal something returns a key or raises an alarm,
never both: a caller that got both would have to remember to check, and the
one that forgot would seal your photograph to the server's padlock and upload
it. So if one person's key has changed, the publish fails before a single byte
is uploaded, and you see this:

> The key we were given for anna is not the one this phone saw before. A new
> phone or a reinstall does not change a key here, so this should not happen on
> its own. It can mean someone is intercepting what you share with them. Check
> with them another way before you share anything with them.

The answers are *i checked, it's them* and *not now*. The copy offers no
everyday explanation because here there is not one: restoring from the six
words brings back the same key, and nothing in the app publishes a new one.
There is no "continue anyway" worded to be the easy path either, because
softening a security alert is how it becomes a dialog people dismiss without
reading. Clearing it is a separate decision somebody made, not a retry.

What the alarm cannot yet do is show you the key it was just handed, so that
the person at the other end could read theirs against it and settle it. Their
profile shows the key your phone wrote down, which is the old one, and the
alarm stops the app before you can get there. That is not built.

### Where the written-down keys live

On your phone. This is the whole of the defence, and an earlier design got it
wrong: the record was going to live on the server, in the clear. That cannot
work. A server that hands over the wrong padlock can rewrite the record of the
right one, then compare its own lie against its own lie and raise nothing. The
check looks like it is working and is doing nothing at all.

So the record that counts is on the device. We hold only a copy your phone
sealed before sending it, which we can store, cannot open and cannot forge. We
can withhold it or serve an older version; a phone that has already seen a
newer one refuses an older one, and a brand-new phone has nothing to compare
against and must take what it is given.

### What the claim is, exactly

Once your phone has written down a key for an account, we cannot swap that
key for one of ours without your phone refusing to seal anything to it and
raising that alarm. And what was sealed to genuine keys stays closed to us:
every copy of a key we hold is locked so that we cannot use it, and only a
phone that already holds a post's key can pass it on to somebody new.

That is a claim about a key *changing*, and it is narrower than "we cannot
begin intercepting". Two things sit outside it.

The first is the very first hello between two people who have never exchanged
a key: a phone with nothing written down takes what it is handed. Closing that
means comparing keys out of band, and the half you read aloud is built. Open a
mutual's profile: under the switches, *their key's short name* is 24
characters in six groups of four, and it is the key your phone locks things to
for them. Their own is in *settings → your key's short name*, on their phone.
Read one against the other. If they match, nobody is in the middle, first
hello included. If they do not, somebody else can read what you share with
them. That checks one direction; the other is them reading yours off your
profile. There is no square to scan yet, and nothing in the app asks you to do
any of this.

The second is the list itself. Your phone asks us who your mutuals are, who is
in a group and who is in an album, and asks again at the moment you post. It
seals to the list it is given, and it keeps no list of its own of the people
you asked or accepted. An account it has never seen is a first hello, written
down without a word. So a dishonest server could *add* a reader of its own
rather than replace one of yours, and no phone would raise an alarm. Comparing
keys with a person does nothing about an extra account; what would is the
phone keeping its own list, and **that is not built either**. The written-down
key is also kept against the account and not against the name on your screen,
so a new account wearing a familiar name is a first hello as well.

Every end-to-end encrypted system has the first of those. The second is ours,
and both are written down here rather than papered over.

### A padlock is handed out only where something is about to be locked to it

Eight routes in the whole API carry somebody's public key, and they are listed
by name in a test that forces every one of them to lie, so the alarm can be
watched firing at each. They are the places where your phone is about to seal
something: a search result you are about to send a request to, the people
waiting on you, your mutuals, an album's members, and so on.

A list of the people who reacted to a photograph carries a handle and an id
and no key at all, because nothing is ever wrapped to somebody who looked at a
photograph. Handing over a stranger's padlock would be a door onto somebody
the caller has no way to verify and no reason to trust.

## Taking something back is destroying a key

On most platforms, removing somebody changes a permission: the photograph
stays where it is, still readable by the platform, behind a flag that says do
not show this to them. A permission is a promise the server has to keep.

Here, the only copy of the post key that a person can open is the wrapped copy
in their own delivery row. Removing a mutual deletes those rows in both
directions in one transaction, for every ordinary post, and takes each of you
out of the albums the other made, with the keys that went with them. There is
nothing left to check, because there is no key left to check it against. It is
arithmetic rather than a policy, which is why [removing
somebody](/how-it-works/people/) is quiet and total. The one thing outside that
arithmetic is a backup of our database, which keeps a deleted row for up to 35
days, as the [privacy policy](/privacy/) says, and which nothing in the product
reads back.

What a removal deliberately does not reach is an album a third person made. A
delivery there rests on being in that room rather than on the connection
between two of the people in it, so two people who stop being mutuals go on
receiving each other's [contributions](/how-it-works/albums/) to it. A block
is what reaches in: in its own single transaction, every delivery between the
pair goes, album photographs included.

The same shape, everywhere it appears:

- Deleting a post for everyone destroys two kinds of wrapped key, the
  recipients' and the author's own, at the moment you tap it. The encrypted
  files leave storage eight days later, and the second copy we keep of them is
  gone within six weeks. Neither wait is an undo: the ciphertext is exactly as
  unreadable at the end of it as it was on the first day.
- [Taking somebody out of an album](/how-it-works/albums/) deletes their
  membership and every wrapped key they held for that album's photographs in
  one statement, and anything contributed afterwards is wrapped only for the
  members who exist at that moment.
- [Deleting your account](/delete-account/) destroys every key it holds and
  every key it handed out, in one transaction.
- Removing or blocking somebody, or a request being declined, cancelled or
  expiring, deletes the copy of your profile key that was wrapped for them,
  and with it the ground on which we served them your sealed name and
  picture. The key itself does not change, and a copy riding on somebody
  else's photograph is a separate ground; both are the third limit below.

### The three things this does not do

**Anything already downloaded to somebody's phone is theirs.** Destroying the
key stops anything new from opening; it does not reach into a phone and take
back what has already been decrypted, any more than any other way of sending
somebody a photograph can. The export in *settings → export my data* is
written to respect the same line: it contains what you made, not other
people's photographs, even though your phone holds a key for every one of
them.

**A hidden comment is hidden by a filter, not by a destroyed key.** This is
one of two places in the product where taking something back is a filter, and
it is worth understanding. A comment is
sealed under the post key, which every recipient of the post already holds, so
when somebody falls out of the group who may [hear a
comment](/how-it-works/comments/) what changes is who is shown the words
rather than who could in principle open them. The obvious fix would be to wrap
each comment to just the right people, and it is worse: the writer's phone
would have to be told which of their mutuals know the poster, which discloses
a graph in order to hide one.

**A name and a face are withheld by us, not by a new key.** This is the other
one. Your profile key is derived from your identity key, so it never changes,
and a new name or a new picture is sealed under the same one. Removing
somebody deletes the copy we held wrapped for them, the app never keeps the
unwrapped key, and we stop serving them your sealed name and picture. But a
phone altered to keep that key could open a later name or picture if it could
get the sealed bytes, and the only thing in its way is our server declining to
hand them over. And a removal does not reach a photograph somebody else shared:
while a person you removed can still see a photograph a mutual named you on, or
one of yours that a mutual reshared to them, the copy of your key on that
photograph goes on opening your name and face for them, until your tag, the
reshare or their copy of the photograph goes. A
[block](/how-it-works/people/#blocking-somebody) does reach it: that copy is
destroyed with the rest, and we refuse them your picture and your card for as
long as the block stands.

## A name and a face travel by key as well

Your display name and your profile picture are sealed too, under a key derived
from your identity key. Derived rather than generated, so that whoever can
restore your identity restores the profile with it: generating a second key
would mean backing it up, and this product names exactly one way to lose your
photographs and does not want a second thing to lose.

That key is wrapped for each person who may read it: your mutuals, and anybody
you have sent a request to. It is why an incoming request shows you a face and
a name while somebody you asked shows you nothing until they accept. It is
also why we cannot compose a notification: we hold the name as ciphertext.

There are two places your profile key is handed to somebody by a third party,
and they are unusual enough to name. The second is a reshare: somebody you
named on a photograph of yours, where you allowed it, passes the post's key and
your profile key on to the people they chose, and that copy rests on each
viewer's copy of the reshare. The first is the tag itself. When a mutual puts
your name on a photograph, the
people who see that photograph may have no connection to you and could not
open your name or your face. So the person who tagged you re-wraps your
profile key onto that post, from their own phone, for each of those viewers.
We hold the copies and cannot open one. Each copy rests on the viewer's
delivery and on your tag, so it disappears when either does, without any part
of the system having to remember to delete it. The third party handing over
the key is the person who named you, and the switch that permits any of it is
yours: *let mutuals tag me*, in *settings*.

## What a notification carries

One word: the kind of thing that happened.

The message we send to Google's push service is a data message with one field
naming a type, and a delivery priority that is worked out from the type and
so says nothing the type does not. There is nothing else in it: no names, no
captions and no post identifier. The sentence you read on your phone—*anna
commented on your post*—is composed on your phone, from the sealed profile
it can open and we cannot. When it cannot open a name, the notification says
*Somebody*, which is the same phone doing the same work with less to go on.

The identifier is the part people are surprised by, because it looks harmless.
Two devices receiving the same post id in the same second are two people in
one audience, and repeated often enough that is the shape of your graph,
handed to a third party. It costs nothing to leave out, since a phone that
must fetch to learn a name will learn the id from the same answer.

The type is a list of fixed cases with no fields on them, which is what makes
"no digests, no streaks, no you-haven't-posted-in-a-while" a property of the
system rather than a note for a reviewer. There is no string a marketing
sentence could be put into, no identifier to correlate two phones with, and no
case for a reaction. And because the message carries no text of any kind,
Android is never asked to post words we chose.

## What the app measures

There is no crash-reporting library and no analytics library in the app. Not
disabled, not opt-out: absent. Every product in that category exists to
capture what the client is holding in memory—breadcrumbs, local variables,
the view hierarchy, the text in a field—and on this phone that is where the
decrypted photographs are. Because a decision that is an absence has nothing
that goes red on its own when somebody adds a dependency in a hurry, a check
in our build refuses fourteen of them by name, in every one of the app's
build files and in the list of versions they share, and refuses the
platform's own logging calls in the app's source. What we get instead is
Google Play's own crash reporting, from phones whose owners turned that on at
the operating-system level, which tells us the app crashed and where in our
code and contains none of your content.

One thing does go the other way, and it is on by default with no switch. Your
phone counts how many sealed things it opened and how many it failed to open
since it last told us—post keys, metadata, frames, comments, album keys,
album titles, profiles—along with the version of the app and the version of
Android, and it counts a file that never arrived separately from one that
arrived and would not open, because the first says something about storage
and the second says something about keys. Never which post, which frame or
whose comment: a failure named by post id would be a row we could join to the
graph.

That number matters because it is the one failure we cannot see for ourselves.
We hold ciphertext and a wrapped key; whether they open is decided on a phone.
The server adds each count to a total and answers with nothing: no row, no log
line, no identifier, so the link between you and the numbers exists for the
length of the request and then does not. There is no switch because there is
nothing here a switch would withhold, and a switch beside a sentence
explaining that it withholds nothing would be the product announcing itself.

The other half of that number is *settings → report a bug*, which is a
paragraph you write and one line about your phone, with no attachment field,
no log and no screenshot. The counter says how often something failed to open.
Only a person can say what they were doing.

### Logs and metrics

Our logs cannot name you, by construction rather than by care. There is one
way to write a log line, and none of the fields it accepts can hold free text,
so a handle, an address, a caption or a token cannot reach a log line by type.
The access log records which route was called and not which path, so what gets
written is the shape of it, /v1/users/{userId}/posts, and never the identifier
that was in its place. An exception is rendered as its class and its stack
frames and never its message, because a library's error message quotes
whatever it choked on. We keep those logs for 30 days.

The operational metrics have no field anywhere that could carry an account,
and every label on them is a fixed word, a small number, or an app version
folded into "other" once there have been more than 32 of them. They are served
on a separate port that is not exposed publicly, and a test asserts they are
absent from the public one, because keeping something off a public API is a
fact about the network rather than a thing that goes red on its own.

## What this does not protect you from

The claim above is narrower than "private", and these are its edges.

- **Metadata.** We know who you are connected to, who you sent a post to and
  when, and whether each of them has seen it and when they first did. That is
  what the server needs to deliver anything at all, and it reveals who talks
  to whom. The [privacy policy](/privacy/) lists it in full.
- **What a recipient keeps.** Anything already on somebody's phone is theirs.
  The app does not stop screenshots and cannot recall a photograph from a
  phone that already downloaded it.
- **Screenshots of your own screen.** The app does not block screenshots
  anywhere, including the screen that shows your six words.
- **The first hello.** A server that was dishonest at the very first exchange
  between two people is caught only if they read their keys' short names to
  each other, above. Nothing asks them to, so most people never will.
- **Accounts made before the second key.** An account made before the app had
  quantum-safe keys has only the older kind, and what is sent to it is only as
  safe as that. The phone cannot add the second key by itself, because the new
  key has to go into the backup your six words open, and the phone does not
  keep your six words. Anything already copied before a key is added stays as
  it was.
- **Something sent to you under one lock.** The second lock is put on by the
  sender's phone, and there are two ways it can be missing on an account that
  has both keys. A phone running a version of the app from before the second
  key seals with the older lock alone, because it does not know there is a
  second one; that stops once everybody has updated. And a dishonest server
  could hand somebody only your older key at the first hello between you:
  their phone would then seal everything to you under one lock for as long as
  the server kept it up, and yours would open it without a word. Nobody can
  read either today; what is at stake is a copy kept for a quantum computer.
  The second case is caught the way the first hello is, by reading your keys'
  short names to each other. Your phone does not refuse something sent under
  one lock yet, because somebody still on an older version would then send you
  posts you could not open.
- **Who a post is sealed to.** The list of people your phone seals a post to
  comes from us, asked for again at the moment you post, and your phone keeps
  no list of its own to check it against. A dishonest server could add an
  account of its own to that list and be handed a copy of the post's key, with
  no alarm on any phone and nothing on your screen that need show it. If
  *share past posts with new mutuals* is set to *always*, which is not how it
  starts, such an account would be handed what you had already shared with
  everybody as well. We could also put a real mutual into a group you did not
  put them in.
- **Who a post is from.** Nothing in a post proves who made it: nothing is
  signed, and the name over a post is a field we fill in. A dishonest server
  could seal a photograph of its own choosing to your key and deliver it under
  a mutual's name, or put one mutual's name on a post another sent. What it
  cannot do is open a genuine post or write anything new inside one; it can
  go on serving an earlier version of a caption or a comment after its author
  edited it, because nothing sealed says which version is the latest. A comment is
  bound to its author's account as it is sealed, so we cannot move one
  person's words under another's name without first holding the post's key.
  Reactions are not sealed at all, so those are ours to write.
- **Withholding.** We can refuse to hand back your sealed key backup, or hand
  back an older one. Both cost you a restore; neither reads a photograph.
- **A password somebody can guess.** The key we hold for a password can be
  used to test guesses at it, as any stored password can. We could do that,
  and so could anybody who took a copy of our database, with no limit on how
  many guesses. Each guess costs the same deliberately slow calculation your
  phone does, and a long password puts it out of reach. A guessed password
  opens the account and never the photographs: only your six words do that.
- **Length.** Ciphertext is about as long as what went into it, so we can tell
  roughly how long a caption is. Nothing pads it.
- **Things that are deliberately in the clear.** Reactions, group names and
  who is in them, album membership, and whatever you type into a report or a
  bug report.
- **Your own export.** *settings → export my data* writes a decrypted copy
  into your phone's downloads, where anything that can read that folder can
  read it, and wherever the folder is backed up to. The app says so before it
  runs.
- **A phone somebody else controls.** A rooted, unlocked phone in the wrong
  hands defeats all of this.

[What encryption means for moderation](/moderation/) is a separate page,
because it is the same constraint seen from the other side: we cannot review
what we cannot read, so whatever we do, removing the one post a report points
at or acting on the account behind it, is decided on what the report says.

The rest of [how it works](/how-it-works/) describes the product these choices
add up to.
