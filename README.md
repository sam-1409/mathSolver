# ✋🧠 Gesture-Based Math Solver using OpenCV and MediaPipe

This project is a **real-time hand gesture-based calculator** that lets users input and evaluate mathematical expressions using only hand gestures. Designed for accessibility, and computer vision practice, it translates hand signs into digits, operators, and commands.

---

## 🚀 Features

- Real-time gesture detection using webcam
- Supports multi-digit input (e.g., showing 2 → 4 → 7 becomes "247")
- Gesture-controlled arithmetic operations (`+`, `-`, `*`, `/`)
- Built-in evaluation and result display
- Hands-free **Clear**, **DELETE** and **Exit** commands
- Works using a standard webcam (no special hardware needed)

---

## 🧠 Tech Stack

| Tool        | Purpose                             |
|-------------|-------------------------------------|
| Python      | Core programming language           |
| OpenCV      | Video capture, frame rendering      |
| MediaPipe   | Hand landmark detection (21 points) |
| NumPy       | Distance computation, math logic    |

---

## ✋ Supported Gestures

| Gesture                             | Function        |
|-------------------------------------|-----------------|
| 1–5 fingers (one hand)              | Digits 1–5      |
| 5 + 1-4 fingers(both hands)         | Digits 6-9      |
| Only one hand with 0 fingers        | Digit 0         |
| 1 finger on both hands              | `+` (add)       |
| 1 + 2 fingers                       | `-` (subtract)  |
| 1 + 3 fingers                       | `*` (multiply)  |
| 1 + 4 fingers                       | `/` (divide)    |
| Both hands with 0 fingers           | `=` (evaluate)  |
| Both hands with 5 fingers           | `Clear` input   |
| Both hands 2 fingers                | `Delete` input  |
| Right index < left index (spatial)  | Exit program    |

> Gestures are detected based on hand landmark positions and finger states.

---

## 📦 Installation

```bash
git clone https://github.com/sam-1409/mathSolver.git
cd mathSolver
pip install -r requirements.txt
