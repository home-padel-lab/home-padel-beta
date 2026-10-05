# Home Padel Lab — English test build 0.0.23

This is a standalone Android APK for testing on a Meta Quest headset. The development target is Quest 3. It runs locally without a game account or an online server. This prototype does not have multiplayer.

Install `HomePadel-0.0.23-English.apk` using your Quest APK installation setup. It is not a Store app; a headset configured for installing development APKs is needed. Open **Home Padel Lab** and wake both controllers if the headset asks for them. Android/Meta system dialogs use the headset's language, not the game's English menu setting.

Build 0.0.23 adds **Court & physics > Court size > Singles size preset / Match format**. See [the current court guide](Court-Profiles-0.0.23-English.txt). Compact, Medium and Large singles are 2.4×6, 3×7 and 5×10 m (width × length); doubles layouts are 4.8×9.6, 6×12 and 10×20 m. Doubles doubles the base singles width, then fixes length to twice the new width. Existing dimensions, including 2.4×6.5, migrate exactly as Custom; selecting Compact explicitly changes them to 2.4×6. New installations start Compact singles. HP2 setup codes preserve the singles base and doubles flag; this app still imports HP1, but older versions cannot import HP2. Ball fit and bot level are not encoded. Player swing/bounce/flight parameters and saved fit/reports are retained; machine/bot trajectories are replanned above 8 m, with faster launches where needed. Doubles is only a layout, not multiplayer or a second bot. Court size does not measure your safe real room; stay within your cleared area and Quest boundary. Older version descriptions below preserve history.

Build 0.0.22 reorganizes the menu into **Play & training**, **Equipment fit**, **Court & physics**, and **Reports & sharing**. See [the current menu guide](Menu-Guide-0.0.22-English.txt). Y returns to the previous screen and remembers its selection; long screens show five rows at once. Each selected row explains its action. Restoring a complete setup or importing needs two X presses; Y or changing row cancels. X on numeric rows still resets only that value, explicitly labelled. Racket-hand X toggles hands. Opening Menu stops both modes; closing alone does not restart them. Physics, geometry, difficulty, saved fits and reports are unchanged. The older version descriptions below preserve history, not the current menu paths.

Build 0.0.21 adds **Bot difficulty: Easy / Medium / Advanced** in **Training · bot / ball machine**. Easy returns slowly near the centre; Medium varies sides and depth; Advanced uses wider, short/deep targets, faster returns and quicker bounded bot movement. Use LEFT stick left/right to select a level, or X to cycle; then **Start selected mode · no ball**. Difficulty is saved independently. The existing pace slider now fine-tunes each level. Upgrades without a level saved start in Easy; previous pace/legacy Easy placement settings remain. See `Bot-Difficulty-0.0.21-English.md`. Natural steps are intended in Medium/Advanced, but only inside a cleared real area and your active boundary: virtual court dimensions do not prove that area is safe. The app does not scan furniture or recenter return targets on your head. Start with Easy. Player racket/bounce and hand-release physics remain unchanged; reports identify the bot level. HP1 does not contain bot difficulty or ball placement.

Build 0.0.20 introduced the shared **Training · bot / ball machine** selector and **Ball in hand · fit & release** with a live ball preview and coloured controller-local adjustment arrows. See the updated `Training-and-HandBall-0.0.21-English.md` for current controls and a short test checklist. The bot predicts with the actual floor/glass/drag/spin solver, including shots off your own back glass. Selecting a mode does not fire a ball. Grip velocity (including wrist rotation) is used at release when valid and consistent with recent movement; a short filtered position history is the fallback. Trigger pickup/release thresholds are 55%/35%, with full neutral needed after a menu or cancellation. There is no preset throw boost. Ball placement saves separately for each free hand. Racket fit, power response, wall bounce and earlier reports remain intact. Bot returns remain controlled neutral-spin practice trajectories, not full opponent swings; it can miss and is not a match AI. No multiplayer or furniture detection.

Build 0.0.18 adds free-hand ball pickup/release when the ball machine is OFF. With the racket in your right hand, squeeze and hold the LEFT index trigger to hold a ball above that controller. Open the trigger to drop it; move your hand while releasing to toss it. The toss inherits measured hand movement, without a preset launch boost or aiming assistance. Squeeze again for another ball. A left-handed racket mirrors this to the right controller. The ball cannot be picked up during automatic feeding, a pending machine launch, menus or fixed calibration. Menu, tracking loss or app pause cancels a held ball without throwing; release the trigger fully before picking up again. Hand releases also start local reports if auto-save is ON. Stand in your safe area; do not chase the ball.

