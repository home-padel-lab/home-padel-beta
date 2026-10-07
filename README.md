# Home Padel Lab — private beta

## Current beta: 0.0.42

[Download version 0.0.42](https://github.com/home-padel-lab/home-padel-beta/releases/tag/v0.0.42). Under Assets, choose **HomePadel-0.0.42-Friend-Package.zip** for the APK and current English instructions, or the APK directly. Do not download Source code to install the game. Sign in with your invited account; this repository remains private.

Update without uninstalling or clearing data, and wake both controllers. This version includes bot matches, scoreboards, umpire, serve-floor guidance and experimental Arcade/NearReal profiles. Bot02/03/04 skin assets are included, but **Bot01 remains active; no skin selector or three-bot doubles gameplay yet**. Read the attached **START-HERE-0.0.42-English.txt** rather than old controls below. Sustained 72 Hz and real padel feel still require headset testing.

## Archived 0.0.29 documentation

The following version-specific details and controls describe the older 0.0.29 beta, not the current release.

Mixed-reality padel physics prototype for Meta Quest 3. This repository is for invited beta testers: installation guides, APK releases and feedback. It does **not** contain the Unity source or the original purchased racket/ball assets.

## Download and install

1. Open [Releases](../../releases) while signed in with an invited GitHub account.
2. Download **HomePadel-0.0.29-Friend-Package.zip** from [version 0.0.29](../../releases/tag/v0.0.29), then extract it on your computer. It contains the APK, English installation/placement/wall-trial guides and audit. Alternatively download the APK on its own. Do not download Source code.
3. Follow [the installation and controls guide](START-HERE-English.md). Your friend does not need Unity. Quest developer mode and an authorized USB connection are needed for the installation method described there.

Current build: **0.0.29**. Wall bounce is now **0.75** instead of 0.55, with racket power, floor bounce, compression, drag and spin unchanged from 0.0.28. An untouched older 0.55 upgrades once; custom wall settings remain unchanged. To compare or restore 0.55, use **LEFT Menu > Court & physics > Bounce & racket power > Wall bounce**. This is an experimental comparison, not certified realistic physics. See [the wall-trial guide](Wall-Trial-0.0.29-English.txt).

Changes since the previously published 0.0.23 include simplified racket rim/edge/throat/handle contacts, floor rolling improvements, impact/rolling/menu sounds and a fourth **Full size (10 × 20 m)** footprint. Racket swing/whoosh sound has been removed. The options menu stays anchored in your physical room when court size changes. **Court & physics > Place court in your room**: LEFT stick slides, RIGHT stick turns, LEFT trigger is fine adjustment, X accepts and Y cancels. Room placement is local to your headset and does not scan furniture or replace the Quest boundary.

Compact / Medium / Large singles remain 2.4×6, 3×7 and 5×10 m (width × length), with doubles footprints 4.8×9.6, 6×12 and 10×20 m. Full size stays 10×20 m in solo training and doubles; it does not double again. Net/wall heights retain experimental compact heights, so Full size is a footprint, not a complete regulation enclosure. Existing custom dimensions remain. Doubles is geometry only, NOT multiplayer.

Bot difficulty **Easy / Medium / Advanced**, pace, 15 drills, hand release and saved grip/reports remain. Defaults: **Wall bounce = 0.75**, **Racket power = 0.45**, **Floor bounce = 0.72**. Physics is not globally scaled by court size. Machine launches are replanned when necessary, including glass drills at the new wall response. Net 0.78 m, side glass 1.40 m, back glass 2.00 m retained. URP fixed foveation requests 72 Hz; sustained refresh and comfort still require headset testing. Clean offline release; no multiplayer or furniture scan. HP2 preserves base dimensions and format; HP1 imports still work. Ball fit, room placement and bot level remain outside setup codes.

Once invited, accept the GitHub invitation and sign in with that SAME account. Open [version 0.0.29](../../releases/tag/v0.0.29) and download the Friend Package ZIP under **Assets**, not Source code. GitHub access does not install the app automatically; this is not a Meta Store release. Update over the existing app without uninstalling. Wake both controllers when prompted. Stop if dizzy, nauseous or tracking/passthrough fails; this update is not a proven comfort fix.

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
