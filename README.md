# Deity Zenith SWGB Saga

A summoning CE table for **STAR WARS Galactic Battlegrounds Saga**, by Bener Kaya.

Deity Zenith lets you play god in **STAR WARS Galactic Battlegrounds**. Pick a civilization and something to summon in the Cheat Engine table, point at the map, press the summon key, and it appears there:

- **Units, buildings and heroes** of all eight civilizations
- **Neutral creatures and objects** from the editor's Gaia list

You also choose **whose side** the summons are on: **Current player**, Gaia, or another player slot. You choose how many to summon in one press.

Summons are placed through the game's own routines, including its terrain, snapping and collision checks.

## Features

- **Civilization → Summon Type → Summon** filters. The lists match the scenario editor: the eight playable civilizations plus Gaia.
- **Units, Buildings or Heroes**, with a separate **Side** selector for the owner.
- **Picked-civilization appearances** for units and heroes, even when the owner belongs to another civilization. No global civilization or template changes.
- **One summon key** (**F1** by default, because the other function keys are used by the game), or **Mouse middle button**.
- **Cursor on map** or exact map-tile coordinates.

## What you need

- **STAR WARS Galactic Battlegrounds Saga** on Steam, **Clone Campaigns 1.1**, 32-bit. Deity Zenith only works with this exact `battlegrounds_x1.exe`:
  - SHA-256 `bbc13b1fa05cafe824ab023e5ab4409c01ced576a071eb0e4eb93da4be748e28`
  - The base-game executable, Expanded Fronts and other executable or data mods are not supported.
