# Desktop Pet

Desktop Pet is a small macOS experiment inspired by Clippy. An animated character stays above other windows, can be dragged around the screen, and periodically shows a practical macOS tip.

The character artwork is original 3D work. The application was built as an experiment in using ChatGPT to help write a native desktop utility.

## What it does

- Plays a frame-by-frame idle animation in a transparent window
- Keeps the character visible above normal application windows
- Lets the user drag the character around the desktop
- Shows a dismissible tip every ten seconds
- Keeps the window inside the main display bounds

## Tech stack

| Area | Technology |
|---|---|
| Language | Python 3 |
| macOS bridge | PyObjC |
| Native interface | AppKit, Foundation, and Quartz |
| Artwork | PNG animation frames and layered character assets |

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
