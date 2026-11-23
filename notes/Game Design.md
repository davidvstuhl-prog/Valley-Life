---
tags: [valley-life, design]
---
# Game Design

Back to [[Home]] · Numbers live in [[Balance Numbers]]

## The idea
A valley surrounded by mountains, with forests, rivers, a lake, a cave and a small town.
You gather, craft and sell to get better gear, unlock upgrades and hatch pets.
Everything is bought with **coins** earned by playing. There are no real-money purchases.

## World
- **Town:** Home (storage), Shop, Market, Upgrades, Workshop (crafting), Pet Hatchery, Kitchen (and restaurant), Boost Shop
- **6 forests:** Pine Ridge, Whispering Pines, Oakwood, Old Oak Wilds, Birch Grove, Maple Hollow
- **Water:** river, lake, pond, and a cave pool, each with its own fish
- **Cave** in the north-east: ore and cave fish, and it's dark inside
- Day and night cycle, plus rain (crops grow faster, fish bite faster)

## Survival
Health, food, water, and oxygen (only underwater). Fainting costs 10% of coins, or 200 coins to revive on the spot.

## Systems
### Fishing
Hold F to charge the cast, wait for the **!**, then the reel minigame: keep the fish inside the green box.
36 fish in 6 rarities. Some only bite at night, some only by day, and some only **in the rain**.
Mutations: Shiny, Golden, Rainbow, Cosmic, plus fish-only ones: Albino (x2), Giant (x3, extra heavy), Frozen (x4, cave only), Shadow (x5, night only), Electric (x6, rain only). Worms are bait.

### Woodcutting
Timing meter: hit in the green for **PERFECT** (3x damage). 5 tree types plus rare **Ancient Trees**.
Stumps have no hitbox and regrow after 45 seconds.

### Mining & digging
Rocks in the cave and near the mountains. A weak pickaxe still works, just very slowly (like obsidian in Minecraft).
Hold Q to dig on grass, sand, or cave floor. Sparkle spots are luckier. Diving in deep water finds pearls and chests.

### Farming
12 plots (6 to start). 9 crops that grow in real time. Mutations: Golden (5x), Rainbow (15x), Wet (2x in rain).

### Hunting
Right click throws a spear, and a left click up close swings your axe.
Rabbit, Deer, Boar, Wolf (at night), Bear, and Golden Stag. Boars, wolves and bears fight back.

### Cooking & restaurant
Raw fish work in recipes (Epic+ and mutated fish are protected). QUICK and MAX buttons, or the COOK minigame for Perfect/Gourmet food.
The restaurant costs 400 coins to open. Serve diners from the kitchen menu for 1.5x value plus tips.

### Crafting
33 recipes at the **Workshop**. Survival recipes work anywhere.
Tabs: Materials, Tools, Charms (permanent bonuses), Survival.

### Pets
3 eggs, 18 pets, 6 rarities. Pets follow you and give bonuses. 1 slot to start, up to 4.

### NPCs
8 buyers wander the whole valley with requests (shown as blue dots on the minimap).

### Progression
Levels, a 28-node upgrade tree, gear tiers, quests (a tutorial chain, then random ones), and a daily reward.

## Two versions
- **Python** (`valley_life.py`, `valley_art.py`): this is where the art and world come from, and the `.exe` is built from it.
- **Browser** (`web/template.html`): the same game in JavaScript. `build_web.py` packs in the Python art and world.
