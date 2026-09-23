# ULT's Loading Screen

A customizable, immersive loading screen for Foundry VTT that replaces the default
loading overlay with a simulated progress bar synchronized to real world loading.

- **Module ID:** `ult-ld`
- **Author:** 4isfate
- **License:** MIT
- **Compatibility:** Foundry VTT v13–v14 (verified on v14, build 368)

## Features

- Full-screen loading panel that covers most of the viewport without hiding everything
- Simulated progress bar that tracks real world loading and never runs ahead of it
- Bar is held at 90–99% until the world is genuinely ready, then completes to 100%
- Configurable minimum on-screen time (default 4 s) with a randomized maximum
- Stage text describing the current loading phase
- Rotating lore tips, in order or shuffled
- Custom background image, Font Awesome icon or custom image icon
- Nine configurable colours plus backdrop opacity, via native colour pickers
- Separate visibility toggles for the GM and for players
- Client-side simplified mode (no animation, blur, or glow) with a toolbox toggle
- Blocks all interaction with the rest of the UI while visible
- Conflict detection against other loading-screen modules
- English, Russian and German localization

## Installation

See `INSTALL-RU.md` for a step-by-step guide, or install from a manifest URL.

## API

```
game.modules.get("ult-ld").api.show()   // show the overlay again
game.modules.get("ult-ld").api.bump(75) // raise the progress ceiling
game.modules.get("ult-ld").api.ready()  // mark the world as ready
game.modules.get("ult-ld").api.instance // the active overlay, or null
```
