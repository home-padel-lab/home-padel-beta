# Testing and calibration feedback

## Court profiles and sharing (0.0.23)

Follow [the court profiles guide](Court-Profiles-0.0.23-English.txt). In **Court & physics > Court size**, test Compact / Medium / Large in singles and doubles. Check the read-only playing width × length, persistence after restarting, and that switching back restores your base singles size. Existing 2.4×6.5 m should remain Custom on upgrade. Reset to Compact requires two X presses. Doubles is only geometry: no networking, partner, scoring or second bot.

Try the same slow drill and bot Easy with each layout, then other drills/levels only within your cleared room. Training trajectories on layouts over 8 m are replanned and may launch faster; player racket response, gravity, drag, spin, wall 0.55 and floor response are not automatically scaled. Do not infer safety from virtual dimensions. Report build, singles base, format, effective dimensions, level/drill and optional exported report. Reports include the new court profile.

New **HP2** codes include the base singles dimensions, preset/custom flag and doubles format. HP1 and older JSON still import; older apps cannot read HP2. Racket-only imports keep the recipient's court/physics. Ball fit and bot level remain excluded. Screenshot both code lines. Reports remain local and sharing is optional.

## Retained menu navigation (from 0.0.22)

Use [the category menu guide](Menu-Guide-0.0.22-English.txt), with the new Court size and HP2 sections above overriding its legacy sections. Options always use the LEFT controller. Up/down selects, left/right changes a value, X performs the labelled action, Y returns to the previous screen, Menu saves/closes. Push firmly; hold the LEFT trigger for finer fit/feel steps.

Try finding each function without PC help: **Equipment fit > Racket fit**, **Ball in hand**, **Play & training > bot / machine / free practice**, **Court & physics > Bounce & racket power**, **Advanced spin & friction**, and **Reports & sharing**. Verify the selected row remains visible when scrolling, Y returns where expected, single-ball and auto-feed actions are distinct, and opening Menu stops both bot and machine. Complete restores/imports require a second X; Y or changing row cancels. X on a numeric row still restores only that value, as labelled.

Start the bot through Play, choose difficulty, then START; serve with the FREE-hand X/A. Machine has Launch one ball (2-second delay) and Start practice (automatic feeding). Free practice closes with both modes OFF. Keep the Quest boundary on; move only in a cleared safe area.

Record through **Reports & sharing > Recording, tests & feedback**. Share codes through **Reports & sharing > Share or load a setup**. HP2 excludes ball fit and bot difficulty: include screenshots of those separately. Existing local data is retained. Report unclear wording, unexpected button actions or text that is hard to read, together with build/headset and optional local reports. Nothing uploads automatically.

The sections below preserve older-version testing history; prefer current paths above.

## Difficulty and natural movement (0.0.21)

Follow [the difficulty guide](Bot-Difficulty-0.0.21-English.md). Start in Easy, pace 1.00. Select **Start selected mode · no ball**; the free-hand primary face button sends a gentle serve, then hit with your racket. Repeat similar strokes for one minute at each level. Medium/Advanced vary sides and depth to encourage natural steps, only inside a cleared real area and your active boundary. Leave balls outside that area and start a new serve; virtual targets are not safe-room measurements.

Check switching bot/machine, difficulty persistence after reopening the app, relative pace/placement, missed or repeated hits, and comfort. Keep auto-save ON: launch records now identify `botDifficulty`, and bot return counts stay separate from your hits. Share level, pace, court dimensions, headset and voluntary local report. HP1 does not include difficulty or ball fit, so screenshot those menu values separately. Physics, grip and release are unchanged from 0.0.20. See [current training and hand-ball controls](Training-and-HandBall-0.0.21-English.md).

The older sections below describe previous builds. In 0.0.21 the old placement row is replaced by difficulty; use the current controls above.

## Bot, machine and hand release (0.0.20)

Follow [the training and hand-ball guide](Training-and-HandBall-0.0.20-English.md) for the exact controls and five-minute checklist. Start with both modes OFF: fit the ball on the free hand using the live preview, then test five still-hand drops and gentle upward/forward tosses. Return the index trigger fully to neutral before each new pickup. No preset throw boost is applied.

