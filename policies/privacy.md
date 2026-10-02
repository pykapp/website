---
title: Privacy policy
permalink: /privacy/
---

*people you know* is a private photo-sharing app for the people you actually
know. This page says what we hold about you, what we cannot see, and what
happens when you leave. It is written to be read, not skimmed; it is short
because there is not much to say.

**Last updated:** 1 October 2026. This policy covers the closed beta.

## Who is responsible, and where this applies

*people you know* is operated by **people you know llc**, a Texas limited
liability company, at 2222 N Alamo St #118, San Antonio, TX 78215, United
States. We decide what is collected and why, which makes us responsible for it.
The company is represented by its managing member, **Jean-Sébastien
Basque-Girouard**.

The same person is in charge of protecting personal information, at that
address or at **pykapp+privacy@proton.me**, which is also the way to reach us
about anything else on this page.

The app is offered in the United States, Canada, New Zealand, Singapore and
Japan. The privacy law of the country you live in applies to what we do with
your information:

- in the United States, the law of the state you live in;
- in Canada, federal privacy law (PIPEDA) and, if you are in Québec, Québec's
  Law 25;
- in New Zealand, the Privacy Act 2020;
- in Singapore, the Personal Data Protection Act 2012;
- in Japan, the Act on the Protection of Personal Information.

## The one-sentence version

Your photos, captions, comments, names and bios are encrypted on your phone
before they leave it, with keys we never see. We hold the encrypted files,
copies of those keys that are locked so that we cannot use them, the list of
who you are connected to, and the bookkeeping needed to deliver things between
you. We do not scan, read, rank, or sell any of it.

## What we cannot see

Everything you would call content is sealed on your phone under keys that
only your phone and the phones of the people you share with can use:

- photos, at every size we store them;
- captions;
- comments;
- your display name, your bio and your profile picture;
- the names of your albums;
- the names of your groups. A name given to a group before this version of the
  policy stays readable to us until you open the app after updating it; the
  app then seals the name.

We store these as ciphertext. We cannot open them, and neither can anybody
who obtains a copy of our servers. If you lose your recovery phrase and every
phone that holds your key, your photos are gone. We cannot recover them, and
this is deliberate: there is no copy that is ours to hand back.

We also hold keys, every one of them locked before it reached us:

- a copy of your own key, sealed on your phone under the six words of your
  recovery phrase. It is how a new phone gets your key back. We never see the
  six words, so we cannot open it; anybody who had both our copy and your six
  words could, which is why the words are yours alone to keep;
- a list of the keys your phone has been given for the people you have met
  here, and of which of those people you added, sealed under your own key, so
  that a new phone can notice if a key is ever swapped and knows who you chose
  to share with. We cannot open that either;
- for each post, album and profile you can open, a copy of its key locked to
  your public key, which only the key on your phone opens.

Beside the first two we can read what it takes to store them and nothing more:
the settings your phone needs to turn six words back into a key, a version
number, and when each was last saved.

## What we can see

To deliver a photo to the right people we hold, in the clear:

- your handle, and your email address if you gave us one;
- if you set a password, a public key your phone made from it and the settings
  your phone needs to make that key again. We never receive the password
  itself. The key cannot be turned back into it, though it can be used to test
  guesses at it, as any stored password can. An account keeps at least one of
  the two, an email address or a password, and may have both;
- if we were full when you tried to join and you asked to be told when there
  is room, the address you gave and when you asked, and nothing else, until we
  have written to it about a place;
- who you are connected to, and when you connected;
- add requests you send and receive, blocks you place, and anybody whose
  posts you have muted (a mute is yours alone; the other person is never
  told);
- an email address somebody typed to invite a person into an album, and when,
  until that person joins or the invitation lapses. If the person at that
  address asks us to stop sending invitations, we keep a fingerprint of the
  address (a one-way hash of it, not the address), so that we never email it
  an invitation again;
- the country your phone was set to when you made your account or, if you made
  it before 22 September 2026, the first time you opened the app after updating
  it. It is written once and never updated. We use it only to count how many
  people we serve in each country, because some countries' laws start to apply
  once a service has enough users there;
- which of your groups a person is in (never shown to that person);
- who is in each album you are in;
- for every post: who made it, when, whether and when it was edited, who it
  was addressed to or which album it is in, who is named on it, whether it
  shares somebody else's post again, how many frames it has, whether each is
  a photograph or a video and how long a video says it runs, how large the
  encrypted files are, the signature the author's phone put on it (which shows
  who made it and says nothing about what is in it), and whether each
  recipient has seen it and when they first did. That is one moment per person
  per post; nothing records which photographs anybody looked at, and nobody is
  ever shown it;
