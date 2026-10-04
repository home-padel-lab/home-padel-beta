# Home Padel Lab — private beta

Mixed-reality padel physics prototype for Meta Quest 3. This repository is for invited beta testers: installation guides, APK releases and feedback. It does **not** contain the Unity source or the original purchased racket/ball assets.

## Download and install

1. Open [Releases](../../releases) while signed in with an invited GitHub account.
2. Download the latest English **Friend Package ZIP**, then extract it on your computer. It contains the APK and `START-HERE-English.md`. Alternatively download the APK on its own.
3. Follow [the installation and controls guide](START-HERE-English.md). Your friend does not need Unity. Quest developer mode and an authorized USB connection are needed for the installation method described there.

Current build: **0.0.17**. URP rendering with fixed foveation, inexpensive transparent glass and a simple ball shadow. Requests 72 Hz; sustained performance and passthrough visuals still need active headset testing. Clean non-development APK excludes developer agents/debugger and unused eye/capture/microphone/network permissions. Physics is unchanged from the published 0.0.16: default **Wall bounce = 0.55**, **Racket power = 0.45**, with the same progressive fast-swing response. Saved grip, hand, court, bounce settings and reports are retained. The app is offline; there is no multiplayer yet.

Once invited, accept the GitHub invitation and sign in with that SAME account. Open Releases and download **HomePadel-0.0.17-Friend-Package.zip** under **Assets**, not the automatically generated Source code ZIP. Extract it and follow the English guide to install the APK on your Quest using an authorized computer. GitHub access does not install the app automatically and this is not a Meta Store release. For updates, download the new version from Releases and install over the existing app; do not uninstall first. Check **Menu > Bounce & feel > Wall bounce** after updating; use 0.55 for the current baseline.

Known issue under investigation: some strokes produce repeated racket contacts within fractions of a millisecond. Reported contact counts must not be interpreted as your actual number of strokes. This release does not fix that issue; report the feel and include the build/settings with optional local reports.

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

This private beta repository belongs to **home-padel-lab**. Testers should be invited with **Read** access so they can download releases and report issues without changing repository files. No tester invitations are automatic. Only the owner is currently a member of the organization.
