# CivitAI Crap Blocker 🚫

A Violentmonkey/Tampermonkey userscript that blocks unnecessary elements on CivitAI to improve performance and reduce bandwidth/RAM usage.

[![GitHub license](https://img.shields.io/github/license/Poutchouli/civitai-crap-blocker)](https://github.com/Poutchouli/civitai-crap-blocker/blob/main/LICENSE)

## Features ✨

- Blocks avatar images and badges (some users avatars and badges are +20mb to be displayed in 64x64p)
- Prevents image outlines/previews from loading
- Replaces blocked elements with lightweight placeholders
- Handles dynamically loaded content
- Preserves page layout while removing bloat
- Reduces memory usage by up to 40% on CivitAI pages

BEFORE:
![image](https://github.com/user-attachments/assets/28f7fe1d-4789-4906-869b-5b463c51c7e3)

AFTER:
![image](https://github.com/user-attachments/assets/73f47891-2f1d-40c3-b670-ead9fabcec8d)

WEBUSAGE (loading the front page)

BEFORE:
13sec load with 92mb
![image](https://github.com/user-attachments/assets/93dcfe71-757e-46f1-986e-04d0e5f7bb0c)

AFTER:
1.2sec load with 27mb
![image](https://github.com/user-attachments/assets/026183b3-bb92-4784-a2be-4c0cd827a3ef)

## Installation ⚡
Option1
1. Install [Violentmonkey](https://violentmonkey.github.io/) (Chrome/Firefox/Edge/Safari)
2. Create a new script
3. Copy the script into your new Violentmonkey script
4. Refresh CivitAI pages to see the changes

Option2
1. Install [Tampermonkey](https://www.tampermonkey.net/) (Chrome/Firefox/Edge/Safari)
2. Create a new script
3. Copy the script into your new tampermonkey script 
4. Refresh CivitAI pages to see the changes

## Need help to add the extension (Chrome) ?
Install from an Unpacked Folder (ZIP)
Download the Extension as a ZIP:
https://github.com/violentmonkey/violentmonkey/releases
![image](https://github.com/user-attachments/assets/91a99e02-0bb3-46bf-a3c5-1ce42f14e71f)
Extract the ZIP to a folder.
Load Unpacked Extension:
Go to chrome://extensions/ and enable Developer mode.
Drag and drop the zip file on your Chrome window

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

**v2.08** - 2025-04-10
- Initial public release
- Basic element blocking functionality

**v2.09** - 2025-04-15
- Fixed React hydration errors by avoiding DOM removal
- Now hides elements instead of deleting them (safer for React)
- Processes elements in batches for better performance
- Smarter MutationObserver that ignores unnecessary changes
- 2-second startup delay to prevent conflicts

## License 📄

MIT © [Poutchouli](https://github.com/Poutchouli)
