# Beta changelog

## 0.0.29

- Wall-only trial: 0.55 to 0.75. Other ball coefficients unchanged from 0.0.28; untouched old defaults migrate once while custom values and previous keys remain. Restore just Wall bounce to 0.55 for comparison.
- Includes local 0.0.24–28 work not previously published: simplified rim/edge/throat/handle contacts, floor sliding/rolling, Full size fixed 10×20 m footprint, impact/glass/net/rolling/UI sounds. No racket swing/whoosh sound.
- Room-anchored options menu; paused joystick court placement with fine adjustment, accept/cancel and two-press reset. Room pose stays local, outside setup codes. No furniture scan or boundary replacement.
- Glass machine drills replan their launch if stronger rebound makes the initial trajectory invalid; live ball coefficients are never changed by the planner.
- 4,511 checks passed (2,462 pure + 2,049 unique Unity). Clean ARM64 URP APK, same signer. Installed on owner's Quest 3 without uninstalling; previous reports retained. Startup migration confirmation awaits reconnection/controller activation. Headset feel, comfort, sustained refresh and Quest 3S remain unverified. No multiplayer.
- Reports remain local. This private repository receives only beta deliverables and guides, not purchased source assets, Unity source or personal session reports.

## 0.0.23

- Three singles presets and derived doubles layouts in Court & physics > Court size. Width × length: Compact 2.4×6 / 4.8×9.6 m; Medium 3×7 / 6×12 m; Large 5×10 / 10×20 m. Doubles width is twice the base singles width; doubles length is twice its new width. Singles custom length survives switching back.
- Seven-row scrolling screen includes preset, format, read-only playing dimensions, custom base width/length, two-X reset and Save and play. Existing dimensions, including 2.4×6.5 m, preserved as Custom; new installs start Compact singles.
- HP2 codes/JSON encode the singles base, preset/custom and doubles flag. HP1/old JSON still import; older apps cannot read HP2. Racket-only scope preserves recipient court/feel. Ball fit and bot level remain excluded.
- Geometry, visible panels and collision planes share the layout. Net 0.78 m, side/back glass 1.40/2.00 m retained. Player swing curve, gravity, drag, spin, restitutions/friction and personal fit retained; no global court speed multiplier.
- Machine/bot trajectories are replanned on layouts longer than 8 m, including faster machine launches where needed. Original short-court planning remains. Doubles is geometry only: no multiplayer, second bot or scoring. Virtual size is not a safe-room measurement.
- 1,234 pure + 1,228 unique Unity checks passed (2,462 total), including 90 machine plans across six layouts and all three bot levels, migration, HP1/HP2 and menus. Eighteen menu previews rendered; five changed screens inspected. APK version 23 / 0.0.23, compatible signature and clean release audit verified. Physical feel, sustained refresh and Quest 3S still need testing.
- Download the Friend ZIP for APK + [English court guide](Court-Profiles-0.0.23-English.txt) + immutable build-time audit (before installation/publication). Update without uninstalling. Reports remain local; no automatic uploads.

## 0.0.22

- Four menu categories: Play & training, Equipment fit, Court & physics, Reports & sharing. Separate bot/machine/free-practice entries and controller help.
- Five-row scrolling lists keep growing menus readable. Y returns to the actual previous screen and restores its selected row. Context help and the footer explain the selected control/action.
- Separate basic bounce/power and advanced friction/spin. Complete restores and setup imports require two X presses; Y or changing the row cancels. Numeric X restores only that value, as labelled. Racket-hand X now toggles hands.
- HP1 sharing labels explain the actual scope; ball placement and bot difficulty are not included in that legacy code.
- Physics, wall 0.55 / racket power 0.45, geometry, bot levels, hand release, saved calibration and reports unchanged. No global speed scaling or new racket/court profile.
- 1,093 pure + 1,153 unique Unity checks passed (2,246 total), including 48 menu-usability checks. Fifteen menu previews inspected. APK version 22 / 0.0.22, signature and clean release components audited. Actual on-headset readability, feel and sustained refresh require testing; Quest 3S unverified.
- Download the Friend Package ZIP for APK + current English menu/install guide + audit. The audit is an immutable build-time snapshot before installation/publication. Update without uninstalling.

## 0.0.21