Select BOT in **Training · bot / ball machine**, pace 1.00 and Centre returns. Choose **Start selected mode · no ball** and press X. Close menus and use the free-hand primary face button for a gentle serve, then hit with your racket: the bot returns your subsequent shots, not an untouched serve/drop. Try straight and gentle back-glass shots, then switch to MACHINE and back. Opening Menu stops both; closing alone does not restart training. Never chase the bot or the ball; its target is a fixed virtual area, not a room scan.

Keep auto-save ON. Share build, headset model, racket hand, ball-fit screenshot and voluntary exported report. `hand_release` records include the ball offset and release velocity source. Bot returns are counted separately from player hits. HP1 does not contain ball fit or bot settings. Observe menu usability, release feel, missed/repeated hits and smoothness; automated tests do not certify these on a headset.

## Hand release and contact comparison (0.0.18)

Keep the machine OFF and close Menu. With a right-handed racket, hold the LEFT index trigger to pick up a ball above that controller, then release it above your racket. Drop from a still hand first; then try a gentle toss using hand movement. Squeeze again for the next ball. With a left-handed racket, use the right trigger. Pickup is blocked during auto-feed, a pending machine launch, menus and calibration. If tracking is lost or you open Menu while holding, the ball is cancelled rather than thrown; return the trigger to neutral before trying again.

Try ten small upward taps while standing safely in one place. Compare soft and moderate strokes with the same wall 0.55/power 0.45 and HP1 setup. Report missed/extra hits, unnatural boosts and grip discomfort. Keep auto-save ON: each hand release starts a trial labelled `hand` / `Hand release`. The contact guard is geometric rather than a fixed cooldown. Optional report fields `racketContactHeld` and `zeroImpulseRacketContacts` help inspect overlap/zero-impulse episodes; do not assume all measured contacts are actual strokes.

## Rendering comparison (0.0.17)

Wear the headset for 2–3 minutes on the same drill/settings as 0.0.16. Check passthrough remains visible, both eyes agree, glass is unobtrusive and paddle/menus render correctly. Stop if passthrough or tracking fails; do not chase balls. Requested 72 Hz is not proof of stable performance.

Local performance CSV files are stored under `reports/performance` in the app's files. Use the authorized-PC retrieval instructions in [START-HERE-English.md](START-HERE-English.md). Share a CSV voluntarily with headset model, build and drill used. Empty counters mean unsupported measurements, not zero cost. No automatic uploads or camera/audio recordings. App timing is not compositor certification.

## Quick comparison

1. Use a safe, cleared standing area. Do not move around chasing the ball.
2. Note the build number, racket hand, court size and selected drill.
3. Keep **Calibration & reports > Auto-save game data** ON if you want measurements.
4. Launch the same drill several times. Change only one setting and compare again.
5. Open **Share setup** and screenshot both lines of the HP1 code. Choose **Racket only** for grip feedback or **Physics + court + machine** for bounce feedback.
6. Describe the result in a GitHub issue. A good personal grip is not necessarily suitable for another player.

## Fixed calibration tests

Choose **Calibration & reports > Run calibration**. Stand still and watch; do not hit the ball. The five virtual tests are drops from 1.00 m, 1.50 m and 2.54 m, then glass shots at 4 and 7 m/s. Opening the menu or losing tracking cancels the sequence. They do not automatically tune the physics.

Choose **Export test report** to save a stable `report-...jsonl` snapshot. Retrieve it using an authorized PC as explained in [START-HERE-English.md](START-HERE-English.md). This app has no remote report upload or in-headset GitHub integration.

GitHub's attachment support may not accept `.jsonl`. Keep the contents unchanged and place the exported file in a `.zip` before attaching it to an issue; alternatively agree a private transfer method with the owner. Do not commit reports to repository history.

## What reports contain

Reports include build/device model, timestamps, setup values, virtual ball trajectories, virtual racket poses and contact measurements. They do not contain camera images, room scans, audio or account IDs. The data may still reveal a player's movement patterns: sharing is optional. An HP1 screenshot shares settings but not measured trajectories.

Avoid room photos/videos unless needed. Crop or blur personal details before sharing; never upload full headset/system logs without reviewing them.
