# Home Padel 0.0.21 — bot, machine and ball in hand

Update with `HomePadel-0.0.21-English.apk`; do not uninstall first. This is an
offline sideload prototype for Quest 3/3S, not a certified Store app.

## Switch training modes

1. Press the LEFT Menu button (three lines).
2. Open **Training · bot / ball machine** with X.
3. Highlight **Training mode**. Push LEFT for BALL MACHINE or RIGHT for BOT;
   X also switches them. Release the stick between deliberate pushes.
4. For BOT, choose **Bot difficulty: Easy / Medium / Advanced**, then
   **Bot pace fine-tune** (0.80–1.15). See `Bot-Difficulty-0.0.21-English.md`.
5. Select **Start selected mode · no ball**, then X. The menu closes with
   only that mode ready. No ball fires automatically.
6. With a RIGHT-handed racket, free-hand LEFT X sends one ball: a gentle
   serve for BOT, the selected drill for MACHINE. BOT returns your subsequent
   racket shots, not an untouched serve/drop. LEFT Y stops an active bot;
   otherwise it toggles automatic machine feeding.
7. To configure repeat practice, choose **Ball machine settings** and use
   **Launch one ball** (two-second delay) or **Start practice** (chosen interval).

For a LEFT-handed racket, gameplay free-hand controls use RIGHT A/B and the
RIGHT index trigger. Options always use the LEFT stick and X/Y.
Opening Menu stops both modes; closing it does not restart either. Select
Start again. Tracking loss/app pause/calibration also cancel training safely.

The bot uses real simulated bounces and bounded movement. It can recover
some shots after either back glass, but can miss high/wide/fast shots. Returns
use fixed court coordinates with level-dependent placement, NOT your tracked
head or a scanned safe spot. They are controlled neutral-spin practice shots, not full physical
opponent swings. No scoring, complete padel rules or multiplayer.

## Fit and release the ball

1. Open **Ball in hand · fit & release**. A live ball preview appears on
   the free hand while the game remains paused. No squeeze is needed here.
2. Select RED, GREEN or BLUE position. LEFT stick RIGHT moves toward that
   coloured arrow; LEFT moves the opposite way. The arrows rotate with the
   controller, not the room. One step is 2 mm; hold the LEFT trigger for 0.5 mm.
3. X resets the selected axis. **Reset ball fit** resets only this free hand's
   ball position, not racket fit or physics. Values are total offsets in cm.
4. Choose **Save and try a drop**. Fully open the free-hand trigger first.
5. Squeeze the free-hand INDEX trigger at least halfway to hold a ball.
   Keep it squeezed while moving. Open it to release before the very end
   of the trigger travel. A still hand drops it; a moving hand tosses it.
6. Open fully before squeezing again for another ball. Automatic feeding,
   pending machine launches, menus and fixed calibration block pickup.

Ball fit saves separately per free hand. Default placement is 12 cm along
the grip-local blue axis; this is a starting fit, not a universal hand position.
Release uses tracked grip velocity plus the held point's rotational velocity
when valid, otherwise recent filtered movement. There is no preset boost or
aiming assistance. Tracking jumps/gaps reset release history, not create a serve.

## Five-minute feedback test

- Use wrist straps, clear your full arm reach and keep the Quest boundary ON.
   Start in Easy. Medium/Advanced use natural steps only within a cleared
   real area and your boundary; leave out-of-area balls. Virtual walls do NOT
  detect furniture or define a safe real-world court.
- Keep **Calibration & reports > Auto-save game data** ON.
- With both modes OFF, make five still-hand drops, then five gentle upward
  tosses and five gentle forward tosses. Do not use dangerous fast swings.
- Try BOT at Easy, pace 1.00. Test straight shots, one-bounce shots and gentle
  own-back-glass shots, then switch to MACHINE and back through the menu.
- Send a ball-fit screenshot (three cm values and racket hand), what felt
  wrong, headset model and a voluntary exported JSONL report. `hand_release`
  records include placement, release velocity/state, trigger value and whether
  tracked grip velocity or pose history was used. `TrainingBot` events and
  bot return counts are separate from your own racket hits. Nothing uploads.
- The HP1 code does not contain ball placement or bot settings. Retrieve
  reports using the English start guide. Do not uninstall before retrieving.

Automated checks and editor previews are not proof of natural release feel,
passthrough comfort or sustained Quest frame rate. Those need on-headset tests.
