# Home Padel 0.0.21 — bot difficulty and natural movement

## Choose and start

1. LEFT Menu (three lines) → **Training · bot / ball machine** → X.
2. Set **Training mode** to BOT.
3. Set **Bot difficulty** with LEFT stick left/right: Easy, Medium or Advanced.
   X cycles levels; left/right stop at the endpoints. Centre the stick between pushes.
4. **Bot pace fine-tune** adjusts the selected level from 0.80 to 1.15;
   X resets this multiplier to 1.00. This does not change your racket power.
5. **Start selected mode · no ball** → X. No ball fires automatically.
6. With a RIGHT-handed racket, LEFT X sends a gentle serve. Hit with your
   racket; the bot returns your subsequent shots. LEFT Y stops the bot.
   LEFT-handed play uses RIGHT A/B and the RIGHT index trigger.
7. Opening Menu stops training. Closing alone does not restart it; choose Start.
   To switch to the machine, select BALL MACHINE and Start, then its settings
   for the usual 15 drills. Both modes never run together.

The ball-in-hand placement menu, trigger pickup/drop/toss and saved racket
fit are unchanged from 0.0.20. See `Training-and-HandBall-0.0.21-English.md`
for the hand-release controls and placement adjustment.

## What the levels change

| Level | Placement | Bot movement | Return pace |
| --- | --- | --- | --- |
| Easy | Near centre; preserves legacy ±18 cm setting if previously saved | 2.1 m/s lateral, 2.5 m/s height | Slower: 0.90 × fine-tune |
| Medium | Eight repeatable side/depth targets; up to ±45 cm lateral | 2.6 m/s lateral, 2.8 m/s height | 1.00 × fine-tune |
| Advanced | Eight wider, short/deep targets with varied receiving height; up to ±80 cm lateral | 3.0 m/s lateral, 3.2 m/s height | 1.15 × fine-tune |

Target bounds shrink for narrower/shorter virtual courts. With the default
6.5 × 2.4 m court, Medium spans up to ±45 cm laterally and -10/+40 cm in
depth around the original receiving point. Advanced spans approximately
±76.5 cm laterally and -25/+100 cm in depth. These are ball receiving targets,
NOT body positions or a measured safe room size. You can reach some with your
arm and need steps for others. Pattern order is reproducible, not random.

Faster levels update interception prediction more frequently. Movement stays
bounded; the bot can miss and never teleports the ball. The same simulated
gravity, drag, net, floor and glass determine the flight. Returns are still
controlled neutral-spin practice trajectories, not a physically swung opponent
racket. Racket power, wall 0.55, floor bounce, grip, hand release and previous
reports are unchanged. Long-court flight-time bounds mean pace is a planner
setting, not a guarantee of that exact speed at arrival.

## Natural movement and safety

Medium/Advanced intentionally encourage real steps within your cleared play
area. Keep the Quest boundary ON, use straps, clear obstacles AND full arm
reach. Start in Easy, then increase difficulty only where you have room.
The app does not scan furniture or move targets to follow your tracked head.
Changing virtual court size does not change the physical room or establish a
safe area. If a ball would take you outside the boundary, let it go and use
the free-hand face button for a new serve. Never retrieve it physically.

## Feedback

Keep **Calibration & reports > Auto-save game data** ON. Try the same strokes
for one minute at each level with pace 1.00, then report difficulty, court,
pace, headset model and whether placement/pace felt appropriate. Launch
records include `botDifficulty`; bot impacts and return counts remain separate
from your racket hits. Nothing uploads automatically. HP1 does not include
bot difficulty or ball placement: send their menu screenshots separately.

Update with `HomePadel-0.0.21-English.apk` without uninstalling. Automated
checks/editor previews are not proof of physical comfort, realistic difficulty
or sustained Quest performance. No scoring, full match rules or multiplayer.
