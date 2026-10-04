# Beta changelog

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
