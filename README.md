# Python Number Guessing Game

A simple yet engaging console-based number guessing game built with Python. This project demonstrates fundamental Python programming concepts and provides an interactive gaming experience.

## 🎮 Game Overview

The Number Guessing Game challenges players to guess a randomly generated number between 1 and 100. Players have 10 attempts to correctly identify the number, with helpful hints provided after each guess.

## ✨ Features

- **Random Number Generation**: Uses Python's `random` module to generate unpredictable numbers
- **User Input Validation**: Robust error handling for invalid inputs
- **Attempt Tracking**: Keeps count of attempts with a maximum limit of 10
- **Smart Hints**: Provides "too high" or "too low" feedback after each guess
- **Play Again Functionality**: Option to restart the game after completion
- **User-Friendly Interface**: Clear instructions and emoji-based feedback
- **Error Handling**: Graceful handling of invalid inputs and edge cases

## 🛠️ Technologies Used

- **Python 3.x**: Core programming language
- **random module**: For generating random numbers
- **Built-in functions**: `input()`, `print()`, `int()`, `str()`
- **Control structures**: `if-elif-else`, `while` loops, `for` loops
- **Exception handling**: `try-except` blocks

## 🚀 How to Run

### Prerequisites
- Python 3.x installed on your system
- Basic understanding of command line/terminal

### Installation & Execution
1. **Navigate to the project directory**:
   ```bash
   cd PROJECTS/FRONT_END/projects
   ```

2. **Run the game**:
   ```bash
   python python_number_guessing_game.py
   ```

3. **Follow the on-screen instructions** to play the game

## 🎯 How to Play

1. **Start the Game**: Run the Python script
2. **Read Instructions**: The game will explain the rules
3. **Make Your Guess**: Enter a number between 1 and 100
4. **Get Feedback**: The game will tell you if your guess is too high or too low
5. **Keep Guessing**: You have 10 attempts to find the correct number
6. **Win or Lose**: Either guess correctly or run out of attempts
7. **Play Again**: Choose to start a new game or exit

## 📋 Code Structure

### Main Functions

#### `number_guessing_game()`
- Core game logic
- Handles user input and validation
- Provides feedback and tracks attempts
- Returns `True` if player wins, `False` if they lose

#### `play_again()`
- Asks user if they want to play another round
- Handles user input validation for yes/no responses
- Returns `True` to continue, `False` to exit

#### `main()`
- Main game loop
- Orchestrates the overall game flow
- Handles the play again functionality

### Key Features Explained

#### Random Number Generation
```python
secret_number = random.randint(1, 100)
```
- Generates a random integer between 1 and 100 (inclusive)

#### Input Validation
```python
try:
    guess = int(input(f"Attempt {attempts + 1}/{max_attempts}: Enter your guess: "))
    if guess < 1 or guess > 100:
        print("❌ Please enter a number between 1 and 100!")
        continue
except ValueError:
    print("❌ Please enter a valid number!")
    continue
```
- Ensures input is a valid integer
- Checks if the number is within the valid range
- Provides clear error messages

#### Smart Feedback System
```python
if guess == secret_number:
    print(f"🎉 Congratulations! You guessed it in {attempts} attempts!")
elif guess < secret_number:
    print("📈 Too low! Try a higher number.")
else:
    print("📉 Too high! Try a lower number.")
```
- Provides specific feedback based on the guess
- Uses emojis for better user experience

## 🎨 User Interface Features

- **Emoji Feedback**: Visual indicators for different game states
- **Clear Instructions**: Step-by-step guidance for players
- **Progress Tracking**: Shows current attempt number and remaining attempts
- **Colorful Output**: Uses emojis and formatting for better readability
- **Error Messages**: Helpful feedback for invalid inputs

## 🔧 Customization Options

### Easy Modifications

#### Change the Number Range
```python
# Modify these lines in the number_guessing_game() function
secret_number = random.randint(1, 100)  # Change 100 to any number
if guess < 1 or guess > 100:  # Update this condition too
```

#### Adjust Maximum Attempts
```python
# Change this line in the number_guessing_game() function
max_attempts = 10  # Modify to any number you prefer
```

#### Add Difficulty Levels
```python
# You could add difficulty selection
difficulty = input("Choose difficulty (easy/medium/hard): ")
if difficulty == "easy":
    max_attempts = 15
    max_number = 50
elif difficulty == "medium":
    max_attempts = 10
    max_number = 100
else:  # hard
    max_attempts = 7
    max_number = 200
```

## 🧪 Testing the Game

### Test Cases to Try
1. **Valid Inputs**: Numbers between 1-100
2. **Invalid Inputs**: Letters, symbols, negative numbers
3. **Boundary Values**: 1, 100, 0, 101
4. **Game Flow**: Win scenarios, lose scenarios
5. **Play Again**: Yes/no responses with various inputs

### Sample Game Session
```
🎮 Welcome to Number Guessing Game! 🎮
========================================
I'm thinking of a number between 1 and 100.
You have 10 attempts to guess it!
----------------------------------------
Attempt 1/10: Enter your guess: 50
📉 Too high! Try a lower number.
Attempts remaining: 9
------------------------------
Attempt 2/10: Enter your guess: 25
📈 Too low! Try a higher number.
Attempts remaining: 8
------------------------------
Attempt 3/10: Enter your guess: 37
🎉 Congratulations! You guessed it in 3 attempts!
The number was 37

Would you like to play again? (yes/no): no
👋 Thanks for playing! Goodbye!
```

## 📚 Learning Objectives

This project helps you learn:
- **Python Basics**: Variables, data types, operators
- **Control Flow**: Conditional statements and loops
- **Functions**: Defining and calling functions
- **User Input**: Getting and validating user input
- **Error Handling**: Using try-except blocks
- **Random Numbers**: Working with the random module
- **Program Structure**: Organizing code into logical functions
- **User Experience**: Creating intuitive interfaces

## 🔗 Related Links

- **GitHub Repository**: [View Code](https://github.com/ASTA91-GIT/portfolio/blob/main/projects/python_number_guessing_game.py)
- **All Projects**: [Portfolio Projects](https://github.com/ASTA91-GIT/portfolio/tree/main/projects)
- **Main Portfolio**: [ASTA Portfolio](https://asta91-git.github.io/portfolio)

## 🤝 Contributing

Feel free to:
- Report bugs or suggest improvements
- Add new features like difficulty levels
- Improve the user interface
- Add sound effects or graphics
- Create variations of the game

## 📄 License

This project is part of the ASTA Portfolio and is available under the MIT License.

---

**Happy Gaming! 🎮**

*This project showcases fundamental Python programming concepts while providing an enjoyable gaming experience.*
