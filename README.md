# Gesture-Based Math Solver (OpenCV + MediaPipe)

This project is a **real-time hand gesture-based calculator** that lets you build and evaluate basic math expressions using only hand gestures in front of a webcam.

---

## Features

- Real-time gesture detection using a webcam
- Supports multi-digit input (e.g., 2 → 4 → 7 becomes `247`)
- Gesture-controlled arithmetic operations (`+`, `-`, `*`, `/`)
- Built-in evaluation and result display
- Hands-free **Clear**, **Delete**, and **Exit** gestures

---

## Requirements

- Python 3
- A working webcam

---

## Installation

If you cloned this repo:

```bash
git clone https://github.com/sam-1409/mathSolver.git
cd mathSolver
pip install -r requirements.txt
```

If you already have the files locally, run:

```bash
pip install -r requirements.txt
```

---

## Run

```bash
python mathSolver.py
```

Keyboard shortcuts:

- `q` / `Esc`: quit
- `c`: clear

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| OpenCV | Video capture + rendering |
| MediaPipe | Hand landmark detection (21 points) |
| NumPy | Distance computation + math helpers |

---

## Supported Gestures

| Gesture | Function |
|---|---|
| One hand showing 0–5 fingers | Append digit `0`–`5` |
| Two hands: one hand `5` + other hand `1`–`4` | Append digit `6`–`9` |
| Two hands: `1` + `1` | Append `+` |
| Two hands: `1` + `2` (either order) | Append `-` |
| Two hands: `1` + `3` (either order) | Append `*` |
| Two hands: `1` + `4` (either order) | Append `/` |
| Two hands: `0` + `0` | Evaluate (`=`) |
| Two hands: `5` + `5` | Clear |
| Two hands: `2` + `2` | Delete last character |
| Two hands: `1` + `1` with index fingertips very close | Exit |

Notes:

- Gestures are based on MediaPipe landmarks and simple finger-state rules.
- The app uses a debounce delay (currently ~1.25s) to avoid repeated inputs; adjust `delay` in `mathSolver.py` if needed.

---

## Troubleshooting

- **Webcam not opening**: close other apps using the camera, or try changing the camera index in `cv.VideoCapture(0)`.
- **Laggy / missed gestures**: improve lighting, keep hands fully in frame, or reduce `delay`.

---

## Contributing

See `CONTRIBUTING.md` for setup and guidelines.

---

## License

This project is licensed under the **Creative Commons Attribution–NonCommercial 4.0 International License**.
To learn more, see https://creativecommons.org/licenses/by-nc/4.0/.

---

## Credits

- Original author: @youngcoder45
