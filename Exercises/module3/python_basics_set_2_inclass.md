# ICCS 102 – Exercise Set

## Python Basics Part 2: Tuples, Sets, Dictionaries, Classes, Nested Loops, and Matrices

This exercise set is designed to help you practice the main ideas from Python Basics Part 2:

* tuples,
* sets,
* dictionaries,
* classes,
* nested loops,
* matrices,
* and writing clear Python functions with type hints.

---

# General Rules Read Carefully

## Assignment Type

Individual in-class coding exercise

You must do all exercises.

This is your own individual work.

## No AI assistance allowed

You may **not** use:

* ChatGPT
* Gemini
* Claude
* Grok
* any other AI tool

Failure to comply with this rule would result in 0 point for this exercise. Further disciplinary actions may be considered.

## What you may use

You may refer to:

* the **Python Basics Part 2** slides
* your own notes
* normal Google search for Python syntax and usage

You may use Google for syntax help, but not AI-generated answers.

## Submission Rules

* Create one Python file per exercise.
* Use the exact file names shown for each exercise.
* Put all `.py` files into one folder.
* Zip that folder and submit it in this format:

`[FirstName]_[leftmost_three_letters_of_your_LastName].zip`

Example:

`Barnabas_Smi.zip`

* Each file must contain the required function or class shown in the exercise.
* You may create helper functions if needed, but the required function or class must still exist.
* Use the correct function signature format you have already learned.
* You are expected to identify suitable input data types and output data types.
* Type hints are required for functions.
* Do not use `import` unless explicitly stated.
* Do not use `input()` unless explicitly stated.
* Do not `print()` unless explicitly stated.

  * You may use `print()` for your own testing, but remove or comment it out before submission.

## File Naming

Use the exact file names shown under each exercise.

Example:

```
f01_point_message.py
f02_unique_numbers.py
```

# Relevant Types for This Exercise Set

Relevant types for this exercise set:

`int`, `str`, `bool`, `list`, `tuple`, `set`, `dict`

You are expected to infer suitable parameter types and return types from the problem statement and the examples.

This means you should decide the correct input data types and output data types yourself, then write them using the proper function signature format.

Examples:

```
int               # whole numbers such as 1, 2, 3
str               # text such as "Alice"
bool              # True or False
list[int]         # a list of integers
list[str]         # a list of strings
list[list[int]]   # a matrix of integers
tuple[int, int]   # a fixed pair of integers
set[int]          # a set of unique integers
dict[str, int]    # keys are strings, values are integers
```

Hints:

* use a `tuple` for fixed grouped values such as a point `(x, y)`
* use a `set` when only unique values matter
* use a `dict` for key-value lookup or counting
* use `list[list[int]]` for a matrix with rows and columns
* use a `class` when related data belongs together as one custom object

---

# Exercises Start Here

## 1. Point Message

Problem: Return a message in the exact format `Point: (<x>, <y>)`.

Function Name: `point_message`
Import: none

Example inputs and their outputs

* `point_message((3, 5))` → `"Point: (3, 5)"`
* `point_message((0, 0))` → `"Point: (0, 0)"`
* `point_message((-2, 7))` → `"Point: (-2, 7)"`

Requirement

* Use the tuple values in the correct order.
* Return the final message.

File: `f01_point_message.py`

---

## 2. Unique Numbers

Problem: Return a set containing only the unique values from the input list.

Function Name: `unique_numbers`
Import: none

Example inputs and their outputs

* `unique_numbers([1, 2, 2, 3])` → `{1, 2, 3}`
* `unique_numbers([5, 5, 5])` → `{5}`
* `unique_numbers([4, 1, 4, 2, 1])` → `{1, 2, 4}` or `{4, 1, 2}`

Requirement

* Return a set.
* Duplicate values must appear only once in the result.

File: `f02_unique_numbers.py`

---

## 3. Product Price Lookup

Problem: Return the price of a product by its name. If the product does not exist, return `-1`.

Function Name: `get_price`
Import: none

Example inputs and their outputs

* `get_price({"water": 10, "coffee": 45}, "water")` → `10`
* `get_price({"water": 10, "coffee": 45}, "coffee")` → `45`
* `get_price({"water": 10, "coffee": 45}, "tea")` → `-1`

Requirement

* Look up the product by key.
* Return `-1` if the key is not found.

File: `f03_get_price.py`

---

## 4. Word Frequency

Problem: Count how many times each word appears and return the result as a dictionary.

Function Name: `word_frequency`
Import: none

Example inputs and their outputs

* `word_frequency(["apple", "banana", "apple"])` → `{"apple": 2, "banana": 1}`
* `word_frequency(["cat", "cat", "cat"])` → `{"cat": 3}`
* `word_frequency([])` → `{}`

Requirement

* Use a dictionary.
* Each word should be a key.
* Each count should be the value for that key.

File: `f04_word_frequency.py`

---

## 5. Student Class

Problem: Create a class named `Student` with attributes `name` and `score`.

Also write a function that receives a `Student` object and returns a message in the exact format:

`<name> scored <score>`

Class Name: `Student`
Function Name: `student_summary`
Import: none

Required Code Structure:

```
class Student:
    def __init__(self, ...):
        ...

def student_summary(student) -> ...:
    ...
```

Example usage and output

* `student1 = Student("Alice", 92)`
* `student_summary(student1)` → `"Alice scored 92"`

Requirement

* The class must be named `Student`.
* The object must store `name` and `score`.
* The function must return the summary message.

File: `f05_student_class.py`

---

## 6. Rectangle Pattern

Problem: Return a rectangle pattern made of `*` using the given number of rows and columns.

Return the whole pattern as one string.

Function Name: `rectangle_pattern`
Import: none

Example inputs and their outputs

* `rectangle_pattern(2, 3)` →

```text
***
***
```

* `rectangle_pattern(3, 4)` →

```text
****
****
****
```

Requirement

* Use nested loops.
* Return one string containing the whole pattern.
* Each row should be on a new line.

File: `f06_rectangle_pattern.py`

---

## 7. Matrix Values

Problem: Return all values in the matrix in row-by-row order as a single list.

Function Name: `matrix_values`
Import: none

Example inputs and their outputs

* `matrix_values([[1, 2], [3, 4]])` → `[1, 2, 3, 4]`
* `matrix_values([[5, 6, 7]])` → `[5, 6, 7]`
* `matrix_values([[1], [2], [3]])` → `[1, 2, 3]`

Requirement

* Use nested loops or equivalent row-by-row traversal.
* Visit values from left to right, top to bottom.
* Return the final list.

File: `f07_matrix_values.py`

---

## 8. Matrix Sum

Problem: Return the total sum of all values in the matrix.

Function Name: `sum_matrix`
Import: none

Example inputs and their outputs

* `sum_matrix([[1, 2], [3, 4]])` → `10`
* `sum_matrix([[5, 5, 5]])` → `15`
* `sum_matrix([[1], [2], [3]])` → `6`

Requirement

* Use nested loops or equivalent row-by-row traversal.
* Add every value into a running total.
* Return the final sum.

File: `f08_sum_matrix.py`

---

# Final Reminder

These exercises are meant to help you practice the lesson clearly and directly.

Keep your solutions simple, readable, and correct.
