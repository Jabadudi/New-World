# New World — Heaven & Earth

A browser RPG exploration foundation with a permanent home dimension and seeded overworlds. Plain HTML/CSS/JavaScript; no build required.

## Play

https://jabadudi.github.io/New-World/

- WASD / arrows / touch directional buttons: real-time movement.
- H or **Teleport home**: instantly leave an expedition for your separate home in heaven. There is no cooldown or cost.
- **Return to exploration** at home: return to the same seed and exact coordinates you left, with discovery and traveled route intact.
- **Explore a new world** at home: generate a new seed and teleport to a random safe point on its connected path network. Existing worlds stay in your world list.
- Select an older world and **Visit selected world** to resume that world's saved position.
- M or the minimap: view the current dimension's atlas. Overworld maps remember revealed terrain, landmarks, and the trail of visited tiles. The home map shows the whole island.

First-time players begin on the home island. The sanctuary, glowing gate, spring, and gardens are scenery in this prototype. Use the sidebar travel buttons to travel; no proximity to the gate is required. Buildings do not yet have interiors. Story, NPCs, enemies, combat, and base construction are future work.

## Saving

Home position, active dimension, world seeds, exact expedition positions, discovered tiles, and visited trails persist in local browser storage. Autosaves occur every two seconds, on dimension travel, and when leaving the page. Old v2 exploration saves migrate automatically and become available through Return to exploration. Each seed reconstructs its own deterministic 192 × 192 landscape. Previously visited worlds remain available. Storage is limited by the browser; if full or blocked, an in-game message reports that the session cannot be saved. Saves are local to the browser and site, without account sync.

## Hosting and verification

GitHub Pages serves main at the repository root. Versioned asset URLs refresh the replacement scripts and stylesheet. The loading overlay displays a runtime error if the world cannot initialize.

Checked JavaScript syntax, rendered both dimensions with an actual Canvas implementation, and inspected the resulting images. Automated runtime checks cover safe spawns, movement, deterministic terrain, dimension switching, exact return coordinates, preserved home position, multiple archived worlds, per-world map/trail retention, reloading in either dimension, and v2 save migration. Browser layout and input verification remain unconfirmed because browser preview access was blocked.
