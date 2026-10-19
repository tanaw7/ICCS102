# Team Assignment 3.4 (TA3.4) — Coding Assessment Practice

## Assignment Type

Group coding practice — **10 points**

## Task

Complete the five exercises in your assigned group. Each exercise requires a function that receives input through its parameters and returns a result.

For **each exercise**:

1. Spend **at least five minutes working individually before any group discussion**. Every member should read the question and attempt their own code. If you finish early, test your solution and wait until the five minutes are over before helping others.
2. Compare your approaches. Discuss what was unclear, explain any mistakes, and agree on a working solution. Make sure every member has a chance to speak and ask questions.
3. Test the group's solution with all the supplied examples and at least one additional valid input.
4. Answer the three discussion questions as Python comments at the top of that exercise's file. Brief, specific answers are enough.

Rotate who types the group's final code and comments across the exercises. Do not divide the exercises among members: everyone must attempt every exercise first.

You may use the class materials and the hints below. Do not use AI assistance or copy solutions from another group or the internet.

## Discussion Comments

Copy this template to the top of **each** exercise file and replace the placeholders between [ and ]. Use `#` comments, not a separate document.

```python
# Group: [group name or number]
# Members present: [first and last names]
# Exercise: [number and title]
#
# 1. What did your group discuss before agreeing on the final solution?
# Answer: [brief answer]
#
# 2. What was the biggest difficulty in understanding this exercise,
#    and how did your group resolve it?
# Answer: [brief answer; if there was no difficulty, say so]
#
# 3. By the end of the individual work period, how many members had a
#    working solution that passed all supplied examples without help?
# Answer: [number] out of [number of members present]
```

For Question 3, using the supplied hints and class materials still counts as working independently. Report the count before group discussion, not after corrections. An unfinished or untested attempt does not count as a verified working solution. A low count does **not** reduce your score; answer honestly so the instructor can identify where more practice is needed.

## Submission Rules

* The appointed coordinator must submit **one set of five Python files per group**, using the exact filenames specified.
* Include the completed discussion comments at the top of each file.
* Use Python 3.9 or later for the `list[int]` type annotation.
* Each file must contain the required function with the **exact function signature shown**, including parameter type hints and the return type.
* Do not use `import` or `input()`.
* Return the result. Do not use `print()` inside the required functions.
* You may use `print()` outside the functions to test your work. Remove or comment out these test statements before submitting.
* You may assume that inputs have the stated types and satisfy the conditions in each exercise. You do not need to handle invalid inputs.
* Put all five Python files into one folder and compress it into a ZIP file. One group member submits the ZIP to Google Classroom on behalf of the group. No PDF or separate reflection document is required.

ZIP filename:

```text
ICCS102_TA3.4_Group[Number].zip
```

Example:

```text
ICCS102_TA3.4_Group1.zip
```

Replace `[Number]` with your assigned group number. Do not include the square brackets.

## Testing Your Functions

After writing a function, call it with the example inputs and check its returned result.

For example:

```python
print(item_label("Notebook", 3))
```

The expected output is:

```text
3 x Notebook
```

Your function must work for other valid inputs as well, not only the examples shown.

---

## 1. Item Label

**Individual attempt first:** Allow at least five minutes for every member to attempt this exercise independently before discussing it. After discussion and testing, answer all three discussion questions as `#` comments at the top of this exercise\'s Python file.

Problem: Return an item label in the exact format `<quantity> x <item>`.

Include one space on each side of the lowercase letter `x`.

Function Name: `item_label`  
Import: none

Function Signature:

```python
def item_label(item: str, quantity: int) -> str:
    ...
```

Inputs

* `item: str` — an item name without leading or trailing spaces.
* `quantity: int` — a nonnegative integer.

Output

* `str`

Example inputs and their outputs

* `item_label("Notebook", 3)` → `"3 x Notebook"`
* `item_label("Pen", 1)` → `"1 x Pen"`
* `item_label("Water bottle", 12)` → `"12 x Water bottle"`
* `item_label("Pencil", 0)` → `"0 x Pencil"`

Requirements

* Keep the item name's original capitalization.
* Return the completed label.

### Hint

You can use an f-string to combine text and numbers:

```python
name = "Alice"
age = 19
message = f"{name} is {age}"
```

Alternatively, use `str()` to convert a number to text before joining it to other strings.

File: `f01_item_label.py`

---

## 2. Delivery Fee

**Individual attempt first:** Allow at least five minutes for every member to attempt this exercise independently before discussing it. After discussion and testing, answer all three discussion questions as `#` comments at the top of this exercise\'s Python file.

Problem: Return the delivery fee based on the order total.

* If the total is below 300 baht, the delivery fee is `40.0` baht.
* If the total is at least 300 baht, the delivery fee is `0.0` baht.

Return only the delivery fee, not the order total plus the fee.

Function Name: `delivery_fee`  
Import: none

Function Signature:

```python
def delivery_fee(total: float) -> float:
    ...
```

