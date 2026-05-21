# ICCS 102 – Exercise Set

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
* Then put them together in a folder and zip it and submit the file in this format **[FirstName]\_[leftmost\_three\_letters\_of\_your\_LastName].zip**. (e.g. "**Barnabas\_Smi.zip**")
* Each file must contain the required function, function name is given in each exercise.
* You may create helper functions if needed, but the required function must still exist.
* Write the exact function signature shown in the exercise.
* **Type hints are required.** This means your function parameters and return type must include types.
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

## 2. Full Name Formatter

Problem: Return a full name in the exact format `<first_name> <last_name>`.

Function Name: `full_name`
Import: none

Function Signature:

```python
def full_name(first_name: str, last_name: str) -> str:
    ...
```

Inputs

* `first_name: str`
* `last_name: str`

Output

* `str`

Example inputs and their outputs

* `full_name("Alice", "Wong")` → `"Alice Wong"`
* `full_name("Somchai", "Jaidee")` → `"Somchai Jaidee"`
* `full_name("John", "Smith")` → `"John Smith"`

Requirement

* Combine the two strings with exactly one space between them.
* Return the full name.

File: `f02_full_name.py`

---

## 3. Rectangle Area

Problem: Calculate and return the area of a rectangle using `width * height`.

Function Name: `rectangle_area`
Import: none

Function Signature:

```python
def rectangle_area(width: float, height: float) -> float:
    ...
```

Inputs

* `width: float`
* `height: float`

Output

* `float`

Example inputs and their outputs

* `rectangle_area(5, 3)` → `15`
* `rectangle_area(2.5, 4)` → `10.0`
* `rectangle_area(7.2, 2)` → `14.4`

Requirement

* Use multiplication.
* Return the calculated area.

File: `f03_rectangle_area.py`

---

## 4. Total Price

Problem: Calculate and return the total price using `price * quantity`.

Function Name: `total_price`
Import: none

Function Signature:

```python
def total_price(price: float, quantity: int) -> float:
    ...
```

Inputs

* `price: float`
* `quantity: int`

Output

* `float`

Example inputs and their outputs

* `total_price(25.0, 3)` → `75.0`
* `total_price(49.5, 2)` → `99.0`
* `total_price(10.25, 4)` → `41.0`

Requirement

* Use multiplication.
* Return the total price as a number.

File: `f04_total_price.py`

---

## 5. Minutes to Seconds

Problem: Convert minutes into seconds using `minutes * 60`.

Function Name: `minutes_to_seconds`
Import: none

Function Signature:

```python
def minutes_to_seconds(minutes: int) -> int:
    ...
```

Inputs

* `minutes: int`

Output

* `int`

Example inputs and their outputs

* `minutes_to_seconds(1)` → `60`
* `minutes_to_seconds(5)` → `300`
* `minutes_to_seconds(0)` → `0`

Requirement

* Use multiplication.
* Return the number of seconds.

File: `f05_minutes_to_seconds.py`

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
    return age >= 18
```

These exercises combine variables, arithmetic, strings, and conditionals.

---

## 6. Even or Odd

Problem: Return `"Even"` if the number is even, otherwise return `"Odd"`.

Function Name: `even_or_odd`
Import: none

Function Signature:

```python
def even_or_odd(number: int) -> str:
    ...
```

Inputs

* `number: int`

Output

* `str`

Example inputs and their outputs

* `even_or_odd(4)` → `"Even"`
* `even_or_odd(7)` → `"Odd"`
* `even_or_odd(0)` → `"Even"`
* `even_or_odd(-3)` → `"Odd"`

Requirement

* Use the modulus operator `%`.
* Use an `if` statement.

File: `f06_even_or_odd.py`

---

## 7. Grade Category

Problem: Return a grade category based on the score. Assume the score is an integer from `0` to `100`.

Function Name: `grade_category`
Import: none

Function Signature:

```python
def grade_category(score: int) -> str:
    ...
```

Inputs

* `score: int`

Output

* `str`

Grade rules

* `score >= 90` → `"A"`
* `score >= 80` and `< 90` → `"B"`
* `score >= 70` and `< 80` → `"C"`
* `score < 70` → `"Needs Improvement"`

Example inputs and their outputs

* `grade_category(95)` → `"A"`
* `grade_category(90)` → `"A"`
* `grade_category(82)` → `"B"`
* `grade_category(75)` → `"C"`
* `grade_category(60)` → `"Needs Improvement"`

Requirement

* Use `if`, `elif`, and `else`.

File: `f07_grade_category.py`

---

## 8. Simple Discount

Problem: Apply a 10% discount if the total price is at least 500 baht. Assume `total >= 0`.

Function Name: `discounted_price`
Import: none

Function Signature:

```python
def discounted_price(total: float) -> float:
    ...
```

Inputs

* `total: float`

Output

* `float`

Discount rule

* If `total >= 500`, return `total * 0.9`.
* Otherwise, return `total` unchanged.

Example inputs and their outputs

* `discounted_price(1000)` → `900.0`
* `discounted_price(500)` → `450.0`
* `discounted_price(300)` → `300`
* `discounted_price(750.5)` → `675.45`

Requirement

* Use an `if` statement.
* Use arithmetic operations.

File: `f08_discounted_price.py`

---

## 9. Password Strength Basic

Problem: Return `"Strong enough"` if the password has at least 8 characters. Otherwise, return `"Too short"`.

Function Name: `password_strength`
Import: none

Function Signature:

```python
def password_strength(password: str) -> str:
    ...
