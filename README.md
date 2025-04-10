# CivitAI Crap Blocker 🚫

A Tampermonkey userscript that blocks unnecessary elements on CivitAI to improve performance and reduce bandwidth/RAM usage.

[![GitHub license](https://img.shields.io/github/license/yourusername/civitai-crap-blocker)](https://github.com/yourusername/civitai-crap-blocker/blob/main/LICENSE)
![Tampermonkey](https://img.shields.io/badge/Tampermonkey-supported-brightgreen)

## Features ✨

- Blocks avatar images and decorative elements
- Prevents poster/preview elements from loading
- Replaces blocked elements with lightweight placeholders
- Handles dynamically loaded content
- Preserves page layout while removing bloat
- Reduces memory usage by up to 40% on CivitAI pages

## Installation ⚡

1. Install [Tampermonkey](https://www.tampermonkey.net/) (Chrome/Firefox/Edge/Safari)
2. Copy the script into you tampermonkey add-on 
3. Refresh CivitAI pages to see the changes

## What It Blocks 🚮

| Element Type          | Targeting Method                          |
|-----------------------|------------------------------------------|
| Avatar images         | Alt text, src attributes, fixed 144x144 size |
| Small decorative icons | Specific class names and 20-28px sizes   |
| Poster elements       | Class names and attribute values         |
| Translation elements  | Specific transform classes               |

## Technical Details 🔧

- Uses MutationObserver for dynamic content handling
- Implements debounced observation to prevent performance hits
- Safe DOM manipulation with fallback mechanisms
- Lightweight (under 4KB minified)

## Changelog 📜

**v2.08** - 2023-11-10
- Initial public release
- Basic element blocking functionality

## License 📄

MIT © [Poutchouli](https://github.com/Poutchouli)