- Easy / Medium / Advanced bot difficulty. Easy gives slower near-centre returns (legacy saved ±18 cm placement retained); Medium varies sides/depth; Advanced combines wider short/deep targets and receiving heights. Eight repeatable targets in Medium/Advanced, not random match tactics.
- Bounded bot movement and prediction frequency increase with level; pace fine-tune remains 0.80–1.15. Difficulty saves separately; upgrades without that preference start Easy. No automatic first serve; bot/machine remain mutually exclusive.
- Natural steps are intended within a cleared physical area and active Quest boundary. Targets are limited by virtual court dimensions, not scanned safe room space; no furniture detection or tracked-head target following.
- Player racket, wall/floor bounce, hand release, fit and previous local data unchanged. Reports add `botDifficulty`; HP1 does not contain bot level or ball placement. No automatic uploads, scoring, complete rules or multiplayer.
- 1,093 pure plus 1,106 unique Unity checks passed (2,199 total), including 216 complete patterned returns over three levels and nine court sizes, pace, finite movement, menu and persistence checks. APK version 21 / 0.0.21 and same signing certificate audited. Installed as an update on the owner's Quest 3; physical feel and sustained refresh still require headset testing. Quest 3S untested.
- [Difficulty guide](Bot-Difficulty-0.0.21-English.md). The ZIP audit is a build-time snapshot from before installation/publication. Update without uninstalling.

## 0.0.20

- Simple blue/cyan training bot and explicit bot/machine selector. Start selected mode closes the menu ready, without automatically firing a ball. The modes are mutually exclusive; opening Menu stops both.
- Bot prediction uses the same simulated court bounces, drag and spin, with finite movement speed. It can recover some own/opponent back-glass shots and can miss. Returns are controlled neutral-spin practice shots near the fixed virtual starting area, not full physical opponent swings or a tracked safe location.
- Dedicated ball-in-hand fit menu with live preview and controller-local coloured position arrows. Placement saves separately per free hand; racket fit and physics are not reset. Default ball placement is a starting fit, not universal anatomy.
- Index-trigger pickup/release hysteresis and neutral rearm. Hand release uses explicit grip pose and tracked contact-point velocity when valid, otherwise recent filtered pose history; no preset boost. Tracking jumps/gaps reset the history. Reports add hand-release placement, velocity source and trigger state; nothing uploads automatically.
- Retains wall 0.55, racket power 0.45, fast-swing curve, repeated-contact guard and existing saved settings/reports. HP1 codes do not contain ball placement or bot settings: send their screenshots separately.
- 428 pure checks plus 1,093 unique Unity checks passed (1,521 total). Version 20 / 0.0.20 and same signing certificate audited. Installed as an update on the owner's Quest 3; launching awaits both controllers. Automated checks and installation do not verify physical feel or sustained refresh. Quest 3S untested; no scoring, full rules or multiplayer.
- See [training and hand-ball instructions](Training-and-HandBall-0.0.20-English.md). Update without uninstalling. The audit inside the Friend ZIP is a build-time snapshot, before installation/publication.

## 0.0.18

- Machine OFF: hold the free-hand index trigger to pick up a ball, release to drop/toss. Default LEFT with right racket; mirrored for left-handed play. No preset throw boost or aiming assistance; menu, tracking loss and app pause cancel without firing. Automatic feeding, pending machine launches and fixed calibration block pickup; neutral trigger is required after returning.
- Corrects a reproduced racket-contact episode that produced up to twelve events, most with zero impulse, and exhausted the physics step. Rearms after geometric separation with 1 mm hysteresis, not an arbitrary cooldown. Zero-impulse contacts are diagnostic only, not hits/haptics.
- Hand releases start local measured trials when auto-save is ON. Reports add `racketContactHeld` to samples and `zeroImpulseRacketContacts` to samples/ball summaries. No automatic uploads.
- Grip pose/anchor/mesh alignment reviewed; existing calibration is retained. Physical controller fit still requires headset testing. Wall 0.55, racket power 0.45, progressive speed curve, court, rendering and previous local reports retained.
- 319 pure checks and 1,043 Unity build checks passed (1,362 total). APK version 18 / 0.0.18, signature, permissions and packaged components audited; same signing certificate as 0.0.17. Installed as an update on the owner's Quest; opening awaits activation of both controllers. Installation is not verification of on-headset feel/rendering or stable refresh. No multiplayer; Quest 3S untested.

## 0.0.17

