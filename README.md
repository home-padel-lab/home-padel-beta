# Home Padel Lab — private beta

Mixed-reality padel physics prototype for Meta Quest 3. This repository is for invited beta testers: installation guides, APK releases and feedback. It does **not** contain the Unity source or the original purchased racket/ball assets.

## Download and install

1. Open [Releases](../../releases) while signed in with an invited GitHub account.
2. Download the latest English **Friend Package ZIP**, then extract it on your computer. Build 0.0.22 contains the APK, `Menu-Guide-0.0.22-English.txt` and build audit. Alternatively download the APK on its own.
3. Follow [the installation and controls guide](START-HERE-English.md). Your friend does not need Unity. Quest developer mode and an authorized USB connection are needed for the installation method described there.

Current build: **0.0.22**. Four menu sections: **Play & training**, **Equipment fit**, **Court & physics**, **Reports & sharing**. Play separates bot, machine and free practice; Equipment has independent racket/ball fit; physics separates the three basic controls from advanced friction/spin. Longer screens show five rows at a time. Y returns to the previous screen, preserving its selection; the footer explains the selected X action. Whole-setup restores/imports require a second X confirmation. See [the current menu and controls guide](Menu-Guide-0.0.22-English.txt).

Bot difficulty **Easy / Medium / Advanced**, pace adjustment, the 15 drills, hand release, collision solver and saved grip/court/reports remain unchanged. Default **Wall bounce = 0.55**, **Racket power = 0.45**. No new automatic speed scaling, court geometry or racket dimensions. URP fixed-foveation rendering requests 72 Hz; physical feel, on-headset readability and sustained refresh still need testing. Clean non-development, offline APK; no multiplayer. Older versioned guides are historical and their menu paths may differ.

Once invited, accept the GitHub invitation and sign in with that SAME account. Open Releases and download **HomePadel-0.0.22-Friend-Package.zip** under **Assets**, not the automatically generated Source code ZIP. Extract it and follow the English guide to install the APK on your Quest using an authorized computer. GitHub access does not install the app automatically and this is not a Meta Store release. For updates, install over the existing app; do not uninstall first. Check **Menu > Court & physics > Bounce & racket power > Wall bounce** after updating; use 0.55 for the current baseline. Activate both controllers when prompted.

The 0.0.18 fix passed reproduced overlapping/overtaking contact tests, including a genuine second hit within 1 ms after separation. This is not proof that all contacts or real-world feel are correct. Please report missed/repeated hits with build/settings and optional local reports. Grip alignment is mathematically checked, not physically certified; your saved fit has not been reset.

## What to test

Keep your Quest boundary active, use wrist straps and clear your arm/controller reach. Start with Easy in one place. Medium/Advanced intentionally encourage natural steps, but only inside your cleared real area and boundary. Leave escaped/out-of-area balls and reset with the free-hand face button. The virtual court does not measure your room or detect furniture.

Start with **Equipment fit > Racket fit**, then **Play & training > Ball machine > Slow straight shot > Launch one ball**. Compare one setting at a time using the same drill and court size. Focus on finding functions, understanding adjustments, grip alignment, floor/glass bounce and missed racket contacts.

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
