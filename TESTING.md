# Testing and calibration feedback

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