- for every comment: who wrote it, on which post, when, and which comment it
  answers;
- reactions, which are one emoji each and are stored in the clear because a
  single emoji from a known set cannot be meaningfully encrypted;
- the text of any report you file, because a report is a message to us and
  we have to be able to read it; and, if somebody reports you, that they did,
  what they wrote, what we decided and when, and whether your account is
  suspended;
- the text of any bug report you send, and the one line shown to you before
  you send it: the version of the app, the version of Android or iOS and the
  model of your phone. Nothing else goes with it—no screenshot, no log, no
  file—and the app has no way to attach one;
- your activity list: what happened, who did it, on which post, when, and
  when you read it. An entry is kept for 128 days;
- whose posts you have asked to be told about, and the other switches in your
  settings;
- for each phone you have signed in on: its push token, whether it is an
  Android phone or an iPhone, which build of the app it runs, and when you
  signed in there and last used it;
- your two public keys, the one your photos are locked to and the one your
  posts are signed with. Both are the halves that are meant to be handed out.
  We also keep when the first was published;
- the moment you confirmed you were 18 or older (never your date of birth);
- counts of what your phone could and could not open, added to a total the
  moment they arrive and not kept against your account.

This is the honest boundary of the claim. It is metadata, and metadata
reveals who talks to whom. We keep it because the app cannot work without it,
we keep as little of it as we can, and we keep our access logs for 30 days
and no longer. Those logs record which kind of request was made and when, and
not who made it: no address of yours, no identifier, no page you asked for.

## What we use it for

We use what we hold for these things and nothing else:

- to make your account, sign you in, and send the one-time codes that sign-in
  uses to your email address;
- to deliver what you post to the people you chose, and what they post to you;
- to send you the notifications you allowed;
- to write to you once there is room, if we were full and you asked us to;
- to send one email to an address somebody typed to invite a person into an
  album, and to stop when that person asks us to;
- to act on reports and keep people safe, as the [moderation
  policy](/moderation/) and the [child safety standards](/child-safety/)
  describe;
- to find out that something is broken, from the counts your phone sends and
  the bug reports you choose to send;
- to do what the law requires of us.

A handle, your date of birth, and an email address or a password are what an
account needs: without them we cannot make one. Everything else is yours to
give or not.

## Where it is held, and for how long

Our servers, our database and the second copy of the encrypted files are in
data centres in the United States. The encrypted files themselves are in object
storage run by a company based in the United States, in its North American
region; it holds ciphertext and never a key.

**If you live outside the United States, your information is held outside your
country**, and while it is there it is subject to United States law, including
lawful requests by US authorities. We are telling you because Québec's Law 25
and Japan's privacy law require it and because it is the kind of thing you
should be able to find out without asking.

