# Home Padel Lab — private beta

Mixed-reality padel physics prototype for Meta Quest 3. This repository is for invited beta testers: installation guides, APK releases and feedback. It does **not** contain the Unity source or the original purchased racket/ball assets.

## Download and install

1. Open [Releases](../../releases) while signed in with an invited GitHub account.
2. Download the latest English **Friend Package ZIP**, then extract it on your computer. It contains the APK and `START-HERE-English.md`. Alternatively download the APK on its own.
3. Follow [the installation and controls guide](START-HERE-English.md). Your friend does not need Unity. Quest developer mode and an authorized USB connection are needed for the installation method described there.

Current build: **0.0.13**. New in this build: firmer joystick input, slower repeat and stronger racket-impact vibration. The app is offline; there is no multiplayer yet.

## What to test

Keep your Quest boundary active, use wrist straps, clear your arm/controller reach and stand in one place. Do not chase virtual balls. The court does not measure your room or detect furniture.

Start with **Racket fit**, then one **Slow straight shot**. Compare one setting at a time using the same drill and court size. Focus on grip alignment, floor/glass bounce, missed racket contacts, menu control and impact vibration.

Use [New issue](../../issues/new/choose) to report a problem or share a good setup. Include:

- Build version and headset model.
- Racket hand, drill and court dimensions.
- What happened, what you expected, and how to reproduce it.
- A screenshot showing both lines of the `HP1-...` setup code when relevant.
- Optionally, an exported calibration report; see [TESTING.md](TESTING.md).

## Privacy and access

The app saves measurements locally by default; nothing is uploaded automatically. Exporting a report creates a local file, not a GitHub submission. Only share a report if you are comfortable with invited repository members seeing it. Do not upload account details, USB/device serials, private room photos or unedited Android logs.

This repository is intended to remain **private**. Private access does not prevent an invited person from keeping or redistributing downloaded files. Keep original purchased assets, credentials, signing keys and Unity source out of this beta repository.

On a personal GitHub account, invited collaborators have write access, not read-only access. For read-only testers, the owner should use an organization-owned private repository and grant **Read**. No tester invitations are automatic.
