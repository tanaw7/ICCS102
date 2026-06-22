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

You must do all exercises. This is individual work.

## Tools rules

You may **not** use:

* Google search, 
* ChatGPT, Gemini, Claude, Grok, or any other AI tool

## What you may use

You may refer to:

* the **Python Basics Part 2** slides
* your own notes
* Official python documentation at [https://docs.python.org/3/tutorial/datastructures.html](https://docs.python.org/3/tutorial/datastructures.html#)

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
* Do not use `import`, `input()`, `print()`  unless explicitly stated. 

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

## 4. Top Student

Problem: Given a dictionary of student names and scores, return the name of the student with the highest score.

Function Name: `top_student`
Import: none

Example inputs and their outputs

* `top_student({"Alice": 92, "Bob": 85, "Cara": 95})` → `"Cara"`
* `top_student({"Dan": 70, "Eve": 88})` → `"Eve"`
* `top_student({"Mina": 100})` → `"Mina"`

Requirement

* Use a dictionary.
* Compare the scores in the dictionary.
* Return the name with the highest score.
* You may assume the dictionary is not empty.
* You may assume there is only one highest score.

File: `f04_top_student.py`

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

def student_summary(student: Student) -> ...:
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

## 6. Menu Combinations

Problem: A meal can be formed by choosing one main dish and one drink. Return all possible combinations as a list of strings in the exact format `<main> - <drink>`.

Function Name: `menu_combinations`
Import: none

Example inputs and their outputs

* `menu_combinations(["Rice", "Noodles"], ["Tea", "Water"])` → `["Rice - Tea", "Rice - Water", "Noodles - Tea", "Noodles - Water"]`
* `menu_combinations(["Burger"], ["Juice", "Soda"])` → `["Burger - Juice", "Burger - Soda"]`
* `menu_combinations([], ["Tea"])` → `[]`

Requirement

* Use nested loops.
* Combine every main dish with every drink.
* Return the final list in the correct order.
* If either input list is empty, return an empty list.

File: `f06_menu_combinations.py`

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

## 8. Find Target in Matrix

Problem: A matrix stores numbers. If a row contains the value `0` anywhere, that whole row is considered void and must be ignored.

Return `True` if the target number appears in any non-void row. Otherwise, return `False`.

Function Name: `find_target_in_matrix`
Import: none

Example inputs and their outputs

* `find_target_in_matrix([[1, 0], [3, 2]], 2)` → `True`
* `find_target_in_matrix([[5, 0], [1, 2]], 5)` → `False`
* `find_target_in_matrix([[1, 2], [0, 4]], 4)` → `False`
* `find_target_in_matrix([[1, 2, 3, 4], [5, 0, 7, 11], [9, 10, 11, 12], [13, 14, 15, 16]], 11)` → `True`

Requirement

* Use nested loops or equivalent row-by-row traversal.
* If a row contains `0` anywhere, ignore that whole row.
* A target inside a void row does not count.
* Stop searching as soon as the target is found in a non-void row.
* Return `True` or `False`.

Hint

* Think about how `continue` can skip a void row, and how `break` (or an immediate `return`) can stop your search early once the target is found.

File: `f08_find_target_in_matrix.py`

---

# Final Reminder

These exercises are meant to help you practice the lesson clearly and directly.

Keep your solutions simple, readable, and correct.
