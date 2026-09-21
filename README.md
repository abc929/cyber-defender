# Cyber Defender Obby

A free, single-file browser game that teaches kids (ages ~9–13) cybersecurity through an
obstacle course: 8 stages, each built around one concept, ending in a "quiz gate" where the
player must choose the right door to move on. No installs, no accounts, no ads, no internet
needed once the page is open. Works on laptops (keyboard) and tablets (on-screen buttons).

Progress, the Hall of Fame and unlocked stages are saved in each player's own browser.

## The 8 stages

| # | Stage | Concept | What the player does |
|---|-------|---------|----------------------|
| 1 | Password Gate | Strong passwords | Learn the controls, cross lava, pick the strongest password door |
| 2 | Phishing Bridge | Spotting phishing | Three message gates: walk into the REAL message; phishy doors zap you |
| 3 | Two-Factor Tower | 2FA / MFA | Remember the code on the sign, climb for the key card, unlock the keypad |
| 4 | Oversharing Maze | Personal info | Collect safe-to-share tokens, jump over private info |
| 5 | Malware Lava Field | Malware & downloads | Ride "official download" platforms; fake "free Robux" bricks are deadly |
| 6 | Update Elevator | Software updates | The elevator only works after you choose "Update now" |
| 7 | Chat Room | Strangers online | Spot the red flags in a stranger's chat; block, report, tell an adult |
| 8 | Encryption Vault | Encryption | Decode a shift-3 cipher to find the right vault door |

Each cleared stage shows a short fact card. Finishing all 8 gives a printable
**Cyber Defender certificate**. The title screen has a **Facilitator guide** (printable) with a
debrief question and an at-home activity for every stage — you do not need to play to run a lesson.

## Controls

- Move: **← →** (or **A / D**) · Jump: **SPACE** (or **↑ / W**)
- Walk into a door and press **JUMP** to choose it. Wrong door = back to the checkpoint, so read first.
- Tablet / phone: on-screen buttons appear automatically. Landscape works best.
- **☰** (top right) pauses and opens the menu; **Stage select** lets you replay any unlocked stage.

## Change the words (no coding needed)

Open `index.html` in any text editor (Notepad, TextEdit, VS Code) — or on GitHub click the file,
then the **pencil** icon to edit in the browser. Near the top you will find:

```
const CONTENT = { ... }
```

Everything the game says lives there: stage names, questions, the three options,
which one is correct (`answer: 0`, `1` or `2`), tips, fact cards, the stranger's chat
messages, and the facilitator guide text. Change the text between the quotes, save, and
refresh (or **Commit changes** on GitHub — the live site updates in about a minute).

Two quick rules: keep the quotes around text, and if a sentence contains an apostrophe,
write it as `\'` (for example `'the game\'s update'`).

## For a young builder

The stages themselves are defined further down in `LEVELS`, using a tiny builder language:
`B.ground(400)` makes 400 px of floor, `B.gap(70)` a hole, `B.lava(100)` a virus pool,
`B.plat(120, 450)` a floating platform, `B.checkpoint(x)` a flag, `B.sign(x, 'text')` a sign,
and `B.gate({ labels: [...] })` the three-door finish. Copying a stage, changing a few numbers
and adding a 9th entry to `CONTENT.stages` is a great first project — the game will pick it up
automatically.

Free to use, copy and adapt for classrooms, scout troops, homeschool co-ops and clubs.
