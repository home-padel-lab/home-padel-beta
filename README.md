# Home Padel Lab — private beta

Mixed-reality padel physics prototype for Meta Quest 3. This repository is for invited beta testers: installation guides, APK releases and feedback. It does **not** contain the Unity source or the original purchased racket/ball assets.

## Download and install

1. Open [Releases](../../releases) while signed in with an invited GitHub account.
2. Download the latest English **Friend Package ZIP**, then extract it on your computer. Build 0.0.23 contains the APK, `Court-Profiles-0.0.23-English.txt` and build audit. Alternatively download the APK on its own.
3. Follow [the installation and controls guide](START-HERE-English.md). Your friend does not need Unity. Quest developer mode and an authorized USB connection are needed for the installation method described there.

Current build: **0.0.23**. Choose **Court & physics > Court size** for Compact / Medium / Large singles and a derived doubles layout. Dimensions (width × length): singles 2.4×6, 3×7, 5×10 m; doubles 4.8×9.6, 6×12, 10×20 m. Existing sizes, including 2.4×6.5 m, stay as Custom. Doubles is a layout only, NOT multiplayer. See [the court profiles guide](Court-Profiles-0.0.23-English.txt). The four-category, scrolling menu from [0.0.22](Menu-Guide-0.0.22-English.txt) remains; the new Court size and HP2 sharing screens supersede that guide's corresponding sections.

Bot difficulty **Easy / Medium / Advanced**, pace, 15 drills, hand release and saved grip/feel/reports remain. Default **Wall bounce = 0.55**, **Racket power = 0.45**. Player swing response, gravity, drag, spin and bounce/friction are not scaled by court size. Machine and bot trajectories are replanned on courts longer than 8 m, including faster launches where needed. Net 0.78 m, side glass 1.40 m, back glass 2.00 m retained. URP fixed foveation requests 72 Hz; sustained refresh and physical feel still need headset testing. Clean offline release; no multiplayer, second bot or furniture scan. New HP2 codes include the singles base and doubles flag; HP1 imports still work, but older apps cannot import HP2. Ball fit and bot level remain outside setup codes.

Once invited, accept the GitHub invitation and sign in with that SAME account. Open Releases and download **HomePadel-0.0.23-Friend-Package.zip** under **Assets**, not the automatically generated Source code ZIP. Extract it and follow the installation guide using an authorized computer. GitHub access does not install the app automatically; this is not a Meta Store release. Update over the existing app without uninstalling. Check **Menu > Court & physics > Bounce & racket power > Wall bounce**; 0.55 is the baseline. Activate both controllers when prompted.

The 0.0.18 fix passed reproduced overlapping/overtaking contact tests, including a genuine second hit within 1 ms after separation. This is not proof that all contacts or real-world feel are correct. Please report missed/repeated hits with build/settings and optional local reports. Grip alignment is mathematically checked, not physically certified; your saved fit has not been reset.

## What to test

Keep your Quest boundary active, use wrist straps and clear your arm/controller reach. Start with Easy in one place. Medium/Advanced intentionally encourage natural steps, but only inside your cleared real area and boundary. Leave escaped/out-of-area balls and reset with the free-hand face button. The virtual court does not measure your room or detect furniture.

Start with **Equipment fit > Racket fit**, then **Play & training > Ball machine > Slow straight shot > Launch one ball**. Compare one setting at a time using the same drill and court size. Focus on finding functions, understanding adjustments, grip alignment, floor/glass bounce and missed racket contacts.

Use [New issue](../../issues/new/choose) to report a problem or share a good setup. Include:

- Build version and headset model.
- Racket hand, drill and court dimensions.
- What happened, what you expected, and how to reproduce it.
- A screenshot showing both lines of the `HP2-...` setup code when relevant (legacy HP1 also readable in this version).
- Optionally, an exported calibration report; see [TESTING.md](TESTING.md).

## Privacy and access

The app saves measurements locally by default; nothing is uploaded automatically. Exporting a report creates a local file, not a GitHub submission. Only share a report if you are comfortable with invited repository members seeing it. Do not upload account details, USB/device serials, private room photos or unedited Android logs.

This repository is intended to remain **private**. Private access does not prevent an invited person from keeping or redistributing downloaded files. Keep original purchased assets, credentials, signing keys and Unity source out of this beta repository.

This private beta repository belongs to **home-padel-lab**. Testers should be invited with **Read** access so they can download releases and report issues without changing repository files. No tester invitations are automatic. Only the owner is currently a member of the organization.
