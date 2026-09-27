---
title: Posting a photo
permalink: /how-it-works/posting/
---

This page is how a photograph gets from your phone to the people you chose,
and what happens to it afterwards. Most of it works the way you would expect.
Where it does not, one decision is usually behind it: a post in *people you
know* is delivered to people, not published to a place. There is no page it
sits on for somebody to come across, no web address for it, and no setting
that would make one. There is no such thing as a public post here.

**Last updated:** 27 September 2026. This page covers the closed beta.

## Choosing the photos and videos

The rightmost mark on the bar at the bottom opens the composer. Its label is
*post*, which is also the title of the screen it opens and the word on the
link that publishes.

Photographs and videos come from Android's own photo picker. *people you know*
has no permission to read your photo library and never asks for one: the
picker hands the app what you chose and nothing else. The app asks the phone for
the internet, for notifications, and, on Android 9 and older only, for
permission to write a saved photograph into your gallery. That is the whole
list.

One post holds up to 32 of them, photographs and videos together in any
order. *choose photos and videos* becomes *add more* once something is picked,
and the number beside it names what you have: *1 photo*, *4 photos*, *1
video*, or *3 photos and 1 video*.
Each row is a small square of the photograph itself with *remove* beside it
and a *=* handle that drags it into a new position; the order of the rows is
the order the photographs appear in the post. Picking the same photograph
twice adds it once. The limit is mentioned only when you actually reach it,
and then it says so plainly: *That is the most photos and videos one post can
hold (32).*

There is no crop tool, no filter, no rotation and no markup. What you pick is
what is posted, and nothing you post is ever cropped. The only cropped picture
in the product is your own profile picture, which has to fill a circle beside
a name. The small square beside each row here, and the tiles of the grid a
long post is drawn as, are contact sheets: square previews of a photograph
that is kept whole.

### Every EXIF tag is gone, because nothing is left to strip

Each photograph is decoded and re-encoded on your phone before it is sealed. A
decoded image has no EXIF, so every tag is simply absent from what leaves the
phone: GPS, device model, serial numbers, lens, the software that wrote the
file. Nothing is filtered, so nothing can be missed by a filter.

