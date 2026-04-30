# 🐍 Snake Water Gun Game (Python)

A simple command-line game built using Python where you play **Snake-Water-Gun** against the computer.

---

## 🎮 Game Rules

* Snake 🐍 drinks Water 💧 → **Snake wins**
* Water 💧 douses Gun 🔫 → **Water wins**
* Gun 🔫 kills Snake 🐍 → **Gun wins**

---

## 🧠 Concept Used

* Python dictionaries (`dict`)
* Random number generation (`random`)
* Conditional statements (`if-else`)
* User input handling

---

## 📂 Code Overview

```python
import random

# 1 for snake, -1 for water, 0 for gun
computer = random.choice([0, -1, 1])

youstr = input("Enter the choice (s for snake, w for water, g for gun): ")

yourDict = {"s": 1, "w": -1, "g": 0}
reverseDict = {1: "Snake", -1: "Water", 0: "Gun"}

you = yourDict[youstr]

print(f"You chose {reverseDict[you]}\nComputer chose {reverseDict[computer]}")

if computer == you:
    print("It's a draw")
else:
    if computer == -1 and you == 1:
        print("You win!")
    elif computer == -1 and you == 0:
        print("Computer wins!")
    elif computer == 0 and you == -1:
        print("You win!")
    elif computer == 0 and you == 1:
        print("Computer wins!")
    elif computer == 1 and you == 0:
        print("Computer wins!")
    elif computer == 1 and you == -1:
        print("You win!")
    else:
        print("Invalid Input")
```

---

## ▶️ How to Run

1. Make sure Python is installed
2. Save the file as `game.py`
3. Run the program:

```bash
python game.py
```

---

## ⌨️ Input Format

| Input | Meaning  |
| ----- | -------- |
| `s`   | Snake 🐍 |
| `w`   | Water 💧 |
| `g`   | Gun 🔫   |

---

## 🧪 Example Run

```
Enter the choice: s
You chose Snake
Computer chose Water
You win!
```

---

## ⚠️ Limitations

* No input validation (wrong input may crash)
* Only single round gameplay
* Uses multiple `if-else` conditions (can be optimized)

---

## 🚀 Future Improvements

* Add score tracking 🧮
* Add multiple rounds 🔁
* Improve UI with emojis 🎨
* Optimize logic using mathematical approach
* Add exception handling for invalid input

---

## 📌 Author

**Ashish Dehariya**

---

## ⭐ If you like this project

Give it a star ⭐ on GitHub and share it!
