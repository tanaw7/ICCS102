# ICCS 102 – Module 3 Assignments

# Assignment: Mini Interactive Python Program

## Assignment Type

Individual assignment

## Learning Objective

By completing this assignment, students should be able to:

* write a complete Python program using variables,
* receive user input using `input()`,
* display output using `print()`,
* use selection structures with `if`, `elif`, and `else`,
* use repetition structures with `for` or `while`,
* define and call functions to organize program logic,
* use parameters and return values in simple functions,
* combine multiple programming constructs to solve a small problem.

## Duration

Recommended working time: **90–120 minutes**

## Task Description

Create a small interactive Python program.

You may choose one of the following options:

1. Number Guessing Game
2. Rock-Paper-Scissors
3. Simple Quiz Game
4. Simple Calculator with Menu
5. Vending Machine Simulator
6. Simple Text Adventure
7. Food Order Price Calculator
8. Fitness Minutes Tracker
9. Movie Ticket Price Checker
10. Simple ATM Simulator
11. Temperature Converter and Weather Advice

Your program should interact with the user, make decisions, repeat at least one part of the program, and organize important logic into functions.

Your program should mainly use Python topics covered in class: variables, strings, numbers, input/output, `if / elif / else`, loops, and functions.

You may use simple standard Python libraries such as `random`, `math`, `time`, `datetime`, or `statistics` if they fit your program. Do not use external libraries that require installation.

## Minimum Program Requirements

Your Python program must include:

* at least **3 variables**,
* at least **1 input()** statement,
* at least **3 print()** statements,
* at least **1 if / elif / else structure**,
* at least **1 loop** using either `for` or `while`,
* at least **3 functions** defined using `def`,
* each function must be called at least **once** in the program,
* at least **2 functions** should receive parameters,
* at least **1 function** should return a value,
* functions should clearly show input types and output/return type, using type hints or comments,
* display functions may use `print()` if their purpose is to show information to the user,
* comments explaining important parts of the code.

## Function Requirement Guidance

Your functions should help organize your program.

They should not be fake functions that only print one word and do not help the program.

A good function has a clear purpose.

* A calculation or decision function should usually `return` a value or message.
* A display function may use `print()` if its purpose is to show information to the user.

Good examples of functions using type hints:

```python
def show_menu() -> None:
    # input: none
    # output/return type: None
    print("1. Add")
    print("2. Subtract")
    print("3. Exit")


def calculate_total(price: float, quantity: int) -> float:
    # input: price is float, quantity is int
    # output/return type: float
    return price * quantity


def check_budget(total: float, budget: float) -> bool:
    # input: total is float, budget is float
    # output/return type: bool
    return total <= budget
```

Your main program should call the functions.

Example:

```python
show_menu()

total = calculate_total(50.0, 2)
within_budget = check_budget(total, 120.0)

if within_budget:
    print("The purchase is within budget.")
else:
    print("The purchase is over budget.")
```

## Example Program Ideas

### Option 1: Number Guessing Game

The program stores a fixed secret number. The user guesses the number. The program tells the user whether the guess is correct, too high, or too low.

### Option 2: Rock-Paper-Scissors

The user chooses rock, paper, or scissors. The program compares the user choice with a fixed computer choice and displays the result.

### Option 3: Simple Quiz Game

The program asks several questions and keeps score. At the end, it displays the final score.

### Option 4: Simple Calculator with Menu

The program displays a menu such as:

1. Add
2. Subtract
3. Multiply
4. Divide
5. Exit

The user chooses an option, enters numbers, and receives the result.

### Option 5: Vending Machine Simulator

The program displays item choices and prices. The user selects an item and enters money. The program determines whether the purchase is successful.

### Option 6: Simple Text Adventure

The program gives the user choices in a short story. Different choices lead to different outcomes.

### Option 7: Food Order Price Calculator

The program shows a small menu of food items and prices. The user chooses items or quantities, and the program calculates the total price. The program can repeat until the user chooses to finish ordering.

### Option 8: Fitness Minutes Tracker

The program asks the user to enter exercise minutes for several days. It calculates the total minutes and gives a simple message such as `Good job`, `Keep going`, or `Needs more exercise`.

### Option 9: Movie Ticket Price Checker

The program asks for the user's age and student status, then calculates a ticket price using simple discount rules. The program may repeat for more than one customer.

### Option 10: Simple ATM Simulator

The program starts with a fixed account balance. The user can choose to check balance, deposit money, withdraw money, or exit. The program should not allow withdrawal if there is not enough money.

### Option 11: Temperature Converter and Weather Advice

The program converts Celsius to Fahrenheit and gives simple advice such as `cool`, `warm`, or `hot`. The program may repeat for several temperature values.

## Required Comment Block at the Top of the Code

At the top of your `.py` file, include a comment block like this:

```python
# ICCS102 Mini Interactive Python Program
# Student Name: Your Name Here
# Program Title: Your Program Title Here
# Short Description: Briefly explain what your program does.
```

## Submission Format

Submit your Python file as a **.py file**.

Submit only one Python file unless the instructor gives permission to submit more than one file.

## File Naming Format

For one Python file:

```text
ICCS102_Assignment_MiniProgram_[YourFirstName]_[threeLeftMostLettersOfLastName].py
```

Example:

```text
ICCS102_Assignment_MiniProgram_Somchai_Jai.py
```

## Rubrics

| Criteria                      | Excellent                                                                                                                                                                                              | Good                                                                                                                                                  | Satisfactory                                                                                                 | Not Acceptable                                              |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------- |
| Program correctness           | 3 pts: Program runs correctly and handles expected inputs well.                                                                                                                                        | 2 pts: Program mostly works with minor issues.                                                                                                        | 1 pt: Program runs but has significant logic issues.                                                         | 0 pts: Program does not run or is mostly incomplete.        |
| Use of Python constructs      | 3 pts: Correctly uses variables, input/output, conditionals, loops, and at least 3 called functions. Functions have reasonably clear input/output types, parameter use, and at least one return value. | 2 pts: Uses most required constructs correctly. Functions are present and called, but parameter use, return value, or type clarity could be stronger. | 1 pt: Uses some constructs but has errors, missing function calls, unclear types, or missing required parts. | 0 pts: Required constructs are mostly missing or incorrect. |
| Code readability and comments | 2 pts: Code is readable, well-named, and functions are used to make the program easier to understand. Includes helpful comments where useful.                                                          | 1.5 pts: Code is mostly readable, with some useful names, comments, or function organization.                                                         | 1 pt: Code is hard to follow, poorly organized, or has minimal comments.                                     | 0 pts: Code is unclear and lacks meaningful organization.   |
| Submission requirements       | 2 pts: Follows file naming, required comment block, and submission instructions.                                                                                                                       | 1.5 pts: Mostly follows submission instructions with minor issues.                                                                                    | 1 pt: Some submission requirements are missing.                                                              | 0 pts: Submission requirements are mostly missing.          |

---