The one thing kept is the moment the picture was taken, and it rides inside
the sealed metadata rather than on the file, because writing a tag back onto a
JPEG would mean putting a decrypted photograph on disk for the length of the
write. The decoding and re-encoding happen in memory. What the app does write
to your phone unencrypted, and for how long, is
[listed further down](#what-is-written-to-your-phone-unencrypted).

## Posting a video

A video's row shows a still of it with a small mark that says it plays, and
otherwise it is a row like any other: *remove*, the *=* handle, and its place
in the order.

### A video longer than a minute keeps one minute of it

A video can run to about a minute. A longer one is not refused. Its row
carries *choose which minute*, which opens a still of the video with a slider
under it. Moving the slider moves where the kept minute starts, and the still
follows it, so you find the part you meant by looking at it rather than by
reading times. The slider's handle is as long as the minute is in the whole
video—a third of the line on a three-minute video, most of it on a
seventy-second one—so you can see how much you keep and where it stops. There
are no times anywhere and no second handle, because the length is always the
same minute; dragging to the end keeps the last one. If you choose nothing,
the first minute is kept.

### What happens to a video

It is converted on your phone before it is sealed: to the format every phone
plays, no larger than 1080 pixels on its short side, and small enough that a
minute of it can travel on a phone's connection. Like a photograph, it keeps
nothing of the original file but its pictures and its sound. The location, the
device and every other tag are gone, and the moment it was recorded rides
inside the sealed metadata, as a photograph's does. What you see on the row is
a still of the converted video, and so is what everybody else sees before they
tap it.

A converter writes a file, so the converted copy sits unencrypted in the app's
own cache, which nothing backs up, for as long as it takes to seal, and it is
deleted the moment it is sealed. It is one of
[four things](#what-is-written-to-your-phone-unencrypted) the app writes to
your phone unencrypted. Everything that leaves the phone is sealed under the
post's key, a piece at a time.

### How a video plays

Nothing plays until you ask it to. In the feed a video is a still with the
mark over it, and tapping it opens the post, as tapping a photograph does. On
the post, tapping it plays it full screen. There, a tap pauses it, another
plays it again, and at the end it goes back to its still. It plays with its sound, at your phone's volume.
There is no sound switch in the app, because nothing plays that you did not
tap. Swiping to another photograph stops it.

A video you receive is never written to your phone unless you save it: it
plays straight out of its sealed copy, a piece at a time, and nothing readable
is left behind when it stops.

## The caption

The field says *say something (optional)*, and it means it. A caption can run
to a couple of thousand characters and there is no counter.

It is sealed in the same envelope as the rest of the post's metadata: each
frame's dimensions, its blurred placeholder, and the capture time. There is no
caption to send on its own.

You can edit it for ever, from *more → edit caption* on your own post, and
clearing the field removes it altogether. An edit re-opens that whole sealed
envelope, replaces the one field and seals it again under the same post key,
so what our server sees is a new blob arriving. It cannot tell that the
caption is what changed. An edited post carries the word *edited* under it,
and the honest limit is worth stating: a dishonest server could set that stamp
or hide it. It could not forge a caption, which would need the post key.

## Choosing who sees it

The heading over the picker is *who sees this*. Your
[groups](/how-it-works/groups/) come first, then a searchable list of your
individual mutuals, as one list of boxes over both rather than a mode switch.
A post can be addressed to several groups at once, or to one group plus one
person, or to one person.

Only your mutuals can be in the audience you pick: people you and they both
agreed to connect with. There are no followers here and nothing addressed to a
friend of a friend. The one exception is an album, further down, where the
audience is the album's membership and can include co-members of it you are
not connected to.

A post addressed to exactly one person is a post, not a message. It has the
same comments and the same reactions as any other, and there is no thread, no
typing indicator and no inbox anywhere in the app.

### Everybody is the one box that combines with nothing

This is the rule most people meet first and find strange. Tick any group or any
person and Everybody clears: its box goes pale and stops answering to a tap.
Its line is the same either way, the count of everyone you are mutuals with,
because every row in that list answers with a count.

The reason is arithmetic. Everybody resolves to every mutual you have, so
Family is inside it and Ana is inside it. Ticking Family alongside Everybody
reaches nobody new: both boxes ticked delivered exactly what Everybody alone
delivered, and read on the screen as something smaller than what was about to
be sent. The claim this composer makes is that the audience is chosen, and a
selection that does not say what it does is not a choice anybody made.

The obvious alternative was refused too. A tap on Everybody does not sweep the
other boxes away, because things disappearing under your thumb is the wrong
behaviour anywhere and worst on the screen that decides who sees a photograph.
Untick what you ticked and Everybody's box comes back to life.

### The picker opens where you left it, and that memory stays on your phone

The composer opens with last time's boxes already ticked, because the common
case is the same people as last time and it should not cost the same taps as
the rare one.

That record is a small file in the app's own storage, kept per account, and it
is never sent to us. The audience of your last post is a fact about your
habits; our server already learns the audience of each post as it delivers
one, and there is no reason to also hand it a standing answer to who this
person usually talks to, askable without a post being made. The honest cost is
that a new phone opens an unticked picker.

Two smaller rules go with it. The remembered set is narrowed to what the
picker is actually drawing, so a group you have since deleted or somebody you
are no longer connected to drops out silently: a ticked box you cannot see on
screen is not a choice you made. And it is written only after a post has
actually landed, never from a draft that failed.

### Contributing to an album has no picker at all

*add photos* on an album's screen opens the same composer with one line where
the picker would be: *everyone in Maine*. The membership is the audience, and
nothing else can be named beside it. Widening means adding somebody to the
album, which the [albums page](/how-it-works/albums/) covers.

## Naming somebody in a photograph

A *tag* link sits on the row of each mutual in the picker, and only on the
rows of mutuals who have left *let mutuals tag me* switched on, which it is
until they turn it off. Up to 32 people can be named on one post.

Naming somebody ticks their audience box and holds it there. A tag is a name
on a photograph the person can see, so the two cannot come apart; *untag* is
the only way to release the box, and it hands it back only if the tag is what
ticked it in the first place.

The names appear under the author's name as *with anna, bruno*, and every
viewer of the post sees them, not only the people who know them. A name that
belongs to somebody the viewer has no connection to opens that person's card.
It is one of the few places here where a stranger is named to you: an album's
member list is another, and so is the list of who chose a reaction, because
both are somebody else's people rather than yours.

Taking a name off belongs to the person named, from *more → remove my tag*. As
the poster you can neither add a name nor remove one after posting.

Once somebody is named, a checkbox appears: *tagged people may reshare this*,
off by default and shown only once there is somebody it could be about. It
lets anybody you named pass the photograph on to their own mutuals, as a post
of theirs drawn under your name and face. You can give that permission or take
it back afterwards from the post itself, and taking it back destroys the
reshares that rested on it.

Somebody you name is told in their activity tab, and being named is the one
thing the tag switch allows their phone to be notified for. The notification
arrives instead of the one they would have had for your post rather than
beside it: one photograph, one interruption. Turning *let mutuals tag me* off
stops the naming and the notification together.

## Publishing

The *post* link at the foot is not tappable until there is at least one
photograph and an audience. There is no error message for having chosen
nobody: the link simply does not answer.

Then, on your phone, in this order: every recipient's key is fetched and
checked against the copy your phone pinned the first time it saw it; a fresh
key is made for this post and no other; each photograph is decoded,
re-encoded, sealed and released, one at a time, so that thirty-two of them do
not have to fit in memory together; the sealed files are uploaded; and the
post key is wrapped once for each recipient and once for you. While it runs
the link reads *posting* beside a ring that fills. There is no percentage: a
number invites arithmetic, and what you want to know is whether it is nearly
done.

If any recipient's key has changed since your phone last saw it, the whole
publish stops before a single byte is uploaded and you are shown an alarm
naming that person. Sending to everybody except them would be the worst of
both outcomes: the photograph goes out anyway, and the one signal that
something is wrong becomes something you get past by carrying on.

The post and every delivery are written together or not at all, and the
audience is resolved again at that instant. Somebody you removed a moment
earlier drops out, and our server delivers to nobody outside the audience your
phone declared, even if a phone tried. That is our server checking a phone;
what a phone can check of our server is narrower, and [how the privacy
works](/how-it-works/privacy/) says where it stops.

### Where you land

The composer closes and you are on your own profile, where the post you just
made is the newest row—unless it was a contribution, which lands on the album
it went to. Nothing says "posted". Announcing it would be the product
congratulating itself.

Nothing tells you how many people got it, either. Our server does answer your
phone with a recipient count, because it has just made that many deliveries,
and the app draws it nowhere. Nothing in this app counts how far a post went.

### Your own post is not in your own feed

There is no delivery from you to you. Your copy of the post key is a column on
the post itself, which is what lets you read your own archive and share the
post with somebody later. [Your feed](/how-it-works/feed/) is a queue of what
other people sent you; your posts live on your profile.

### When a post is refused

- Addressing Everybody before you have any mutuals: *There is nobody in that
  audience yet.*
- A great deal uploaded in one hour: *That is a lot at once. Try again later.*
  The refusal never states the number, and never which of the ceilings it was.

A photograph the phone cannot decode fails the publish with a sentence, and
nothing is sent. So does a video: *A video in that post could not be read. Try
choosing it again.* A video whose conversion comes out too large is converted
again, smaller, and only when two more tries have not made it fit does the post
say *A video in that post came out too large to share. Try a shorter one.*

Two more refusals live on our server and are backstops rather than sentences
you should ever read: more than 32 photographs, and a single file too large
for us to take. The picker stops at 32 before the first can happen, and the
re-encode further down puts every photograph far under the second.

## How a post is drawn

Up to eight photographs are a carousel you swipe, with dots under it. Nine or
more are a two-by-two grid of the first four in the order you put them, with a
link reading *view all 24 ->*—the post's own number—into the full-screen
viewer. The first four, not the best four: choosing the best four would be
this app ranking somebody's photographs, which is the one thing it does not
do.

No photograph is ever stored or sent cropped, and none is refused for its
shape. What is bounded is the box it is drawn in, and only so that one frame
cannot own the screen: between 1:2 and 2:1, and never taller than three fifths
of the screen. A 4:3 photograph from a phone held upright sits exactly at that
second bound and is drawn the full width of the row. A 9:16 crop, a stitched
panorama or a long screenshot is fitted inside the box whole, smaller, with
margins, so nothing is hidden. Tapping it opens the full-screen viewer, which
has no bound at all, and that is what "see the whole thing" means here.

What is stored is not your camera original. Each photograph is re-encoded on
the phone at up to 3,200 pixels on its long edge—a ceiling and never an
upscale, so a smaller photograph is left at its own size—which is enough to
look right on a real computer screen rather than only on a phone. That is why
the app's own label says *save photo* and not "save original": it will not
promise something we do not keep.

## There are no drafts

A post you have not sent is not saved. The photographs you picked, the caption
you typed and the boxes you ticked live in the screen and go with it.

So leaving asks, once, if you have chosen or typed anything. The dialog is
titled *discard* and says: *Nothing will be posted, and what you have chosen
will be lost.* Both the arrow at the top and the system back gesture go
through that same question, which was not always true: the gesture used to
walk straight past it, and a guard one of the two ways out ignores is not a
guard.

### A post you have sent is written down until it goes

The moment you tap *post*, the app has told you it is sending, and it keeps
that word even if it closes. So a post that is on its way—and only one that
is—is written to your phone: the caption, who it is for, and a copy of each
photograph and video, in the app's own storage, which no backup copies and
nothing else on the phone can read. All of it is deleted the moment the post
goes out, and the moment you discard it.

If the app closes before it goes—you swiped it away, it crashed, your phone
needed the memory for something else—the post is waiting for you at the next
launch, at the top of your profile, saying *This post did not go out. Nothing
was posted.* Under it are the same two things any post that stopped carries:
*try again*, which sends that same post rather than a second copy of it, and
*discard*, which throws it away and deletes the copies with it. Nothing is
ever sent again on its own. A post you composed on Tuesday does not go out on
Thursday because you happened to open the app.

## What is written to your phone unencrypted

Everything that leaves your phone is sealed. Before that, four things are
written to your phone's storage unencrypted. All four are in the app's own
storage, which no backup copies and no other app can read.

- **A photograph you take with *take a photo*.** It goes into the app's own
  folder and not your library, so until you post it, that file is the only
  copy. It is deleted the next time you open the app and take a photograph, if
  it has not been cleared before then, and at once if you back out.
- **On an iPhone, a copy of every photograph and video you choose.** The
  iPhone's picker lends the app a file and takes it back straight away, so the
  app keeps a copy of its own. It is deleted the next time you open the app and
  choose or take something, if it has not been cleared before then.
- **A copy of each photograph and video in a post you have sent**, until the
  post goes out or you discard it, as the section above says.
- **A converted video**, while it is being sealed. It is deleted the moment it
  is sealed.

*save photo*, *save video* and *export my data* write decrypted copies too,
because that is what you asked for. Those land where you can find them, and
each is described where it happens.

## Sharing a post with more people afterwards

*more → add to audience* on your own post opens the composer's picker again,
with one difference: everybody the post already went to is ticked and cannot
be unticked, each row marked *already shared*. Only what you newly tick is
sent. The action is *add* and the confirmation is the single word *added*,
with no number. When there is nobody left, the screen says *everyone you know
already has it*.

The worked case is the one everybody has. The baby photographs went to
Everybody in March. Ana became a mutual in August. In September you open one
of them and add her, and she gets it.

This is one of two ways an audience grows, and both are things you did on
purpose. The other is *sharing the past*: when somebody becomes a mutual, or
is added to a group, the app offers to share what you had already posted to
Everybody or to that group, by name and one person at a time. The
[people page](/how-it-works/people/) and the
[groups page](/how-it-works/groups/) cover it. The key work is the same either
way, and it happens on your phone: it opens your own copy of the post key and
wraps it again for Ana. Our server has never held a key it could have handed
her, which is also why Ana scrolling your profile cannot quietly grant her
anything.

Two consequences of the dates are worth knowing. A post added to somebody's
audience is stamped with now, so it arrives in their feed as new rather than
sinking to wherever March would put it, while the row itself still says
*posted on 3 march*. And adding a group takes that group's members at the
moment you add them, exactly as publishing does.

*add to audience* is not offered on an album contribution, whose audience is
the album, or on a reshare, whose audience is what the resharer chose once.

### Nothing can take somebody out of a post

There is no control for it anywhere, and it is not an oversight. When the post
was published, the key was wrapped for each person in the audience at that
moment, and it is already on their phone. Taking a permission away would not
help; what works is destroying the key.

So there are two remedies, and both are bigger than the post.
[Removing somebody](/how-it-works/people/) as a mutual, or blocking them,
destroys the wrapped keys between you in both directions. *delete for
everyone* takes the post back from everybody at once. What neither can do is
reach a photograph somebody has already downloaded or screenshotted, and no
app can.

## Saving a photograph out of a post

Anybody who can see a post can save its photographs, from *more → save photo*.
It saves the one you are looking at, which is not necessarily the one the post
opened at, and it follows your swipe the instant you swipe: which photograph
am I saving is not a question that should lag behind your thumb. It always
fetches the full-size copy, even when the smaller one is already on screen.

Files land in *Pictures/people you know/* on Android 10 and later, and in the
gallery without that folder on Android 9 and older. A video is saved the same
way, from *more → save video*, into *Movies/people you know/*: the minute that
was posted, as it was converted, and not the file it was made from. The confirmation is a
snackbar reading *saved to your photos*. The capture time is put back as the
file's date, so a photograph from 2019 sorts where it belongs in your gallery
rather than at the top dated today. Everything else that was on the original
file is still gone, because it was gone before the photograph ever left the
phone that took it.

Screenshots are not blocked. What you share with somebody, they can keep, the
same as with any other way of sending a photograph.

## Deleting a post

*more → delete for everyone*, on your own post. The confirmation is a sentence
rather than "are you sure": *Everyone loses this photo straight away, and it
cannot be brought back. The files are gone from our servers by 23 october.*

At the tap, every wrapped copy of the post key is destroyed: the recipients'
copies and your own. The comments were sealed under that same key, so they
close with it. Eight days later the encrypted files come off storage, and the
reactions go with them: a reaction is a single emoji and was never encrypted.
What stays is the post's row, marked deleted, which still says when it was made
and who it was addressed to; the [privacy policy](/privacy/) lists it.

We also keep a second copy of the encrypted files, in case storage ever loses
them. It lets go of a deleted file 30 days after storage does, and the date in
the confirmation is the day the files are gone from there too.

None of that waiting is a grace period or an undo. The ciphertext is exactly
as unreadable at the end of it as it was on the first day; there is nothing an
undo could restore. The confirmation names the date rather than counting down
to it, which is the habit throughout the app.

Deleting is never gated. A suspended account can still delete its own posts,
because this is the act that narrows rather than adds, and what stays
published should not depend on the state of an account.

## Your own posts

The person mark on the bar opens your own profile, which is also where
publishing lands you. Below your face, the people you know and your groups and
albums, there is *your posts*: one row per post, with its caption and the line
*posted on 3 march*. Before you have made any it reads *nothing yet*.

There is no count on it and nothing that grows. It is visible only to you.
Asking for your own profile the way somebody else would gets nothing back,
because a profile here is simply the posts of that person you personally hold
a delivery for, and you hold none from yourself. What another person sees of
you is what you shared with them, and it differs per person, so there is no
single version of it to preview.

## What there is no way to do

Worth stating plainly, because several of these are standard elsewhere:

- Make a post public, give somebody a web address for one, or let somebody see
  one without either being addressed in it or receiving it as a reshare you
  permitted.
- Add, replace or reorder photographs after posting. What can still change on
  a published post is the caption, the audience, and whether the people named
  on it may reshare it.
- Take one person out of a post's audience.
- Schedule a post, or save a draft.
- Find out who looked at a post, or how many people received it. Nobody is
  told who looked at anything here, including you about your own posts.
- Crop, filter, rotate or edit a photograph you are posting.
- Post a text post or a link, or a video longer than about a minute; a longer
  one keeps the minute you choose.
- Play a video without tapping it, or turn its sound down anywhere but on the
  phone itself.

The [rest of the guide](/how-it-works/) covers the other halves of this: who
can hear a [comment](/how-it-works/comments/) on a post, what a
[group](/how-it-works/groups/) does and does not do, and what happens to a
photograph when somebody is [removed](/how-it-works/people/). The
[privacy policy](/privacy/) says exactly what we hold while all of it is
happening.