```

Inputs

* `password: str`

Output

* `str`

Example inputs and their outputs

* `password_strength("abcd")` → `"Too short"`
* `password_strength("password123")` → `"Strong enough"`
* `password_strength("12345678")` → `"Strong enough"`
* `password_strength("1234567")` → `"Too short"`

Requirement

* Use `len()`.
* Use an `if` statement.

File: `f09_password_strength.py`

---

## 10. Temperature Advice

Problem: Return advice based on the temperature.

Function Name: `temperature_advice`
Import: none

Function Signature:

```python
def temperature_advice(temperature: float) -> str:
    ...
```

Inputs

* `temperature: float`

Output

* `str`

Advice rules

* `temperature >= 35` → `"Very hot, drink water"`
* `temperature >= 25` and `< 35` → `"Warm weather"`
* `temperature < 25` → `"Cool weather"`

Example inputs and their outputs

* `temperature_advice(36)` → `"Very hot, drink water"`
* `temperature_advice(35)` → `"Very hot, drink water"`
* `temperature_advice(30)` → `"Warm weather"`
* `temperature_advice(25)` → `"Warm weather"`
* `temperature_advice(20)` → `"Cool weather"`

Requirement

* Use `if`, `elif`, and `else`.

File: `f10_temperature_advice.py`

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

## 11. Sum from 1 to N

Problem: Return the sum of numbers from `1` to `n`, including both `1` and `n`. Assume `n >= 1`.

Function Name: `sum_to_n`
Import: none

Function Signature:

```python
def sum_to_n(n: int) -> int:
    ...
```

Inputs

* `n: int`

Output

* `int`

Example inputs and their outputs

* `sum_to_n(5)` → `15`
* `sum_to_n(10)` → `55`
* `sum_to_n(1)` → `1`

Requirement

* Use a `for` loop.
* Use a variable to store the running total.
* Do not use the built-in `sum()` function.

File: `f11_sum_to_n.py`

---

## 12. Count Down

Problem: Return a list of numbers counting down from `n` to `1`, including both `n` and `1`. Assume `n >= 1`.

Function Name: `count_down`
Import: none

Function Signature:

```python
def count_down(n: int) -> list[int]:
    ...
```

Inputs

* `n: int`

Output

* `list[int]`

Example inputs and their outputs

* `count_down(5)` → `[5, 4, 3, 2, 1]`
* `count_down(3)` → `[3, 2, 1]`
* `count_down(1)` → `[1]`

Requirement

* Use a `while` loop.
* Return the list.

File: `f12_count_down.py`

---

## 13. Count Vowels

Problem: Count how many vowels are in a word. Count only `a`, `e`, `i`, `o`, and `u`. Do not count `y` as a vowel.

Function Name: `count_vowels`
Import: none

Function Signature:

```python
def count_vowels(word: str) -> int:
    ...
```

Inputs

* `word: str`

Output

* `int`

Example inputs and their outputs

* `count_vowels("apple")` → `2`
* `count_vowels("banana")` → `3`
* `count_vowels("sky")` → `0`
* `count_vowels("AEIOU")` → `5`

Requirement

* Use a `for` loop.
* Treat uppercase and lowercase letters the same.
* Use `.lower()` to handle uppercase letters.

File: `f13_count_vowels.py`

---

## 14. First Multiple of Seven

Problem: Starting from `start`, return the first integer greater than or equal to `start` that is divisible by `7`. Assume `start >= 1`.

Function Name: `first_multiple_of_seven`
Import: none

Function Signature:

```python
def first_multiple_of_seven(start: int) -> int:
    ...
```

Inputs

* `start: int`

Output

* `int`

Example inputs and their outputs

* `first_multiple_of_seven(10)` → `14`
* `first_multiple_of_seven(21)` → `21`
* `first_multiple_of_seven(22)` → `28`
* `first_multiple_of_seven(1)` → `7`

Requirement

* Use a `while` loop.
* Use the modulus operator `%`.

File: `f14_first_multiple_of_seven.py`

---

## 15. Build Even Numbers List

Problem: Return a list of even numbers from `1` to `n` in ascending order. Include `n` if `n` is even. Assume `n >= 1`.

Function Name: `even_numbers_up_to`
Import: none

Function Signature:

```python
def even_numbers_up_to(n: int) -> list[int]:
    ...
```

Inputs

* `n: int`

Output

* `list[int]`

Example inputs and their outputs

* `even_numbers_up_to(10)` → `[2, 4, 6, 8, 10]`
* `even_numbers_up_to(7)` → `[2, 4, 6]`
* `even_numbers_up_to(1)` → `[]`
* `even_numbers_up_to(2)` → `[2]`

Requirement

* Use a `for` loop.
* Use an `if` statement.
* Use `%` to check whether a number is even.

File: `f15_even_numbers_up_to.py`

