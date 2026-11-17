# Voice profile

A voice profile lets every draft sound like the user without re-reading their mail each time. Andock
stores no profile on the server, so keep it where this assistant can find it again: project memory,
or a file the user keeps (suggest `voice-profile.md`). Say where you saved it.

## Build it

1. Ask first: the profile is built from the user's own sent mail.
2. Take 20 to 50 mails from the sent folder (`search_emails` with `folder: "sent"`, `limit: 100`,
   across several months), spread over different recipients: customers, offices, friends, colleagues.
   Skip one-word replies, forwards and automated mail. With fewer than 5 usable mails, say the
   profile will be rough.
3. Leave out 3 threads where the user answered someone. Build the profile from the rest.
4. Write down only what you saw, with how often you saw it ("'Liebe Grüsse' in 14 of 20"):

```
Voice profile, <user>, built <date> from <n> sent mails, checked on 3 threads
Greeting:   <exact forms, and to whom>        e.g. "Hoi <Vorname>" to friends, "Guten Tag Frau <Name>" to offices
Sign-off:   <exact forms, name as written>
Formality:  du/Sie by person or group
Length:     typical sentences per mail; where the request lands
Habits:     phrases the user really uses, verbatim
Never:      phrases never seen ("I hope this finds you well", "circle back", exclamation marks)
Signature:  added by the mail program or typed? Drafts add none if the program does it.
Corrections: <date>: <what the user changed, and why>
```

5. Check it: for each held-out thread, draft the reply from the profile alone and compare it with
   what the user really sent. Fix the profile where they differ, usually a missing rule about
   greeting, length or du/Sie by audience.
6. Show the profile and ask what feels wrong; the user's answer wins over what you counted.

## Keep it current

When the user edits a draft, compare their version with yours and name the change in one line
("you cut the thank-you; leave it out next time?"). If they agree, add it under Corrections. A
correction made once should not be needed twice.

## Use it

The profile sets greeting, sign-off, length and formality. The thread still decides language and
content, and a person's own history beats the general profile (someone the user always calls by first
name stays on first-name terms).
