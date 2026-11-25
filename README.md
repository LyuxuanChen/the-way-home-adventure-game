# The Way Home

A single-player, story-driven puzzle adventure played in the terminal. Explore an abandoned laboratory, repair a time machine, and return to the past to prevent a disastrous experiment.

## About the game

Forty years after an experiment destroyed the Rewinder laboratory, an engineer returns to the ruins with a chance to save his wife. Recover clues, restore the machine, and decide how to confront the people behind the experiment.

The story has five endings shaped by your choices. Once you enter the past, travelling and taking major actions increase **FADE**. Reach 100 and your character disappears. FADE advances through actions, so you can take your time reading and solving puzzles.

## Features

- Connected puzzles involving levers, encoded clues, coordinates, and dialogue.
- Branching conversations and five possible endings.
- A notebook that keeps track of discovered clues.
- A turn-based FADE system that makes actions matter.
- A paginated terminal interface and a plain-text alternative.
- Offline play with no external assets or third-party Python packages.

The game was developed collaboratively across story writing, puzzle design, programming, and testing.

## Requirements

- Python 3.
- For `main.py`: macOS or Linux with Python's `curses` module and an interactive terminal at least **80 columns by 24 rows**.
- For a plain-text interface, including on Windows: use `arbsize.py`, which does not require `curses`.

## Getting started

Clone the repository and open its folder:

```bash
git clone https://github.com/LyuxuanChen/the-way-home-adventure-game.git
cd the-way-home-adventure-game
```

### macOS and Linux

Launch the terminal interface:

```bash
python3 main.py
```

If the game asks you to resize the terminal, enlarge the window to at least 80 × 24. Use a terminal that supports interactive input, such as Terminal, a Linux terminal emulator, or the VS Code integrated terminal.

### Plain-text interface

For an interface without `curses` or the fixed terminal layout:

```bash
python3 arbsize.py
```

On Windows, use the Python launcher:

```powershell
py arbsize.py
```

If your Python installation uses `python` instead of `python3` or `py`, use that command instead. Both game interfaces use only the Python standard library.

## Controls

| Input | Action |
| --- | --- |
| Menu number, then Enter | Choose an action |
| Enter | Continue the story or advance a page |
| Q, then Enter | Quit at an answer prompt |
| R, then Enter | Restart when an ending offers the option |
| Ctrl-C | Exit the game |

In the terminal interface, Q also exits immediately on a pagination page. Read the notebook whenever you need to revisit a clue. Reading, hints, and incorrect puzzle answers do not increase FADE.

## Project files

| File | Purpose |
| --- | --- |
| `main.py` | Game with the paginated `curses` terminal interface |
| `arbsize.py` | Game with a standard text interface |
| `README_CHOICES_AND_ENDINGS.md` | Puzzle solutions, branching choices, and ending routes; contains spoilers |

## Troubleshooting and limitations

- **Terminal is too small:** enlarge the window to at least 80 × 24, or run `arbsize.py`.
- **`curses` is unavailable:** run `arbsize.py` for the plain-text interface.
- **Interactive-terminal message:** run `main.py` directly in a terminal. Redirected input and output are not supported by this interface.
- **Progress is lost after quitting:** there is no save/load system. Each new game starts from the beginning.
- **Answer input:** the `main.py` interface accepts printable ASCII characters, which cover the game's required answers.

For puzzle help and a full ending guide, see [Choices and endings](README_CHOICES_AND_ENDINGS.md). This guide contains spoilers.
