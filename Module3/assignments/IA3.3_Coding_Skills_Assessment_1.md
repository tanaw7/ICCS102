# ICCS 102 – Coding Skills Assessment 1

## Deck 1 Foundations: Variables, Strings, Numbers, Conditions, and Loops

This exercise set is designed to help you practice the core ideas from class lesson:

* variables,
* strings,
* numbers,
* arithmetic operations,
* type conversion,
* conditionals,
* `for` loops,
* `while` loops,
* and writing clean functions with type hints.

---

# General Rules Read Carefully

## Submission Rules

* Create **one Python file per exercise**.
* Use the exact file names shown for each exercise.
* Then put all individual exercise .py files together in a folder and zip the folder and submit the zipped file in this format **[FirstName]\_[leftmost\_three\_letters\_of\_your\_LastName].zip**. (e.g. "**Barnabas\_Smi.zip**")
* Each file must contain the required function, function name is given in each exercise.
* Write the exact function signature shown in the exercise.
* --- **IMPORTANT** **Type hints are required.** This means your function parameters and return type must include types.
* Do **not** use `import` unless explicitly stated. The purpose of the assignment is for you to write your own functions.
* Do **not** use `input()` unless explicitly stated.
* Do **not** `print()` unless explicitly stated.
  - You may however use `print()` statements for yourself just to see the result. But remove or comment them out when submitted.


## File Naming

Use the exact file names shown under each exercise.

Example:

```text
f01_greeting_message.py
f02_rectangle_area.py
```

## What is a Function Signature?

A function signature is the first line that defines the function.

It includes:

* the function name,
* the parameters or inputs,
* the input types,
* the return type.

Example:

```python
def greeting_message(name: str) -> str:
    ...
```

This means:

* the function name is `greeting_message`,
* it receives one input called `name`,
* `name` must be a `str`,
* the function returns a `str`.

Types matter because they make your program clearer and help other programmers understand what kind of data your function expects.

* To test your code and function
  - You can do the following:
  ```text
  print(greeting_message("Nick"))
  ```
  - Press Run button in your IDE and see the result in the console output.

---

# Topic A — Variables, Strings, and Number Manipulation Exercises 1–5

## Mini Lesson: Variables, Strings, and Numbers

A variable stores a value.

Examples:

```python
name = "Alice"
age = 19
price = 45.5
```

Strings are used for text.

Numbers can be used in arithmetic expressions.

Example:

```python
total = price * quantity
```

Functions should receive input through parameters and return the result.

## Mini Lesson: Types

Relevant types for this exercise: int, float, str, bool, list

```python
int    # Whole numbers such as -1, 0, 1, 2, 3, etc.
float  # Decimal numbers such as 1.1, 2.0, 3.73, etc.
str    # Text, such as "hello" or "Alice"
bool   # A logical value: True or False
list   # An ordered collection of values, such as [1, 2, 3]
```


---
.
.
.
# Exercises Start Here

## 1. Greeting Message

Problem: Return a greeting message in the exact format `Hello, <name>!`.

Function Name: `greeting_message`
Import: none

Function Signature:

```python
def greeting_message(name: str) -> str:
    ...
```

Inputs

* `name: str`

Output

* `str`

Example inputs and their outputs

* `greeting_message("Alice")` → `"Hello, Alice!"`
* `greeting_message("Nick")` → `"Hello, Nick!"`
* `greeting_message("Somchai")` → `"Hello, Somchai!"`

Requirement

* Use string concatenation or an f-string.
* Return the final message.

File: `f01_greeting_message.py`

---

- . ####################################################################
- .
- Exercises 02 - 15 are omitted at this stage until the assessment day.
- .
- . ####################################################################

---

# Topic B — Slightly More Advanced Exercises 6–10

## Mini Lesson: Combining Operations and Conditions

Programs often need more than one idea at the same time.

For example:

* calculate a value,
* compare it with a condition,
* return a message depending on the result.

Example:

```python
def is_adult(age: int) -> bool:
    more_than_eightteen = age >= 18 # the right hand side resolves to a boolean value (True/False)
    return more_than_eightteen
```

or in shorter form:

```python
def is_adult(age: int) -> bool:
    return age >= 18
```

These exercises combine variables, arithmetic, strings, and conditionals.

---

# Topic C — For Loops and While Loops Exercises 11–15

## Mini Lesson: Loops

A loop repeats code.

Use a `for` loop when you know how many times to repeat.

Example:

```python
for i in range(5):
    print(i)
```

Use a `while` loop when repetition depends on a condition.

Example:

```python
count = 1
while count <= 5:
    count += 1
```

In functions, loops are often used to build totals, count values, or build lists.

---