Build 0.0.17 migrates rendering to URP with fixed foveation and requests 72 Hz. It adds inexpensive transparent glass and a simple ball shadow, without changing the physics, saved racket fit or menu controls from the published 0.0.16. It excludes unused developer agents/debugger tools, eye-tracking/capture permissions and network/microphone permissions. It is an offline sideload beta, not a certified Store release. Quest 3S is a development target but remains untested. Check the room remains visible, menus/paddle render correctly and movement stays smooth. Stop playing if passthrough is lost. Sustained 72 Hz and visual behaviour still require headset testing.

The published 0.0.16 build uses **Wall bounce = 0.55** and **Racket power = 0.45** by default. A perpendicular wall hit returns 55% of its incoming normal speed; this is not a uniform reduction of total speed for angled/spinning hits. Updating from the previous saved 0.45 wall default adopts 0.55 once; other custom wall values and all saved power, grip, court, floor and report data are preserved. Old preferences remain intact. After updating, check **Menu > Bounce & feel > Wall bounce**; use 0.55 for a comparable baseline. Do not reset all settings or uninstall the app.

Build 0.0.16 adds experimental progressive racket response for the compact court. Advancing contact-point speed normal to the face is unchanged up to 3 m/s; above this, response speed is `3 + 2 * ln(1 + (speed - 3) / 2)`. Faster swings still produce stronger shots, without a hard speed cutoff. Raw tracking, collision geometry and incoming ball velocity are not scaled. The response works in all face directions, not only upwards, and leaves floor/glass/net responses unchanged. Your saved power, wall bounce, grip, court and reports are retained. Racket spin can differ on compressed hits because friction depends on the contact impulse. This is an experimental feel adjustment, not a measured real-world padel model.

To compare: use the same drill and settings as 0.0.15. Start with several soft taps, then moderate upward taps and normal faster strokes while standing still. Keep auto-save ON. Do not swing dangerously fast or chase balls. Reports include the raw `SurfaceVelocity`, the `ResponseSurfaceVelocity` used for response, and the curve parameters at each launch. The curve is fixed in this build and is not part of an HP1 code; always include the build number when sharing a configuration.

Build 0.0.18 corrects a reproduced repeated-contact case: an overlapping racket/ball episode could create up to 12 reported contacts, most with zero impulse, and exhaust a physics step. A new hit now requires geometric separation from the face, with 1 mm hysteresis, rather than an arbitrary timed cooldown. Zero-impulse contact is diagnostic only, not a hit or vibration. Reports add `racketContactHeld` to trajectory samples and `zeroImpulseRacketContacts` to samples/ball summaries. This does not prove every contact is correct: send reports if taps feel strange or repeated. Wall 0.55, racket power 0.45, the progressive speed curve and your saved grip remain unchanged.

The supplied yellow padel-ball model from build 0.0.11 is retained, including its seam and logo. Its diameter remains 67 mm and its visible spin follows the simulation. Shared setup codes and saved grip/bounce adjustments remain compatible.

Build 0.0.12 adds automatic local test reports and five fixed calibration tests. Physics responses and your saved grip/bounce values are not automatically changed by recording or calibration.

Build 0.0.13 makes menu changes more deliberate and increases racket-impact vibration. Push the LEFT stick firmly in one direction: the menu ignores axis input below 75% and ambiguous diagonals. Release toward the centre between pushes for single steps. Holding starts repeating after 0.65 seconds, then once every 0.35 seconds. Return to centre before changing direction. X/Y take priority over stick movement, so pressing a button cannot accidentally act on a different row. Keep holding the left trigger for fine racket/physics adjustments.

Impact vibration is stronger on the controller holding the racket, with stronger pulses for harder hits. Floor, glass and net bounces do not vibrate your hand. Very small racket microcontacts do not keep buzzing. Actual vibration feel and requested pulse duration still need testing on your headset.

Build 0.0.14 changes the compact court: default length 6.50 m (previously 6.00), width 2.40 m, net height 0.78 m (previously 0.88), back walls 2.00 m and lower middle side walls 1.40 m. End sections and the doorway frames are taller, at 2.00 m. Side door openings are 0.80 m wide and 1.75 m tall. Balls can leave through the doors or above the visible walls; invisible tall glass is not retained. These are experimental virtual proportions, not regulation padel dimensions or measured Racket Club geometry.

