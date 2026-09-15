# BOO# BOO // Wicker House

A small playable browser prototype for the BOO cooperative horror concept.

## Run

Install Node.js 20 or newer, then run:

```powershell
npm install
npm start
```

The Electron wrapper is the intended desktop build. Opening `index.html` directly still works for quick browser iteration.

## Steam build

Create the Windows build with:

```powershell
npm run dist:win
```

This produces a portable x64 executable in `dist/`. Upload that executable as a Windows depot in SteamPipe and set it as the launch target. The wrapper disables Node access inside the game page and loads the game from local files, so it does not depend on a web server at runtime.

Steamworks features such as lobbies, achievements, cloud saves, and matchmaking should be added behind a separate Steamworks bridge after the core co-op networking layer is chosen. The current build is Steam-compatible as a desktop game, but does not claim Steam achievements or multiplayer services yet.

## Controls

- `WASD` moves through the house
- `E` takes nearby valuables or records nearby evidence
- `F` toggles the flashlight
- `R` resets the run

The current mission asks for `$900` in valuables and three evidence records before returning to the glowing front door. The house becomes active after 30 seconds or when noise gets high.