- Migrates to URP Forward, Vulkan single-pass stereo and medium fixed foveation; requests 72 Hz. No postprocessing, camera depth/opaque buffers or shadow maps.
- Low-cost transparent glass matches the existing court dimensions/open doors. Procedural ball shadow supplies a floor-depth cue; no room scan or realtime reflections.
- Non-development tester APK excludes developer agents, Immersive Debugger, Operator/Metrics libraries and unused eye-tracking/capture/microphone/network permissions. Essential Meta runtime and passthrough feature remain.
- Physics, fast-swing response, default wall 0.55 / power 0.45, saved grip/hand, court, menu controls, haptics and physics reports unchanged.
- Local performance CSVs provide five-second app-timing windows; optional unsupported counters remain empty. Nothing is recorded from the camera/mic or uploaded automatically.
- 250 pure checks and 1,022 Unity build checks passed, plus five glass/transparency editor checks. Final APK version, signature, permissions and packaged components audited. Same signing certificate as 0.0.16; installed as an update on the owner's Quest. Active headset rendering and sustained refresh still need testing; installation is not visual verification.
- Known repeated racket-contact issue remains. No multiplayer. Quest 3S is a development target, not yet tested; this is a private sideload beta, not a certified Meta Store release.

## 0.0.16

- Default wall response 0.55 for more return towards the opposite half. Previous saved 0.45 defaults adopt 0.55 once; other custom responses and original preferences are preserved.
- Racket power remains 0.45 by default. Soft advancing contact-point motion up to 3 m/s is unchanged; above this, experimental response uses `3 + 2 * ln(1 + (speed - 3) / 2)`. Continuous progressive response in all directions, no hard ball-speed cutoff. Raw tracking, sweep geometry and incoming ball motion are not scaled.
- Saved power, racket fit, hand, court, floor response, gravity, haptics, joystick controls and reports retained. Racket spin can vary with the smaller contact impulse on compressed hits.
- Reports include raw and response contact velocities plus the curve parameters. HP1 codes do not encode the curve: compare on the same build.
- The first published 0.0.16 package includes wall 0.55. The earlier local-only 0.0.16 candidate had wall 0.45 as its default and was not released on GitHub.
- Known issue: repeated racket contacts can inflate reported hit counts. This release does not fix it; counts are not actual stroke counts.
- APK build, signature and version 16 / 0.0.16 verified. Passed 250 pure physics/drill checks and 982 Unity checks: 1,232 in total, including wall-default migration and preservation of custom values. Automated checks do not certify real-world feel or resolve the known contact issue.
- Experimental beta; no multiplayer, automatic uploads or certification of real-world physics.

## 0.0.15

- Wall response 0.45: a little more return than the previous 0.30 saved setting / 0.35 default.
- Racket response 0.45 instead of 0.65: moving-racket shots are softer, without a ball-speed cap or swing-speed clamp.
- These two values deliberately adopt the new profile on the first upgrade, using separate preferences so the earlier values remain intact. Later adjustments are saved normally.
- Racket fit, hand, court, floor response, friction/spin, menu controls, haptics and local reports retained. No multiplayer or automatic uploads.
- Regression checks cover slow/fast swings, the fifteen drills, old/new preferences, persistence, invalid settings and preservation of personal grip/floor values.
- APK build, signature, version and 1,136 automated checks verified. Installed as an update on the owner's Quest; real-world feel still needs play testing.

## 0.0.14

- Default court extended slightly from 6.00 to 6.50 m; width remains 2.40 m.
- Net lowered from 0.88 to 0.78 m; back walls and end/doorway sections 2.00 m, middle side walls 1.40 m.
- Door openings 0.80 m wide / 1.75 m high. Visible borders and collisions share the profile: no invisible tall glass or blocked doorway.
- Softer default glass response: 0.35 instead of 0.50. Glass drills re-aimed to contact the visible walls.
- Untouched previous defaults migrate once; custom length/rebound, personal grip and saved reports are retained. Floor response, gravity, haptics and joystick controls are unchanged.
- HP1 remains readable; compare on the same build because the derived wall/net profile has changed.
- APK build/signature and 1,091 automated checks verified. Headset installation is not verification of real-world physics accuracy.
- Experimental compact proportions inspired by the supplied Racket Club image and padel wall layout; not measured Racket Club or regulation padel dimensions.

## 0.0.13

- Joystick menu changes require a firm directional push: 75% activation and 35% release threshold.
- Return to centre between pushes for one step. Holding repeats after 0.65 seconds, then every 0.35 seconds.
- Ambiguous diagonals are ignored; X/Y actions take priority over stick changes.
- Stronger racket-controller impact vibration, scaled with impact speed. Actual headset feel still needs beta testing.
- Existing grip/physics settings and automatic local reports are retained.
- APK build, signature and 614 automated checks verified. This is not a claim of on-headset validation.

## 0.0.12

- Automatic local recording of launches, setups, trajectories and contacts.
- Five fixed virtual calibration tests, feedback ratings and report export.
- No automatic uploads or automatic physics tuning.

## 0.0.11

- Purchased padel-ball model integrated, with 67 mm diameter and simulated visible spin.
