# Contributing

Thanks for considering contributing!

## Quick start (local setup)

### Prerequisites

- Python 3
- A working webcam

### Install dependencies

```bash
pip install opencv-python mediapipe numpy
```

### Run the app

```bash
python mathSolver.py
```

While running:

- `q` / `Esc` quits
- `c` clears

## Making changes

- Keep changes small and focused.
- Prefer readable, straightforward code over cleverness.
- Match the existing style (simple functions, minimal structure).

### Useful places to tweak

- Input debounce: update `delay` in `mathSolver.py` to make gesture entry faster/slower.
- Exit gesture sensitivity: the exit condition uses the distance between both index fingertips.

## Pull request checklist

- App runs locally without errors.
- README stays accurate (gestures/controls/requirements).
- No unrelated formatting-only changes.

## Reporting issues

If you open an issue, please include:

- OS + Python version
- Dependency versions (`pip show mediapipe opencv-python numpy`)
- What you expected vs what happened
- Any error output (stack trace) if applicable