What such a request could reach is what this page already says we hold: the
encrypted files and the locked keys, neither of which we can open, and the
metadata. There is no key here that we can use, and so none that anybody can
compel us to hand over or to use, which is the point of the whole arrangement
rather than a happy accident. What a server made to act dishonestly from then on
could do is a different question, and [how it works](/how-it-works/#what-the-encryption-does-not-protect)
answers it.

The United States has no single national privacy law of the kind Canada, New
Zealand, Singapore and Japan have, and no national privacy regulator like
theirs. Privacy there is protected by federal laws that each cover one kind of
information, by the privacy laws some states have passed, and by the Federal
Trade Commission, which can act against a company that breaks the promises its
privacy policy makes. We decided how to protect your information knowing
that, and what protects it here is therefore what this page commits us to,
which is the same whichever country you live in, and the fact that we cannot
read your content at all.

We keep what is above for as long as your account exists, and then:

- when you delete your account, the keys go at once, the sealed copy of your
  own key among them, and the encrypted files leave storage eight days later;
- the second copy of the encrypted files follows storage within a day, and
  keeps a file storage deleted for 30 days more, in case it was deleted by
  mistake. So a file you delete is gone from it within six weeks, and until
  then it is ciphertext whose keys were destroyed when you deleted it;
- backups of our database are kept 35 days, and the output of anything we run
  by hand against the database is kept 90 days, so a row deleted today, a
  deleted account's included, can survive in those for that long and no
  longer;
- access logs are kept 30 days;
- the database's own log of errors is kept 30 days, and it can name the handle
  or the email address an error was about;
- the counts your phone sends are added to a total on arrival and are never
  stored against your account, so there is nothing to keep;
- the record of a search is swept after the hour it is rate-limited over;
- one-time sign-in codes, with the address they were sent to, and the record
  of each password sign-in, with the handle it was for and how many wrong
  guesses it drew, are swept after two days, which is what the limits on wrong
  guesses need to read;
- after deletion we keep only the record described under *Deleting your
  account* below.

## How we protect it

- Your content is encrypted on your phone before it leaves, with keys we never
  hold in a form we can use, so the most sensitive thing you give us is never
  readable here.
- Everything between the app and our servers travels encrypted.
- Our database is encrypted where it is stored and cannot be reached from the
  internet, only from our own servers.
- Only the people who run the service can reach our servers and our database,
  and the person named at the top of this page is responsible for how they
  do.
- We keep as little as the app can work with, and delete it on the schedule
  above.

## What you can ask for

- **See it.** *settings → export my data* writes your posts, captions,
  comments and the handles of your connections to your phone, decrypted there
  because we hold nothing readable to give you. If you no longer have the
  phone, write to us and we will send what we hold.
- **Correct it.** Your handle and your display name are yours to change in the
  app. There is very little else we hold that you could correct, because we
  hold very little.
- **Delete it.** *settings → delete my account*, or [this
  page](/delete-account/) if you cannot reach the app. Immediate, and not
  reversible.
- **Take it elsewhere.** Ask and we will send what we hold in a structured,
  commonly used machine-readable format. The export above already is one.
- **Complain.** Write to us first. If you are not satisfied, go to the privacy
  regulator where you live:
  - in Canada, the Office of the Privacy Commissioner of Canada, and in Québec
    the Commission d'accès à l'information du Québec;
  - in New Zealand, the Office of the Privacy Commissioner;
  - in Singapore, the Personal Data Protection Commission;
  - in Japan, the Personal Information Protection Commission;
  - in the United States, your state attorney general.

To ask for any of this, write to pykapp+privacy@proton.me from the address on
your account. If your account has no address, write from any address and give
your handle, and we will ask you for something only the account's owner could
know. We do not charge for any of it, we will not make you justify asking, and
we answer as soon as we can and within four weeks at the latest.

## If something goes wrong

If personal information we hold is lost or reaches somebody it should not, we
will tell the regulators that have to be told, within the time each of them
allows. If there is a real risk of serious harm to you, we will tell you too,
promptly and in plain words: what happened, what it reached, and what you can
do. We will keep a record of such incidents whether or not they reach that
bar, because Québec's Law 25 requires one and because an
incident nobody wrote down is one nobody learns from.

What we cannot do is tell you that your photographs were read, because they
cannot be: what an attacker who took everything we have would hold is
ciphertext, keys locked so that they cannot be used, and the metadata this page
lists.

## Who else sees anything

Nobody, unless you share it with them. Only people you have both agreed to
connect with can see what you post, and only the people you address a post
to receive it. The exception is an album: what you put in one is seen by
everybody in it, including people you are not connected to, and the album
lists who they are. There is no public profile, no search by name, no
suggestions, and no way for a stranger to find you unless they already know
your exact handle or email address. Somebody who knows one can ask to connect,
unless you have limited requests to people with a mutual in common, and sees
nothing of yours until you accept.

What you share with someone, they can keep. The app does not stop screenshots
and cannot recall a photo from a phone that has already downloaded it, any
more than any other way of sending a photo can.

## What we do not do

- We do not sell, rent or share your data with anybody.
- We do not show advertising and do not build profiles for it.
- We do not scan content, because we cannot see it.
- We do not send you engagement notifications: there is no "you haven't
  posted in a while", no digest, no streak.
- We do not collect analytics about what you look at, and the app contains
  no crash-reporting or analytics library. If your phone is set to share
  usage and diagnostics with Google or Apple, they tell us that the app
  crashed and where in our code; that report is theirs and contains none of
  your content.
- Your phone tells us how many photographs, captions, comments and album
  names it could or could not open since it last told us, and which version
  of the app and of Android or iOS it runs. Never which ones, and never whose. This
  is how we find out that something is broken before you would think to
  write to us, and it is on for everybody because it carries nothing that
  could be turned off.

## Third parties we use

- **Hosting** for our servers, our database and the second copy of the
  encrypted files. The provider runs the machines and does not use what is on
  them.
- **Object storage** for the encrypted files. The provider holds ciphertext
  and never a key.
- **Push notifications**, through Google's Firebase Cloud Messaging on
  Android and Apple's Push Notification service on iPhone, when you allow
  them. A push carries a type and nothing else: no names, no captions, no
  post identifiers; the words you see are written by your phone.
- **Email**, to send one-time sign-in codes and album invitations. The
  provider sees the address and the message, and nothing else about you.

Each of them is a company based in the United States. Each receives only what
its part of the service needs, and uses it only to provide that part to us.
Using the app means your information goes to them and to the United States,
and this page is where we tell you so before you sign up.

## If the company is sold

If somebody else comes to own people you know llc, or the service is sold or
merged into another company, bankruptcy included, what we hold goes with the
service to whoever runs it next, and this page goes with it unchanged.

- The new owner can read no more than we can. What passes is what this page
  already lists: encrypted files and locked keys we cannot open, and the
  metadata. There is no key here that we can use, and so none that a buyer can
  use either.
- The new owner takes on every promise on this page, in our place. It may use
  what we hold only to run this service, for the purposes listed above, and
  every line under *What we do not do* binds it as it binds us. It can change
  this page only as *Changes* below allows.
- What we hold is never sold apart from the service, and never to anybody who
  will not take this page on. If nobody will take the service over on those
  terms, we close it the way the [terms](/terms/) describe, with 30 days'
  notice and time to export, and then delete what we hold.
- A company that is only thinking of buying us may be told how the service
  works and how many people use it, and nothing about any one of you.
- We will tell you in the app before it happens. You can export your data and
  delete your account before then if you would rather not go with it.

## Deleting your account

*settings → delete my account*. Deleting is immediate and it is not
reversible. If you no longer have the app, [this page](/delete-account/) is how
to ask without it:

- every key that let anybody open your posts is destroyed at once, and so are
  the keys that let you open theirs;
- your posts, comments and reactions are gone for everyone straight away;
- your connections are severed and your groups are removed;
- albums you made are closed, and the people in them keep what they already
  had from each other;
- every phone you were signed in on is signed out;
- your handle and any email address are freed, and any key made from a
  password is deleted.

Eight days later the encrypted files are removed from storage. Those eight
days are not an undo: the keys were destroyed at the tap and nothing in the
product can restore them. A deleted row can outlive the tap in a backup of our
database or in the output of something we ran by hand, for the 35 and 90 days
those are kept. The second copy of the encrypted files keeps each file for 30
days after it leaves storage, so the last of them is gone within six weeks of
the tap. Signing in during that time with the same address starts a new, empty
account.

What we keep afterwards is kept under an identifier that no longer carries your
name, handle, address or key: that the account existed, when it was made, when
it confirmed its age and when it was deleted; blocks you placed or that were
placed against you; reports you filed or that were filed about you, and bug
reports you sent; the country written for your account; the add requests you sent and received, marked cancelled;
when you signed in on each phone and last used it; and the rows of your posts
and comments, marked deleted, which still say when each was made and, for a
post, who it was addressed to. A deleted comment's sealed text stays in its row
until the post it was on is removed, and we serve it to nobody. Entries about
what you did in other people's activity lists go within 128 days.

One exception. When we delete an account because it was engaged in child
sexual abuse or exploitation, we first set aside its email address, phone
number and handle, when it joined and confirmed its age, each phone it used
with that phone's push token, when it signed in, who it was connected to, and
when it posted and to whom. We keep that for the report we make to the
National Center for Missing & Exploited Children, for a year from the report,
as United States law requires, and then delete it. The [child safety
standards](/child-safety/) say more.

## Exporting your data

*settings → export my data* writes a folder to your phone containing your
posts at full size, your captions, the comments on your posts, and the
handles of the people you were connected to. It is decrypted on your phone,
because we could not produce it: we hold nothing readable to give you.

If you no longer have the phone, write to pykapp+privacy@proton.me from the
address on your account, or with your handle if it has no address, and we will
send what we hold within four weeks: your account record, the handles of your
connections, and the encrypted files and the locked keys if you want them. We
cannot send readable photographs, because we cannot read them.

## Children

You must be 18 or older to use *people you know*. We ask for your date of
birth once, at signup, compare it, and keep only the fact that you passed.

## Changes

If this policy changes, the date at the top of this page changes with it. If
a change means we keep more about you, keep it longer, or use it for something
new, we will also tell you in the app before it takes effect. A change never
lets anybody use what we already hold in a way this page did not allow when we
collected it, unless you agree to that.

## Contact

pykapp+privacy@proton.me