In build 0.0.14, the default glass response changed to 0.35 instead of 0.50: a perpendicular, no-spin contact returned 35% of the incoming normal speed. Angled/spinning contacts also depend on friction. Floor response, gravity, racket fit and the build 0.0.13 controls were unchanged. Glass drills start closer to the appropriate side so they hit a visible panel. The current published default is 0.55, as described above.

Updating preserves custom grip, floor/physics settings and saved reports. Untouched old 6.00 m / 0.50 defaults migrate once to 6.50 m / 0.35; other custom length and wall-response values are retained. To try the new defaults with a custom configuration, use **Court size > Reset court** and reset only the **Wall bounce** row in **Bounce & feel**. Do not reset your racket fit. HP1 codes remain readable, but the wall/net profile is defined by the build: compare configurations on the SAME app version and include the version in feedback.

## Install on a friend's Quest

Build 0.0.15 uses **Wall bounce = 0.45** and **Racket power = 0.45**. This restores a little wall return compared with 0.30–0.35 while reducing racket response compared with 0.65. The first update to this tuning profile deliberately adopts BOTH values even if an earlier build saved different wall/power settings. Previous values remain in separate old preferences; no uninstall or data clearing is needed. Subsequent adjustments in 0.0.15 are remembered normally. Racket fit/hand, court size, floor response, friction, spin, menu controls, haptics and local reports are retained.

Only the response settings change: the physics does not clamp ball speed or cap your swing. Faster swings still produce stronger shots, but the new racket response is softer. These are experimental settings informed by play feedback, not measured real-world padel constants. To compare: repeat **Slow straight shot**, vary only one value at a time and keep auto-save ON. Share an HP1 setup screenshot and, optionally, an exported report.

Send the APK and this guide, or the ZIP containing both. Extract the ZIP on the computer first. Your friend does NOT need Unity or the project source.