- **[Cheat Engine](https://www.cheatengine.org/) 7.5** or newer.
- Optional: **[cnc-ddraw](https://github.com/FunkyFr3sh/cnc-ddraw)** for windowed mode and easier Alt+Tab. If you use it, only the verified wrapper next to `battlegrounds_x1.exe` is accepted:
  - SHA-256 `85e0f7d530dfda134793a57cb3e76b0287dcc96892ee57162dd68f47283b03a9`

Deity Zenith is made for **Singleplayer**. Multiplayer and replays are not supported.

## Install

Nothing to install into the game folder. Keep these files in any folder:

| File | What it is |
|---|---|
| `Deity Zenith Galactic Battlegrounds.CT` | the Cheat Engine table |
| `EDITOR_CATALOGUE.txt` | every unit, building and hero in the lists |
| `README.md` | this file |

The table works on its own: the lists are built into it. The catalogue file is only there for reference and can be kept anywhere (or left out).

## How to use it

1. Start **STAR WARS Galactic Battlegrounds Saga** and enter a **Singleplayer** game.
2. Start **Cheat Engine** and open **`Deity Zenith Galactic Battlegrounds.CT`**.
3. Manually attach Cheat Engine to **`battlegrounds_x1.exe`**.
4. Tick **"Deity Zenith - Enable"**. The summon rows appear once Enable has initialized.
5. Choose **Civilization**, **Summon Type** and **Summon**, set **Side** and **Count**, put the mouse on the map and press **F1**. To use the mouse wheel button instead, set **Summon Key** to **Mouse middle button** and click the wheel once (scrolling does not summon).
6. Untick **"Deity Zenith - Enable"** before closing Cheat Engine or changing matches.

To change a selector, double-click its **Value** cell and pick from the list. Do not tick selector rows to freeze them.

## The table

| Entry | What it does | Default |
|---|---|---|
| **Deity Zenith - Enable** | turns Deity Zenith on after you attach to the game | off |
| ---Summon Units/Buildings/Heroes--- | section title, does nothing | |
| **Civilization** | whose list to use: the eight civilizations, or **Gaia** | Galactic Empire |
| **Summon Type** | Units, Buildings or Heroes: switches the Summon list | Units |
| **Summon** | what to summon (filtered by both Civilization and Summon Type) | (E) Trooper Recruit |
| **Side** | **Current player**, Gaia / slot 0, or present player slots 1–8 | Current player |
| **Count** | how many appear per key press: pick 1–25 from the dropdown | 1 |
| **Where** | Cursor on map, or Map tile X / Y | Cursor on map |
| **X / Y** | shown in tile mode; zero-based map tiles, not pixels | |
| **Summon Key** | F1–F12 or Mouse middle button | F1 |
| ---Other--- | section title, does nothing | |
| **Diagnostics** | Status, last result and counts (collapsed; shown while Enable is ticked) | |

Civilizations: Galactic Empire, Gungans, Rebel Alliance, Royal Naboo, Trade Federation, Wookiees, Republic, Confederacy, and Gaia.

## Good to know

- **Gaia summons** use the editor's Gaia player list (neutral creatures and objects that only appear when the Gaia player is selected). Choosing Civilization = Gaia switches **Side to Gaia** automatically, the same as the editor. Leave Side on Gaia to place them. After they are on the map, you can convert them in the game as usual.
- If Side is not Gaia and you try to summon from the Gaia list, nothing is placed. Status explains why, and Enable unticks itself a moment later. Tick Enable again, set Side back to Gaia, and summon once more.
- **Units and heroes keep the picked civilization's look** even when they belong to another player. **Buildings keep the picked civilization's portrait**, but if you summon them directly onto your side, the game can still give them your faction's map skin. To keep a building's original skin, summon it as Gaia and convert it in the game.
- Researched technologies, team bonuses, production rosters and later upgrades stay with the owner. They are not copied from the picked civilization.
- **Buildings need room.** The game's own placement checks stay on. If a spot is blocked, nearby tiles within eight tiles may be tried, so a batch may place only some of the requested count.
- **Count** (1–25) is how many appear **per key press**. It is not a limit on how many you can summon in a match: press the key again as often as you like. A batch is refused only if it would push the game's object IDs to 30,000 (Status: Count/object limit).
- If the game is closed while **Enable** is still ticked, the table disables itself quietly. Cheat Engine shows no error and closes normally. Close and reopen Cheat Engine before you use the table with a new game.
- The editor's separate **Other** category (trees, rocks, resources, cliffs, doodads and the Jedi Holocron) is not included. Those are not Units, Buildings or Heroes in the editor.
- Spawned objects stay on the map if you disable the table.

## Troubleshooting

If Enable will not tick, or a summon does nothing, open **---Other--- → Diagnostics** and read **Status**:

| Status says | What to do |
|---|---|
| Manually attach CE to battlegrounds_x1.exe first. | Attach Cheat Engine to `battlegrounds_x1.exe`, then tick Enable again. |
| Offline single-player only. / Enter a single-player match first. | Start a disposable offline match, not a replay or multiplayer game. |
| Focus the game before summoning. | Click the game so it is in the foreground, then press the summon key. |
| Gaia list objects are placed for Gaia… | Set **Side** to **Gaia / slot 0**. |
| Disable the old Deity Zenith table and restart CE… / Older/unknown native core remains… | Untick Enable, then close both the game and Cheat Engine and start again with this table only. |
| Game reports paused… | Close the pause or menu dialog and resume the game. |
| Cheat Engine 7.5 or newer is required. | Use Cheat Engine 7.5 or later. |
| Unsupported DDRAW.dll… | Use the verified cnc-ddraw wrapper next to the exe, or remove an unknown `DDRAW.dll`. |
| Cursor/coordinates invalid | Put the mouse over the map, or enter valid tile X/Y values. |
| Count must be 1–25 | Pick a value from the **Count** dropdown. |
| Count/object limit | The batch would push object IDs to 30,000. Use a smaller Count, or start a fresh match. |
| Game closed or detached… | The game was closed while Enable was ticked. Close and reopen Cheat Engine, start the game, then attach and enable again. |

If Enable unticks itself after a refusal, tick it again to continue. Diagnostics is visible only while Enable is ticked.

## Credits

Deity Zenith Galactic Battlegrounds by **Bener Kaya**.
STAR WARS and STAR WARS Galactic Battlegrounds are trademarks of their respective owners. This is an unofficial fan-made table.
