# New World — exploration prototype

A real-time 2D RPG foundation with a top-down tile perspective inspired by classic handheld adventure games. Original procedural pixel scenery; no game assets or dependencies required.

## Play

Open `index.html`, or visit https://jabadudi.github.io/New-World/ . Move with WASD, arrow keys, or the on-screen directional buttons. Press M or click the minimap to open the atlas. Water, mountain ridges, and the outer boundary block movement; woodland can be traversed. Paths connect the starting clearing to four discoverable landmarks.

## World and exploration

Each new world generates a seeded 192 × 192 tile landscape with water, banks, trails, meadows, woodland, and ridges. Terrain is deterministic for its seed. The camera follows a temporary explorer character. This is a finite exploration prototype; quests, NPCs, combat, creatures, and the final setting are not implemented yet.

The minimap reveals terrain within eight tiles as you walk. Discovered terrain remains visible permanently, including after you leave that area. The atlas shows all discovered terrain, a permanent tile-based history of your traveled route, discovered landmarks, the starting point, and your current position. It does not yet offer waypoint routing or a chronological replay.

The world seed, position, discovered terrain, and travel trail save automatically in browser local storage every two seconds and when you leave the page. Saves stay with this browser and site origin. If storage is blocked, a message explains that progress lasts only for the session. New World asks before replacing the current save. The previous terrain-painting prototype uses a separate storage key.

## Hosting

Plain HTML/CSS/JavaScript; no build step. GitHub Pages serves the repository root from main. Push changes to update it. Google Fonts is optional and falls back to system fonts offline.

## Verification

JavaScript syntax checked. A mocked browser runtime checks deterministic terrain generation, distinct seeds, reachable landmarks across four seeds, world bounds, movement, rendering calls, discovery and route persistence, save validation, and atlas toggling. Full visual browser verification was unavailable in the development environment.
