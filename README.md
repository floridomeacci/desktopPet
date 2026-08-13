# Desktop Pet

<p align="center">
  <img src="https://github.com/floridomeacci/Desktop-Pet/assets/28354552/673af905-4979-4dc1-85be-83965a8d1ec2" alt="Desktop Pet" width="200">
</p>

Desktop Pet is a small macOS experiment inspired by Clippy. An animated character stays above other windows, can be dragged around the screen, and periodically shows a practical macOS tip.

The character artwork is original 3D work. The application was built as an experiment in using ChatGPT to help write a native desktop utility.

## What it does

- Plays a frame-by-frame idle animation in a transparent window
- Keeps the character visible above normal application windows
- Lets the user drag the character around the desktop
- Shows a dismissible tip every ten seconds
- Keeps the window inside the main display bounds

## Screenshots

### Starting position

![Desktop Pet in its starting position](https://github.com/floridomeacci/Desktop-Pet/assets/28354552/605b1548-c748-438b-9e6b-89e3666dd479)

### Dragging the pet

![Desktop Pet being dragged](https://github.com/floridomeacci/Desktop-Pet/assets/28354552/73004ea0-36c6-4a3e-8965-d105f628e979)

### Tip popup

![Desktop Pet showing a tip](https://github.com/floridomeacci/Desktop-Pet/assets/28354552/80d7014e-77f1-4d23-9859-7fe30a409e0e)

## Tech stack

| Area | Technology |
|---|---|
| Language | Python 3 |
| macOS bridge | PyObjC |
| Native interface | AppKit, Foundation, and Quartz |
| Artwork | PNG animation frames and layered character assets |

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)

[![Tech stack: Python](https://skillicons.dev/icons?i=py)](https://skillicons.dev)

This project is macOS-only because it uses native Cocoa APIs.

## Run locally

You need macOS, Python 3, and the Xcode Command Line Tools.

```bash
git clone https://github.com/floridomeacci/desktopPet.git
cd desktopPet
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install pyobjc
python main.py
```

Run the last command from the repository root so the application can find `images/idle_ani`.

Stop the pet from the terminal with `Control-C`.

## Project structure

```text
main.py       Window behavior, animation, dragging, and timers
popup.py      Native tip window and close action
messages.py   Tip copy
images/       Character artwork and animation frames
```

Project page: [github.com/floridomeacci/desktopPet](https://github.com/floridomeacci/desktopPet)

## Support

[![Buy Me A Coffee](https://img.shields.io/badge/Buy_Me_A_Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/floridomeacci)