Inputs

* `total: float` — a nonnegative order total in baht.

Output

* `float`

Example inputs and their outputs

* `delivery_fee(250.0)` → `40.0`
* `delivery_fee(299.5)` → `40.0`
* `delivery_fee(300.0)` → `0.0`
* `delivery_fee(500.0)` → `0.0`
* `delivery_fee(0.0)` → `40.0`

Requirements

* Return the correct delivery fee.

### Hint

An `if` and `else` statement can choose between two results. Pay attention to what should happen when the total is exactly 300 baht.

File: `f02_delivery_fee.py`

---

## 3. Count the Letter A

**Individual attempt first:** Allow at least five minutes for every member to attempt this exercise independently before discussing it. After discussion and testing, answer all three discussion questions as `#` comments at the top of this exercise\'s Python file.

Problem: Return the number of times the letter `a` appears in the supplied text. Count both uppercase `A` and lowercase `a`. Ignore all other characters.

Function Name: `count_a`  
Import: none

Function Signature:

```python
def count_a(text: str) -> int:
    ...
```

Inputs

* `text: str` — any text, including an empty string.

Output

* `int`

Example inputs and their outputs

* `count_a("Banana")` → `3`
* `count_a("APPLE")` → `1`
* `count_a("A cat and a dog")` → `4`
* `count_a("Python")` → `0`
* `count_a("")` → `0`

Requirements

* Count uppercase and lowercase versions of the letter equally.
* Return the count.

### Hint

Use `.lower()` to create a lowercase version of a string:

```python
word = "HELLO"
lowercase_word = word.lower()
```

Here, `lowercase_word` contains `"hello"`.

You can use a `for` loop to examine each character and a counter starting at zero to keep track of matches.

File: `f03_count_a.py`

---

## 4. Count Up

**Individual attempt first:** Allow at least five minutes for every member to attempt this exercise independently before discussing it. After discussion and testing, answer all three discussion questions as `#` comments at the top of this exercise\'s Python file.

Problem: Return a list of integers counting up from `1` to `n`, including both `1` and `n`.

Function Name: `count_up`  
Import: none

Function Signature:

```python
def count_up(n: int) -> list[int]:
    ...
```

Inputs

* `n: int` — an integer greater than or equal to `1`.

Output

* `list[int]`

Example inputs and their outputs

* `count_up(4)` → `[1, 2, 3, 4]`
* `count_up(2)` → `[1, 2]`
* `count_up(1)` → `[1]`
* `count_up(6)` → `[1, 2, 3, 4, 5, 6]`

Requirements

* Return the numbers in ascending order.
* Return a list, not a string containing the numbers.

### Hint

Start with an empty list:

```python
numbers = []
```

Use `.append()` to add a value to the end of a list:

```python
numbers.append(7)
```

You can use a `while` loop to add successive numbers. Remember to update the number inside the loop so that the loop eventually stops.

File: `f04_count_up.py`

---

## 5. Sum of Even Numbers

**Individual attempt first:** Allow at least five minutes for every member to attempt this exercise independently before discussing it. After discussion and testing, answer all three discussion questions as `#` comments at the top of this exercise\'s Python file.

Problem: Return the sum of all even integers from `1` to `n`. Include `n` if it is even. If there are no even integers in the range, return `0`.

Function Name: `sum_even_to_n`  
Import: none

Function Signature:

```python
def sum_even_to_n(n: int) -> int:
    ...
```

Inputs

* `n: int` — an integer greater than or equal to `1`.

Output

* `int`

Example inputs and their outputs

* `sum_even_to_n(6)` → `12`
* `sum_even_to_n(7)` → `12`
* `sum_even_to_n(10)` → `30`
* `sum_even_to_n(2)` → `2`
* `sum_even_to_n(1)` → `0`

Requirements

* Return the sum as an integer, not a list of even numbers.

### Hint

You can use a `for` loop to go through the numbers and an `if` statement to check which ones are even.

The expression `number % 2` gives the remainder after division by 2. An even number has a remainder of zero.

Keep a running total starting at zero. Remember that the stopping value in `range()` is excluded.

File: `f05_sum_even_to_n.py`

---

## Rubric — 10 Points

Each exercise is worth **1 point**. There is **no partial credit**.

| Result | Points | Criteria |
|---|---:|---|
| Correct | 2 | The required function has the exact signature, including all parameter type hints and the return type annotation, and returns the correct values in the required type and format for all grading test cases. |
| Not correct | 0 | The function fails any grading test case, is missing, cannot run, uses an incorrect signature, or is missing any required parameter type hint or return type annotation. |

Printing the expected answer without returning it is **not correct**.

The examples are provided for practice. Grading may include other inputs that follow the stated conditions.

The hints suggest possible approaches. Your solution is graded on its required signature and returned results, not on whether you follow a hint's approach.


The discussion comments are required but carry no separate points. The correctness score remains based on the function signature and returned results. Your group's reported difficulties and independent-success count do not affect that score.