1. Use a Quest 3 with both controllers. Other Quest models have not been tested.
2. Enable Developer Mode and complete any developer-account requirements in [Meta's official headset setup guide](https://developers.meta.com/vr/documentation/unity/unity-env-device-setup/). Install the Quest USB driver on Windows if required by that guide.
3. Connect the headset to the computer with a USB DATA cable. Put on the headset and approve **Allow USB debugging** for your own computer.
4. If you already use an APK installer, install `HomePadel-0.0.23-English.apk` with it. Otherwise follow the Windows alternative below.
5. Open **Home Padel Lab** from the headset's sideloaded-app library (commonly labelled **Unknown Sources**; the library layout may vary). Wake both controllers if prompted. Once installed, the USB cable and PC are not needed to play.

### Windows alternative: Android Platform Tools

Download [Google's official SDK Platform Tools for Windows](https://developer.android.com/tools/releases/platform-tools), extract them and copy the APK into the extracted `platform-tools` folder. Open PowerShell in that folder and run these commands one at a time:

```powershell
.\adb.exe devices
.\adb.exe install -r .\HomePadel-0.0.23-English.apk
.\adb.exe shell am start -n com.homepadel.lab/com.unity3d.player.UnityPlayerGameActivity
```

Before installing, the first command must show your headset with the status `device`. If it says `unauthorized`, approve USB debugging inside the headset. If it shows no headset, check the data cable and driver. Installation should finish with `Success`. If more than one Android device is connected, disconnect the others before using these commands. The `-r` option updates the same app while keeping its local settings. See [Android's official ADB guide](https://developer.android.com/tools/adb) for troubleshooting.

## First two minutes

Clear a safe standing area and keep the Quest boundary active. Press the LEFT Menu button (three lines). Use the LEFT stick up/down to select, left/right to change, and X for the labelled action. Start with **Equipment fit > Racket fit**, then **Save and test grip**. Reopen Menu, choose **Play & training > Ball machine**, select **Slow straight shot**, then **Launch one ball**. It launches after two seconds. Once comfortable, select **Start practice** for repeated balls. Opening Menu stops both modes.

For gentle tap testing, keep the machine OFF and close Menu. Hold the LEFT trigger to pick up a ball, then release it above the racket face. Try ten small upward taps without leaving your safe standing area. Compare slow and moderate strokes before changing power or bounce. The grip anchor and pose have been checked mathematically; only you can confirm the physical fit while holding the controller. Existing calibration has not been reset.

## Automatic recording and calibration

**Just play:** recording is ON by default. Each launched ball starts a measured trial. Launches, setup values, ball trajectories, virtual racket poses and floor/glass/net/racket contacts are saved locally. Opening Menu ends that ball's trial; launching again starts another. Nothing is uploaded. No camera images, room scans, microphone audio or account IDs are recorded.

1. Play for a few minutes using the same court and one repeated drill or bot level. Keep your boundary active and move only within your cleared area. Leave escaped/out-of-area balls; do not go beyond your boundary to retrieve them.
2. Open **Menu > Reports & sharing > Recording, tests & feedback**. **Auto-save game data** shows ON/OFF. X or left/right toggles it. The choice is remembered. OFF prevents new measurements and feedback, but does not delete existing reports.
3. Optionally select **Your feedback** with left/right, then highlight **Save feedback** and press X. Ratings are linked to the last recorded ball: Feels good / Bounce too high / Too fast / Too many bounces.
4. Select **Export test report**, then X. This creates a stable `report-...jsonl` snapshot containing the session so far. The filename appears on screen. Export does NOT send it anywhere. Repeated export without new data reuses the same snapshot.
5. Connect the headset to an authorized PC when you want the files retrieved. Your tester can send the exported report, their headset model and a short description of what felt wrong. A setup-code screenshot alone does not include measured motion/bounce data.

**Run calibration:** highlight this action and press X. The menu closes, waits two seconds and runs five virtual tests lasting about 17 seconds in total: drops from 1.00 m, 1.50 m and 2.54 m, then perpendicular glass shots at 4 and 7 m/s. Stand still and WATCH; do not hit or chase these balls. Racket collisions are disabled during these tests. Launches are fixed and are not re-aimed when bounce settings change. Opening Menu, losing racket tracking or pausing the app cancels the sequence. Reopening Menu lets you export the results. The tests do not automatically select new physics values.

Normal play and fixed tests use the same physics. Ball/racket trajectories are sampled at 15 Hz; significant contacts are recorded individually. Very small contacts below 0.2 m/s are counted separately to avoid flooding the report. Rebound peak height is measured on each physics step and recorded at floor contacts. The report identifies metres, seconds, rad/s, build version and the exact configuration at each launch.

Reports are in the app's `CalibrationReports` folder, with snapshots in `CalibrationReports/Exports`. For the current Android build, PC-assisted retrieval normally uses:

```powershell
.\adb.exe pull /sdcard/Android/data/com.homepadel.lab/files/CalibrationReports ./HomePadelReports
```

Run this from your Platform Tools folder with the authorized headset connected. Send a `report-...jsonl` file from the retrieved `Exports` folder. If access fails, ask for PC-assisted retrieval rather than changing unrelated device permissions. Installing an update with `-r` keeps app files; uninstalling the app can remove them, so retrieve reports first.

Files are flushed about every 250 ms, and on app pause/normal shutdown. An abrupt crash or power loss can lose the last buffered records. Recording stops with an error if a session reaches 20 MB or the report folder reaches 100 MB. No old reports are automatically deleted. Check the report status in this menu; it must not show SAVE ERROR. These files contain simulated-game measurements, not proof of real-world accuracy.

## Gameplay and options controls

- Right controller: racket.
- Left X: one gentle serve while the bot is active; otherwise one machine ball.
- Left Y: stop an active bot; otherwise start/stop automatic feeding.
- Free-hand index trigger: hold a ball when automatic feeding is OFF, open to drop/toss. Use **Equipment fit > Ball in hand** if its placement feels wrong.
- Left Menu button (three lines): open options; press again to save and close.
- Every options screen uses the LEFT controller: stick up/down selects a row, left/right changes its value, X performs the labelled action, Y returns to the previous screen. Complete restores/imports need a second X. The bottom line says exactly what X will do.
- **Racket fit** combines hand, position and rotation on one screen. For grip position, match the RED/GREEN/BLUE arrow near your virtual handle: push the left stick right to move toward that arrow, left to move the other way. Rotation controls show your adjustment relative to the default, starting at zero degrees. Hold the left trigger for smaller adjustment steps. **Save and test grip** closes without launching a ball.
- **Court & physics > Bounce & racket power** has wall/floor bounce and racket power; **Advanced spin & friction** has friction and spin. X resets only the highlighted numeric value. **Restore physics defaults** resets all seven physics values, after confirmation, without changing grip/court.

Opening the menu pauses the ball and stops the machine, including any pending shot. Pressing Menu to close saves your settings but does NOT launch a ball. Explicit launch/start actions below are the exception because you deliberately chose to start. Losing racket tracking also stops the machine. Settings are saved locally on your headset, including hand, grip, physics, court and drill settings.

## Start the ball machine

1. Open Menu, select **Play & training > Ball machine**, then press X.
2. Highlight **Shot type** and use left/right to choose a ball. Start with **Slow straight shot**.
3. Set **Seconds between balls** and **Practice mode**: repeat one shot or cycle all fifteen.
4. Select **Launch one ball** and press X for ONE ball after a two-second delay, or select **Start practice** and press X for automatic feeding after the selected interval.
5. The menu closes so you can play. Press Menu to stop safely and adjust again. With a right-hand racket, left Y also stops/starts auto-feed during play; left X launches a ball manually. For a left-hand racket, these gameplay actions use right A/B. Configuration always uses the left controller.

If the selected drill shows **NOT FEASIBLE**, change the court/bounce or choose another ball. Launch actions stay blocked until a valid trajectory exists. **Save & close · machine OFF** closes the menu without starting training.

## Send a good setup back

1. Open **Reports & sharing > Share or load a setup**, or use **Share racket fit** / **Share bounce & feel** from the adjustment screen.
2. In **Settings to share**, choose **Racket only**, **Physics setup** (physics/court/machine), or **Racket + physics setup** with left/right. HP1 does NOT include ball fit or bot difficulty.
3. Take a screenshot showing BOTH lines of the `HP1-...` setup code and send it with your feedback. No configuration-file access is needed for this method. The code reproduces the chosen settings; it is not just a random reference number.
4. Please include headset model, racket hand, drill used and what improved. Change one physics setting at a time and compare the same drill at the same court size.

Racket-only imports never change physics/court. Physics-only imports preserve another player's personal grip and racket hand. A grip that feels good for one player is not automatically correct for everyone.

Optional: **Export JSON file** saves a full-precision setup file into the app's `Setups` directory; its filename appears on screen. Retrieving that file from the Quest currently needs PC-assisted app-file access. Exporting does not send a message or upload a file automatically.

The existing HP1 sharing code covers racket/physics/court/machine settings, NOT the new ball-in-hand placement or bot pace. For ball placement, send a screenshot of the three centimetre values with the racket hand, plus a report containing a few drops/tosses. For bot feedback, include pace, placement and court size.

Import currently uses **Load SharedSetup.json** after a supplied JSON file (or plain setup code) has been placed in the app's files using a PC. The desktop lab can also paste and apply a setup code. There is no in-headset keyboard or one-click network sharing yet. Import always stops the machine and validates version, model and parameter ranges; code checksums catch damaged code text.

## Safety and feedback

### Rendering check (0.0.17)

For a useful comparison, wear the headset and use the same drill/settings for 2–3 minutes. Include a minute of normal strokes, turn your head naturally and open/close the menu. Keep a clear standing space; do not chase balls. Tell us if glass hides the room, either eye shows an incorrect image, menus/paddle are missing or movement stutters.

A separate local CSV is saved every five seconds while the app is running. It records game timing/counters, not video/audio. Retrieve it with your authorized PC:

```powershell
.\adb.exe pull /sdcard/Android/data/com.homepadel.lab/files/reports/performance ./HomePadelPerformance
```

Send the `render-...csv` file voluntarily with headset model, build number and which drill you used. Empty CPU/GPU/counter columns mean unsupported measurements, not zero cost. Display Hz and app-observed FPS do not by themselves prove compositor stability. Existing physics JSONL reports remain in `CalibrationReports` as described above.

Start with **Slow straight shot** or **Easy bot**, one ball at a time, while standing in one place. For Medium/Advanced bot play, clear room for natural steps as well as the entire reach of your arms and controllers. Keep the Quest safety boundary active and use wrist straps. Movement is part of training, but never follow a ball outside the cleared area; reset it with the free-hand face button instead. Stop if passthrough or tracking is lost.

The virtual court and walls are NOT a measurement of safe physical space. This prototype does not detect furniture or obstacles. Court size changes virtual geometry only.

Please report: headset model, grip alignment, racket-face orientation, bounce feel, any missed contacts, and whether the menus are readable. A screenshot or short recording helps. Physics values are experimental, not measurements of a real padel racket or ball.
