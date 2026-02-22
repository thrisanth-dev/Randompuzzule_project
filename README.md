# 🎮 Random Puzzle Game

A command-line Python puzzle game featuring multiple logic-based challenges, user input validation, time-based scoring, and a persistent leaderboard system.

> 🧑‍💻 Developed during my Python Programming Internship at **InternForte** (May 2024 – June 2024)

---

## 📸 Demo

```
╔══════════════════════════════════════════════════╗
║          🎮  RANDOM PUZZLE GAME  🎮              ║
║                                                  ║
║   Test your wits with Riddles, Math, Words &     ║
║   Number Guessing challenges!                    ║
╚══════════════════════════════════════════════════╝

Enter your name: Alex
Welcome, Alex! Let's see how smart you are... 🧠

──────────────────────────────────────────────────
  ROUND 1 of 5    |    Current Score: 0 pts
──────────────────────────────────────────────────

🔢 Math Puzzle  [Difficulty: MEDIUM]

📐 Problem:
  What is 23 × 7?

Attempts remaining: 3
Your answer: 161
✅ Correct! The answer is 161.
```

---

## ✨ Features

| Feature | Description |
|---|---|
| 🧩 **4 Puzzle Types** | Riddles, Math Challenges, Word Scramble, Number Guessing |
| 🎲 **Random Selection** | Each round picks a puzzle type and question at random |
| ✅ **Input Validation** | All user inputs are validated with helpful error messages |
| 💡 **Hint System** | Request hints with a 10-point penalty per hint |
| ⏱️ **Time Bonus** | Answer quickly (< 15 seconds) to earn bonus points |
| 🏆 **Leaderboard** | Top 10 scores saved locally and displayed after each game |
| 🎖️ **Player Ranking** | Earn a rank (Genius, Excellent, Good Job, etc.) based on performance |

---

## 📁 Project Structure

```
random_puzzle_game/
│
├── game.py                  # Main entry point
│
├── puzzles/
│   ├── __init__.py
│   ├── base_puzzle.py       # Abstract base class for all puzzles
│   ├── riddles.py           # Riddle puzzle (8 riddles)
│   ├── math_puzzle.py       # Arithmetic challenges (3 difficulty levels)
│   ├── word_scramble.py     # Unscramble programming vocabulary words
│   └── number_guess.py      # Binary-search-style number guessing
│
├── utils/
│   ├── __init__.py
│   ├── score_tracker.py     # Score calculation & JSON leaderboard
│   └── display.py           # All UI/display functions
│
├── data/
│   └── scores.json          # Auto-generated leaderboard (top 10)
│
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.7 or higher
- No external libraries needed — uses the Python standard library only!

### Installation & Run

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/random-puzzle-game.git
cd random-puzzle-game

# 2. Run the game
python game.py
```

---

## 🎯 How to Play

1. Enter your name when prompted.
2. Play **5 rounds** — each round is a randomly selected puzzle.
3. You have **3 attempts** per puzzle (6 for Number Guess).
4. Type `y` when prompted to use a hint (costs 10 pts).
5. Your score is calculated based on:
   - ✅ Correct answer: **+100 base points**
   - 💡 Each hint used: **-10 points**
   - ⏱️ Fast answer (<15 sec): **+bonus points**
6. Your final score is saved to the leaderboard!

---

## 🧠 Puzzle Types

### 🧩 Riddles
Classic brain-teaser riddles. Type your answer as a single word or phrase.

### 🔢 Math Puzzle
Arithmetic problems with three difficulty levels:
- **Easy**: Addition/subtraction up to 20
- **Medium**: Multiplication and larger numbers
- **Hard**: Powers and larger multiplication

### 🔤 Word Scramble
Unscramble programming-related vocabulary words. Great for building Python vocabulary!

### 🎯 Number Guess
Guess a number between 1–100 in 6 attempts. The game narrows the range after each guess.

---

## 📊 Scoring System

| Condition | Points |
|---|---|
| Correct answer | +100 |
| Each hint used | -10 |
| Answer in < 15 seconds | +bonus (up to +30) |
| Wrong answer | 0 |
| Minimum per correct | 10 |

### 🏅 Rank Tiers
| Score % | Rank |
|---|---|
| 90%+ | 🏆 GENIUS |
| 70–89% | 🥇 EXCELLENT |
| 50–69% | 🥈 GOOD JOB |
| 30–49% | 🥉 KEEP TRYING |
| < 30% | 📚 NEEDS PRACTICE |

---

## 🛠️ Concepts Used

- **Object-Oriented Programming** — Base class with inheritance for each puzzle type
- **Randomization** — `random` module for puzzle/question selection and word scrambling
- **File I/O** — JSON-based persistent leaderboard storage
- **Input Validation** — Type checking and error handling for all user inputs
- **Modular Design** — Separated into `puzzles/` and `utils/` packages
- **Time Tracking** — `time` module for bonus scoring

---

## 🤝 Contributing

Pull requests are welcome! Feel free to:
- Add new puzzle types
- Expand the riddle or word lists
- Add difficulty selection at game start
- Add a timer countdown display
---

## 👤 Author

**Your Name**  
🔗 [GitHub](https://github.com/YOUR_USERNAME) | [LinkedIn](https://linkedin.com/in/YOUR_PROFILE)

> *Built as part of the InternForte Python Programming Internship — May 2024 to June 2024*
