# Valley Life (prototype)

A playable Python/pygame prototype of a "do everything in one valley" survival + collecting game,
built to show that a game mixing fishing, farming, digging, mining, hunting, cooking and pets is doable.

## Play it

- **In your browser:** https://davidvstuhl-prog.github.io/Valley-Life/
- **Windows download:** https://github.com/davidvstuhl-prog/Valley-Life/releases/latest (get `ValleyLife.exe`)
- **itch.io:** everything for the itch.io page (zips, cover, screenshots, description, steps) is in [`itch/ITCH_PAGE.md`](itch/ITCH_PAGE.md)

Other ways:

- **Windows:** open the **Actions** tab, click the newest "Build Valley Life .exe" run, and download
  **ValleyLife-Windows** under *Artifacts*. Unzip it and double-click `ValleyLife.exe`
  (if Windows shows "Windows protected your PC", click *More info* → *Run anyway*).
- **Browser:** double-click `valley_life_web.html`. It works with keyboard + mouse or a touchscreen.
- **Python:**

  ```bash
  pip install pygame
  python valley_life.py
  ```

The map is the same every time, and your progress saves to `valley_save.json` next to the game
(autosave every minute and on quit). Delete that file, or click **New game** on the title screen, to start over.
Every push to this repo rebuilds the Windows `.exe` automatically.

## Controls

| Key | Action |
|-----|--------|
| WASD / arrows | walk (SHIFT = sprint) |
| E | use: chop tree, mine rock (hold), plant/harvest, drink, talk to NPCs, serve diners, enter buildings |
| Hold F, aim with mouse, release | cast your fishing rod. Press F / SPACE / click on the **!** |
| Hold SPACE or mouse | reel: keep the fish inside the green box |
| Hold Q | dig up treasure (on grass/sand/cave), or dive for loot in deep water |
| Left click | throw spear / shoot (hunting) |
| R | eat the best food in your bag |
| B | build a campfire (3 logs) to cook anywhere |
| Z / mouse wheel | change selected seed |
| TAB / K / P / G / C / H | backpack / upgrade tree / pets / boost shop / crafting / help |

## What's in it

- **Map**: mountains around a valley, a river, a lake and a pond, forests, a cave with ore, a town with buildings, garden plots
- **Survival**: health, food, water and oxygen (swimming) bars; you faint if health hits 0
- **Fishing**: power-meter cast, bite timing, a reel minigame; 36 fish across river/lake/deep/cave zones (some only bite in the rain),
  day, night and rain-only fish, weights, 9 mutations (incl. Frozen, Shadow, Electric), worm bait, a list of fish you've found
- **Woodcutting**: timing-meter chops (PERFECT hits = 3x damage), 5 tree types, rare Ancient trees, trees grow back
- **Mining**: cave ore with pickaxe tiers (Stone → Mythril)
- **Digging**: hold-to-dig treasure with luck rolls, sparkle spots, holes that refill; diving uses up oxygen
- **Farming**: 12 plots (6 to unlock), 9 crops that grow in real time, Golden/Rainbow/Wet mutations, rain speeds growth
- **Hunting**: rabbits, deer, boars, bears, wolves at night, a rare Golden Stag; animals that run away or attack
- **Cooking**: scale & fillet fish, 9 recipes, a timing minigame that sets quality (Burnt → Gourmet)
- **Restaurant**: diners sit down, order dishes, pay and tip
- **NPC buyers**: townsfolk show up wanting wood, fish, ore, food and so on
- **Progression**: levels, an upgrade tree with 28 nodes, 6 gear lines (rods, axes, pickaxes, shovels, weapons, backpacks),
  storage chest, a quest chain with an arrow pointing to the goal, daily login reward
- **Pets**: 3 eggs, 18 pets in 6 rarities, a hatch animation, equip slots, pet bonuses
- **Coins only**: everything (gear, eggs, seeds, boosts, VIP) is bought with coins you earn by playing. No real-money purchases.

## Files

| File | What it is |
|---|---|
| `valley_life.py` | The game (Python + pygame). This is what the Windows `.exe` is built from. |
| `valley_art.py` | All the art: trees, rocks, buildings, people, animals, pets, item icons and the 2.5D map, drawn with code. |
| `web/template.html` | The same game in JavaScript, for browsers. |
| `build_web.py` | Packs the Python art and world into the browser version: `python build_web.py` writes `valley_life_web.html`. |
| `valley_life_web.html` | The built browser version. |

## Browser version

`valley_life_web.html` is the same game in JavaScript, with the exact same map and art. Double-click it to play in any browser; nothing to install.
After changing the art or the Python world, run `pip install pygame pillow` and `python build_web.py` to rebuild it.
When it starts, it asks whether you're on a keyboard + mouse or a touchscreen. The joystick and big buttons only
appear in touchscreen mode, and you can switch from the pause menu. Progress saves in that browser.
