# Home Padel Lab — private beta

Mixed-reality padel physics prototype for Meta Quest 3. This repository is for invited beta testers: installation guides, APK releases and feedback. It does **not** contain the Unity source or the original purchased racket/ball assets.

## Download and install

1. Open [Releases](../../releases) while signed in with an invited GitHub account.
2. Download the latest English **Friend Package ZIP**, then extract it on your computer. It contains the APK and `START-HERE-English.md`. Alternatively download the APK on its own.
3. Follow [the installation and controls guide](START-HERE-English.md). Your friend does not need Unity. Quest developer mode and an authorized USB connection are needed for the installation method described there.

Current build: **0.0.21**. Switch between the training bot and ball machine in **Training · bot / ball machine**. Choose **Bot difficulty: Easy / Medium / Advanced**: Easy returns slowly near centre; Medium varies sides/depth; Advanced combines wider, short/deep targets and quicker bounded bot movement. Difficulty saves independently; **Bot pace fine-tune** retains the 0.80–1.15 adjustment. See [difficulty and natural-movement instructions](Bot-Difficulty-0.0.21-English.md) and [training/hand-ball controls](Training-and-HandBall-0.0.21-English.md). The bot uses real simulated bounces and can miss; controlled neutral-spin returns, not full physical opponent swings. The existing ball-fit menu and trigger drop/toss are retained. Default **Wall bounce = 0.55**, **Racket power = 0.45**, fast-swing response, contact guard and saved grip/hand/court/report data are unchanged. URP fixed-foveation rendering requests 72 Hz; physical feel and sustained refresh still need testing. Clean non-development, offline APK; no multiplayer.

Once invited, accept the GitHub invitation and sign in with that SAME account. Open Releases and download **HomePadel-0.0.21-Friend-Package.zip** under **Assets**, not the automatically generated Source code ZIP. Extract it and follow the English guide to install the APK on your Quest using an authorized computer. GitHub access does not install the app automatically and this is not a Meta Store release. For updates, download the new version from Releases and install over the existing app; do not uninstall first. Check **Menu > Bounce & feel > Wall bounce** after updating; use 0.55 for the current baseline. Activate both controllers when prompted.

The 0.0.18 fix passed reproduced overlapping/overtaking contact tests, including a genuine second hit within 1 ms after separation. This is not proof that all contacts or real-world feel are correct. Please report missed/repeated hits with build/settings and optional local reports. Grip alignment is mathematically checked, not physically certified; your saved fit has not been reset.

## What to test

Keep your Quest boundary active, use wrist straps and clear your arm/controller reach. Start with Easy in one place. Medium/Advanced intentionally encourage natural steps, but only inside your cleared real area and boundary. Leave escaped/out-of-area balls and reset with the free-hand face button. The virtual court does not measure your room or detect furniture.

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
