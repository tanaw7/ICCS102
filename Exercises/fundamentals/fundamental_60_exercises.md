# Fundamental exercises&#x20;

## General Rules (Read Carefully)


- **DO ALL THE 60 EXERCISES!**
- Create **one file per exercise**. Use the exact given file names for each exercise (see below, e.g. ex01\_rectangle\_area.py).
- Then put them together in a folder and zip it and submit the file in this format **[FirstName]\_[leftmost\_three\_letters\_of\_your\_LastName].zip**. (e.g. "**Barnabas\_Smi.zip**")
- Each file should contain **the required function** (and optional helper functions if needed).
  - [Meaning if you need to create more function in order for your required function to work, you can do so. Ask yourself whether your approach is efficient though].
- Write correct function signatures. This is very important. You already are given input(s) types and expected output type (return).
- Do **not** use `import` unless explicitly stated. The purpose of the assignment is for you to write your own functions.
- Do **not** use `input()` unless explicitly stated.
- Do **not** print unless explicitly stated.
  - You may however use `print()` statements for yourself just to see the result. But remove or comment them out when submitted.
- Use the **exact Function Name** shown\*\*\*

---

**What is a function signature?**

A **function signature** is the first line that defines the function.\
It includes:

- the function name
- the parameters (inputs)
- the return type (output type)

Example:

```
def rectangle_area(width: float, height: float) -> float:
    ...

```

- `rectangle_area` is the function name
- `width` and `height` are inputs
- `-> float` means it returns a number (a float)

---

## Topic A — Types & Basic Expressions (Exercises 1–10)

### Mini Lesson: What are “types”?

A **type** is the kind of data a value is.

- `int` = whole numbers (e.g., `3`, `-10`)
- `float` = decimals (e.g., `3.14`, `-0.5`)
- `str` = text (e.g., `"hello"`)
- `bool` = `True` or `False`

Types matter because Python behaves differently depending on the type. For example, `3 + 4` does math, but `"3" + "4"` joins text into `"34"`.

---

### 1. Add Two Integers

Problem: Return the sum of two integers.

Function Name: `add_two` Import: none

Inputs

- `a: int`
- `b: int`

Output

- `int`  # sum of a and b

Hint

- Use `a + b`.

Example Inputs (to test)

- `add_two(3, 5)` → `8`
- `add_two(-2, 10)` → `8`

File: `f01_add_two.py`

### 2. Minutes to Seconds

Problem: Convert minutes to seconds.

Function Name: `minutes_to_seconds` Import: none

Inputs

- `minutes: int`

Output

- `int`  # number of seconds

Hint

- 1 minute = 60 seconds.

Example Inputs (to test)

- `minutes_to_seconds(2)` → `120`
- `minutes_to_seconds(0)` → `0`

File: `f02_minutes_to_seconds.py`

### 3. Average of Two Floats

Problem: Return the average of two numbers.

Function Name: `average_two` Import: none

Inputs

- `a: float`
- `b: float`

Output

- `float`  # (a + b) / 2

Example Inputs (to test)

- `average_two(2.0, 4.0)` → `3.0`
- `average_two(1.5, 2.5)` → `2.0`

File: `f03_average_two.py`

### 4. Greeting Text

Problem: Return a greeting in this exact format: `"Hello, <name>!"`

Function Name: `greet` Import: none

Inputs

- `name: str`

Output

- `str`  # greeting string

Example Inputs (to test)

- `greet("Mina")` → `"Hello, Mina!"`
- `greet("")` → `"Hello, !"`

File: `f04_greet.py`

### 5. String Length

Problem: Return the number of characters in the string.

Function Name: `string_length` Import: none

Inputs

- `s: str`

Output

- `int`  # number of characters

Example Inputs (to test)

- `string_length("abc")` → `3`
- `string_length("")` → `0`

File: `f05_string_length.py`

### 6. Is Positive

Problem: Return True if the number is positive (> 0), otherwise False.

Function Name: `is_positive` Import: none

Inputs

- `n: int`

Output

- `bool`  # True if n > 0

Example Inputs (to test)

- `is_positive(5)` → `True`
- `is_positive(0)` → `False`

File: `f06_is_positive.py`

### 7. Percent to Decimal

Problem: Convert a percent number into a decimal.

- Example: 25 means 25% and becomes 0.25

Function Name: `percent_to_decimal` Import: none

Inputs

- `percent: float`  # percent form, like 25 for 25%

Output

- `float`  # decimal form

Example Inputs (to test)

- `percent_to_decimal(25.0)` → `0.25`
- `percent_to_decimal(5.0)` → `0.05`

File: `f07_percent_to_decimal.py`

### 8. Decimal to Percent

Problem: Convert a decimal into a percent number.

- Example: 0.25 becomes 25

Function Name: `decimal_to_percent` Import: none

Inputs

- `decimal: float`  # decimal form, like 0.25

Output

- `float`  # percent form

Example Inputs (to test)

- `decimal_to_percent(0.25)` → `25.0`
- `decimal_to_percent(0.05)` → `5.0`

File: `f08_decimal_to_percent.py`

### 9. Quotient and Remainder

Problem: Return both the quotient and remainder when `a` is divided by `b`.

Function Name: `divmod_pair` Import: none

Inputs

- `a: int`
- `b: int`  # assume b > 0

Output

- `tuple[int, int]`  # (a // b, a % b)

Example Inputs (to test)

- `divmod_pair(17, 5)` → `(3, 2)`
- `divmod_pair(10, 2)` → `(5, 0)`

File: `f09_divmod_pair.py`

### 10. Degrees to Radians (Use math.pi)

Problem: Convert degrees to radians using: `radians = degrees * pi / 180`

Function Name: `degrees_to_radians` Import: `import math` (use `math.pi`)

Inputs

- `degrees: float`

Output

- `float`  # radians

Example Inputs (to test)

- `degrees_to_radians(180.0)` → `3.14159...`
- `degrees_to_radians(90.0)` → `1.57079...`

File: `f10_degrees_to_radians.py`

---

## Topic B — Conditions (if / elif / else) (Exercises 11–20)

### Mini Lesson: How conditions work

An `if` checks a condition that is **True** or **False**.

- If True → that block runs.
- If False → it skips.

Use `elif` for another condition, and `else` for “none of the above”.

---

### 11. Is Odd

Problem: Return True if `n` is odd, otherwise False.

Function Name: `is_odd` Import: none

Inputs

- `n: int`

Output

- `bool`  # True if n is odd

Hint

- Odd numbers have remainder 1 when divided by 2.

Example Inputs (to test)

- `is_odd(7)` → `True`
- `is_odd(6)` → `False`

File: `f11_is_odd.py`

### 12. Compare Two Numbers

Problem: Return:

- `"greater"` if a > b
- `"less"` if a < b
- `"equal"` if a == b

Function Name: `compare_two` Import: none

Inputs

- `a: float`
- `b: float`

Output

- `str`  # "greater", "less", or "equal"

Example Inputs (to test)

- `compare_two(5, 2)` → `"greater"`
- `compare_two(3, 3)` → `"equal"`

File: `f12_compare_two.py`

### 13. Bigger of Two

Problem: Return the bigger number. If they are equal, return either one.

Function Name: `bigger` Import: none

Inputs

- `a: float`
- `b: float`

Output

- `float`  # the larger value

Example Inputs (to test)

- `bigger(3, 10)` → `10`
- `bigger(5, 5)` → `5`

File: `f13_bigger.py`

### 14. Letter Grade

Problem: Convert a score into a letter grade using these rules:

- 80–100: A
- 70–79: B
- 60–69: C
- 50–59: D
- 0–49: F

Function Name: `grade_letter` Import: none

Inputs

- `score: int`

Output

- `str`  # "A", "B", "C", "D", or "F"

Example Inputs (to test)

- `grade_letter(83)` → `"A"`
- `grade_letter(49)` → `"F"`

File: `f14_grade_letter.py`

### 15. Between (Inclusive)

Problem: Return True if `x` is between `low` and `high` (inclusive), otherwise False.

Function Name: `between_inclusive` Import: none

Inputs

- `x: float`
- `low: float`
- `high: float`

Output

- `bool`  # True if low <= x <= high

Example Inputs (to test)

- `between_inclusive(5, 0, 10)` → `True`
- `between_inclusive(-1, 0, 10)` → `False`

File: `f15_between_inclusive.py`

### 16. Ticket Price

Problem: Return the ticket price based on age:

- age < 12: 50
- 12–59: 100
- 60+: 70

Function Name: `ticket_price` Import: none

Inputs

- `age: int`

Output

- `int`  # ticket price

Example Inputs (to test)

- `ticket_price(10)` → `50`
- `ticket_price(60)` → `70`

File: `f16_ticket_price.py`

### 17. Safe Division

Problem: Return `a / b`. If `b == 0`, return `None`.

Function Name: `safe_divide` Import: none

Inputs

- `a: float`
- `b: float`

Output

- `float | None`  # result, or None if dividing by zero

Example Inputs (to test)

- `safe_divide(10, 2)` → `5.0`
- `safe_divide(10, 0)` → `None`

File: `f17_safe_divide.py`

### 18. Is Vowel

Problem: Return True if `ch` is a vowel (a, e, i, o, u), case-insensitive.

Function Name: `is_vowel` Import: none

Inputs

- `ch: str`  # assume length 1

Output

- `bool`  # True if vowel

Example Inputs (to test)

- `is_vowel("A")` → `True`
- `is_vowel("b")` → `False`

File: `f18_is_vowel.py`

### 19. Median of Three Integers

Problem: Return the middle value (median) of three integers.

- Example: (1, 9, 3) → 3

Function Name: `median_of_three` Import: none

Inputs

- `a: int`
- `b: int`
- `c: int`

Output

- `int`  # median value

Hint

- One easy approach: put them in a list, sort it, return the middle.

Example Inputs (to test)

- `median_of_three(1, 9, 3)` → `3`
- `median_of_three(5, 5, 1)` → `5`

File: `f19_median_of_three.py`

### 20. Sign of Number

Problem: Return:

- `"positive"` if n > 0
- `"negative"` if n < 0
- `"zero"` if n == 0

Function Name: `sign` Import: none

Inputs

- `n: int`

Output

- `str`  # "positive", "negative", or "zero"

Example Inputs (to test)

- `sign(5)` → `"positive"`
- `sign(0)` → `"zero"`

File: `f20_sign.py`

---

## Topic C — For Loops (Exercises 21–30)

### Mini Lesson: How `for x in [1,3,2,5]` works

A `for` loop takes items **one by one** from a list, then stops **after the last item**. Example list `[1, 3, 2, 5]` → x becomes: `1`, then `3`, then `2`, then `5`, then stop.

---

### 21. Sum of a List

Problem: Return the sum of all numbers in the list.

Function Name: `sum_list` Import: none

Inputs

- `nums: list[int]`

Output

- `int`  # sum of all items

Example Inputs (to test)

- `sum_list([1, 3, 2, 5])` → `11`
- `sum_list([])` → `0`

File: `f21_sum_list.py`

### 22. Count Greater Than

Problem: Count how many numbers in the list are **greater than** `threshold`.

Function Name: `count_greater_than` Import: none

Inputs

- `nums: list[int]`
- `threshold: int`

Output

- `int`  # how many values are > threshold

Example Inputs (to test)

- `count_greater_than([1, 5, 7, 2, 7], 4)` → `3`
- `count_greater_than([], 10)` → `0`

File: `f22_count_greater_than.py`

### 23. First Divisible by k

Problem: Return the first number in the list that is divisible by `k`.

- If no number is divisible by k, return `None`.

Function Name: `first_divisible` Import: none

Inputs

- `nums: list[int]`
- `k: int`

Output

- `int | None`  # first divisible number, or None

Example Inputs (to test)

- `first_divisible([5, 7, 9, 10], 3)` → `9`
- `first_divisible([5, 7], 2)` → `None`

File: `f23_first_divisible.py`

### 24. Count Consonants

Problem: Count consonant letters in the string (a–z), case-insensitive.

- Vowels are a, e, i, o, u
- Ignore spaces and non-letters

Function Name: `count_consonants` Import: none

Inputs

- `s: str`

Output

- `int`  # number of consonant letters

Hint

- Check `ch.isalpha()` and `ch.lower()`.

Example Inputs (to test)

- `count_consonants("Hello World")` → `7`
- `count_consonants("AEIOU")` → `0`

File: `f24_count_consonants.py`

### 25. Squares from 1 to n

Problem: Return a list of squares from 1..n.

Function Name: `squares_1_to_n` Import: none

Inputs

- `n: int`  # assume n >= 1

Output

- `list[int]`  # squares list

Example Inputs (to test)

- `squares_1_to_n(5)` → `[1, 4, 9, 16, 25]`
- `squares_1_to_n(1)` → `[1]`

File: `f25_squares_1_to_n.py`

### 26. Cumulative Maximum

Problem: Return a list where each position i is the maximum value seen so far.

- Example: [2, 1, 3, 0, 5] → [2, 2, 3, 3, 5]

Function Name: `cumulative_max` Import: none

Inputs

- `nums: list[int]`

Output

- `list[int]`  # cumulative max list

Example Inputs (to test)

- `cumulative_max([2, 1, 3, 0, 5])` → `[2, 2, 3, 3, 5]`
- `cumulative_max([])` → `[]`

File: `f26_cumulative_max.py`

### 27. Keep Only Even Numbers

Problem: Return a new list containing only the even numbers.

Function Name: `keep_only_evens` Import: none

Inputs

- `nums: list[int]`

Output

- `list[int]`  # only even values

Example Inputs (to test)

- `keep_only_evens([3, 4, 0, 7, 8, 9])` → `[4, 0, 8]`
- `keep_only_evens([])` → `[]`

File: `f27_keep_only_evens.py`

### 28. Dash Join Words

Problem: Return all words joined by dashes.

Function Name: `dash_join` Import: none

Inputs

- `words: list[str]`

Output

- `str`  # words joined with '-'

Example Inputs (to test)

- `dash_join(["coding", "for", "all"])` → `"coding-for-all"`
- `dash_join([])` → `""`

File: `f28_dash_join.py`

### 29. Count Occurrences

Problem: Count how many times `target` appears in the list.

Function Name: `count_occurrences` Import: none

Inputs

- `nums: list[int]`
- `target: int`

Output

- `int`  # number of occurrences

Example Inputs (to test)

- `count_occurrences([1, 2, 1, 1, 3], 1)` → `3`
- `count_occurrences([], 7)` → `0`

File: `f29_count_occurrences.py`

### 30. Minimum in List (non-empty)

Problem: Return the smallest number in the list. Assume the list is not empty.

Function Name: `min_in_list` Import: none

Inputs

- `nums: list[int]`  # non-empty

Output

- `int`  # smallest value

Example Inputs (to test)

- `min_in_list([5, 2, 9, -1, 3])` → `-1`

File: `f30_min_in_list.py`

---

## Topic D — While Loops (Exercises 31–40)

### Mini Lesson: How `while` loops stop

A `while` loop repeats **as long as** its condition is True. It stops when the condition becomes False.

---

### 31. Countdown List

Problem: Return a list counting down from n to 0.

Function Name: `countdown_list` Import: none

Inputs

- `n: int`  # n >= 0

Output

- `list[int]`  # n, n-1, ..., 0

Example Inputs (to test)

- `countdown_list(5)` → `[5, 4, 3, 2, 1, 0]`
- `countdown_list(0)` → `[0]`

File: `f31_countdown_list.py`

### 32. Sum Until Zero

Problem: Sum numbers from the list until you see a 0.

- Stop when you reach 0.
- Do not include the 0 in the sum.

Function Name: `sum_until_zero` Import: none

Inputs

- `nums: list[int]`

Output

- `int`  # sum until the first 0

Example Inputs (to test)

- `sum_until_zero([3, 4, 2, 0, 100])` → `9`
- `sum_until_zero([0, 5])` → `0`

File: `f32_sum_until_zero.py`

### 33. Count Digits

Problem: Return how many digits are in n (n >= 0).

- Special case: 0 has 1 digit.

Function Name: `count_digits` Import: none

Inputs

- `n: int`

Output

- `int`  # number of digits

Example Inputs (to test)

- `count_digits(0)` → `1`
- `count_digits(12345)` → `5`

File: `f33_count_digits.py`

### 34. Reverse Number

Problem: Reverse the digits of n (n >= 0).

- Example: 120 → 21

Function Name: `reverse_number` Import: none

Inputs

- `n: int`

Output

- `int`  # reversed digits

Example Inputs (to test)

- `reverse_number(120)` → `21`
- `reverse_number(7)` → `7`

File: `f34_reverse_number.py`

### 35. Multiply by Repeated Addition

Problem: Compute `a * b` using repeated addition.

- Assume `b >= 0`.

Function Name: `multiply_repeat` Import: none

Inputs

- `a: int`
- `b: int`

Output

- `int`  # a \* b

Example Inputs (to test)

- `multiply_repeat(3, 4)` → `12`
- `multiply_repeat(5, 0)` → `0`

File: `f35_multiply_repeat.py`

### 36. Power by Repeated Multiplication

Problem: Compute `base ** exp` using a loop.

- Assume `exp >= 0`.

Function Name: `power_loop` Import: none

Inputs

- `base: int`
- `exp: int`

Output

- `int`  # base^exp

Example Inputs (to test)

- `power_loop(2, 5)` → `32`
- `power_loop(3, 0)` → `1`

File: `f36_power_loop.py`

### 37. Double Until Target

Problem: Start from 1 and keep doubling until the value is at least `target`. Return the final value.

Function Name: `double_until` Import: none

Inputs

- `target: int`  # target >= 1

Output

- `int`  # first power of 2 >= target

Example Inputs (to test)

- `double_until(9)` → `16`
- `double_until(1)` → `1`

File: `f37_double_until.py`

### 38. Last Index

Problem: Return the last index of `target` in the list, or -1 if not found.

Function Name: `last_index` Import: none

Inputs

- `nums: list[int]`
- `target: int`

Output

- `int`  # last index or -1

Example Inputs (to test)

- `last_index([5, 3, 5, 2, 5], 5)` → `4`
- `last_index([5, 3, 5, 2, 5], 9)` → `-1`

File: `f38_last_index.py`

### 39. Remove Leading Zeros

Problem: Remove leading `'0'` characters from a string.

- If the result becomes empty, return `"0"`.

Function Name: `remove_leading_zeros` Import: none

Inputs

- `s: str`

Output

- `str`  # string without leading zeros

Example Inputs (to test)

- `remove_leading_zeros("000123")` → `"123"`
- `remove_leading_zeros("0000")` → `"0"`

File: `f39_remove_leading_zeros.py`

### 40. Repeat Text

Problem: Return the text repeated n times.

Function Name: `repeat_text` Import: none

Inputs

- `text: str`
- `n: int`  # n >= 0

Output

- `str`  # repeated text

Example Inputs (to test)

- `repeat_text("ha", 3)` → `"hahaha"`
- `repeat_text("x", 0)` → `""`

File: `f40_repeat_text.py`

---

## Topic E — Lists (Indexing & Common Patterns) (Exercises 41–50)

### Mini Lesson: Lists and indexing

A list is an ordered container of items. Indexing starts at 0:

- `nums[0]` is the first item
- `nums[1]` is the second item
- `len(nums)` is how many items are in the list

---

### 41. Last Element (non-empty)

Problem: Return the last element of the list. Assume the list is not empty.

Function Name: `last_element` Import: none

Inputs

- `nums: list[int]`  # non-empty

Output

- `int`  # last item

Example Inputs (to test)

- `last_element([3, 1, 9])` → `9`

File: `f41_last_element.py`

### 42. First Two Elements (safe)

Problem: Return the first two elements of the list.

- If the list has fewer than 2 items, return the whole list.

Function Name: `first_two` Import: none

Inputs

- `nums: list[int]`

Output

- `list[int]`  # first two items (or fewer)

Example Inputs (to test)

- `first_two([1, 2, 3, 4])` → `[1, 2]`
- `first_two([9])` → `[9]`

File: `f42_first_two.py`

### 43. Swap First and Last

Problem: Return a new list where the first and last elements are swapped.

- Assume the list length is at least 2.

Function Name: `swap_first_last` Import: none

Inputs

- `nums: list[int]`

Output

- `list[int]`  # new list with swapped ends

Example Inputs (to test)

- `swap_first_last([1, 2, 3, 4])` → `[4, 2, 3, 1]`

File: `f43_swap_first_last.py`

### 44. Count Above Average

Problem: Return how many numbers are strictly above the average.

- Assume the list is not empty.

Function Name: `count_above_average` Import: none

Inputs

- `nums: list[int]`

Output

- `int`  # count above average

Example Inputs (to test)

- `count_above_average([1, 2, 3, 4, 10])` → `1`

File: `f44_count_above_average.py`

### 45. Remove All Occurrences

Problem: Return a new list where all occurrences of `target` are removed.

Function Name: `remove_all` Import: none

Inputs

- `nums: list[int]`
- `target: int`

Output

- `list[int]`  # list without target

Example Inputs (to test)

- `remove_all([1, 2, 1, 3, 1], 1)` → `[2, 3]`

File: `f45_remove_all.py`

### 46. Append (Return New)

Problem: Return a new list with `value` added to the end.

- Do not change (mutate) the original list.

Function Name: `append_new` Import: none

Inputs

- `nums: list[int]`
- `value: int`

Output

- `list[int]`  # new list with value appended

Example Inputs (to test)

- `append_new([1, 2], 9)` → `[1, 2, 9]`

File: `f46_append_new.py`

### 47. Flatten One Level

Problem: Flatten a list of lists by one level.

Function Name: `flatten` Import: none

Inputs

- `items: list[list[int]]`

Output

- `list[int]`  # flattened list

Example Inputs (to test)

- `flatten([[1, 2], [3], [4, 5]])` → `[1, 2, 3, 4, 5]`

File: `f47_flatten.py`

### 48. Rotate Left by k

Problem: Rotate the list left by k positions.

- Example: items=[1,2,3,4,5], k=2 → [3,4,5,1,2]
- If k is larger than the list length, wrap around.
- If the list is empty, return [].

Function Name: `rotate_left` Import: none

Inputs

- `items: list[int]`
- `k: int`

Output

- `list[int]`  # rotated list

Hint

- Use `k = k % len(items)` when the list is not empty.

Example Inputs (to test)

- `rotate_left([1, 2, 3, 4, 5], 2)` → `[3, 4, 5, 1, 2]`
- `rotate_left([1, 2, 3], 5)` → `[3, 1, 2]`

File: `f48_rotate_left.py`

### 49. Is Sorted (Ascending)

Problem: Return True if the list is in non-decreasing order.

- Non-decreasing means each next value is >= previous.

Function Name: `is_sorted` Import: none

Inputs

- `nums: list[int]`

Output

- `bool`  # True if sorted ascending

Example Inputs (to test)

- `is_sorted([1, 2, 2, 5])` → `True`
- `is_sorted([3, 2, 1])` → `False`

File: `f49_is_sorted.py`

### 50. Has Duplicates

Problem: Return True if the list contains any duplicate value, otherwise False.

Function Name: `has_duplicates` Import: none

Inputs

- `nums: list[int]`

Output

- `bool`  # True if any value repeats

Hint

- A set stores unique values. If a value is already in the set, it’s a duplicate.

Example Inputs (to test)

- `has_duplicates([1, 2, 3, 2])` → `True`
- `has_duplicates([1, 2, 3])` → `False`

File: `f50_has_duplicates.py`

---

## Topic F — Dictionaries (Counting + dict.get) (Exercises 51–60)

### Mini Lesson: Dictionaries and `get()`

A dictionary stores **key → value** pairs.

- Example: `{"apple": 2, "banana": 1}` means apple has count 2.

`d.get(key, default)` means:

- If `key` exists, return its value.
- If not, return `default`.

Counting pattern:

- `counts[x] = counts.get(x, 0) + 1`

---

### 51. Frequency Dictionary (Numbers)

Problem: Return a dictionary counting how many times each number appears.

Function Name: `frequency` Import: none

Inputs

- `nums: list[int]`

Output

- `dict[int, int]`  # number → count

Hint

- Start with an empty dictionary: `counts = {}`
- For each number `x`, update using:
  - `counts[x] = counts.get(x, 0) + 1`

Example Inputs (to test)

- `frequency([2, 2, 5, 2, 5])` → `{2: 3, 5: 2}`
- `frequency([])` → `{}`

File: `f51_frequency.py`

### 52. Character Frequency (Ignore Spaces)

Problem: Count each character in the string, but ignore spaces.

Function Name: `char_frequency_no_spaces` Import: none

Inputs

- `s: str`

Output

- `dict[str, int]`  # character → count

Hint

- Loop through the string one character at a time.
- Skip spaces:
  - `if ch == ' ': continue`
- Count using the same pattern:
  - `counts[ch] = counts.get(ch, 0) + 1`

Example Inputs (to test)

- `char_frequency_no_spaces("a b a c")` → `{ "a": 2, "b": 1, "c": 1 }`

File: `f52_char_frequency_no_spaces.py`

### 53. Get With Default

Problem: Return `d[key]` if the key exists, otherwise return `default`.

Function Name: `get_with_default` Import: none

Inputs

- `d: dict[str, int]`
- `key: str`
- `default: int`

Output

- `int`  # value if key exists, else default

Hint

- Use dictionary `.get()`:
  - `return d.get(key, default)`

Example Inputs (to test)

- `get_with_default({"a": 3}, "a", 0)` → `3`
- `get_with_default({"a": 3}, "b", 0)` → `0`

File: `f53_get_with_default.py`

### 54. Sum of Dictionary Values

Problem: Return the sum of all values in the dictionary.

Function Name: `sum_dict_values` Import: none

Inputs

- `d: dict[str, int]`

Output

- `int`  # sum of values

Hint

- Start `total = 0`
- Loop over the dictionary values:
  - `for v in d.values(): total += v`

Example Inputs (to test)

- `sum_dict_values({"a": 2, "b": 5})` → `7`
- `sum_dict_values({})` → `0`

File: `f54_sum_dict_values.py`

### 55. Most Frequent Number

Problem: Return the number that appears the most. Tie rule: if two numbers have the same highest frequency, return the smaller number.

Function Name: `most_frequent_number` Import: none

Inputs

- `nums: list[int]`  # assume non-empty

Output

- `int`  # most frequent number

Hint

- Step 1: Build counts using a dictionary (like Ex51).
- Step 2: Track the best answer:
  - Start with `best_num = nums[0]`
  - For each number `x` in `counts`:
    - If `counts[x]` is bigger → update
    - If equal and `x` is smaller → update

Example Inputs (to test)

- `most_frequent_number([2, 2, 3, 3, 3, 1, 1])` → `3`
- `most_frequent_number([4, 4, 5, 5])` → `4`

File: `f55_most_frequent_number.py`

### 56. Merge Counts

Problem: Combine two count dictionaries by adding counts.

Function Name: `merge_counts` Import: none

Inputs

- `a: dict[str, int]`
- `b: dict[str, int]`

Output

- `dict[str, int]`  # merged counts

Hint

- Start with a new dictionary `out = {}`
- Copy keys from `a` into `out`.
- Then for each key in `b`, add it into `out` using:
  - `out[key] = out.get(key, 0) + b[key]`

Example Inputs (to test)

- `merge_counts({"a": 2}, {"a": 1, "b": 3})` → `{ "a": 3, "b": 3 }`

File: `f56_merge_counts.py`

### 57. Word Count

Problem: Count how many times each word appears.

- Words are separated by spaces.

Function Name: `word_count` Import: none

Inputs

- `s: str`

Output

- `dict[str, int]`  # word → count

Hint

- Split the string into words:
  - `words = s.split()`
- For each word, count it with:
  - `counts[w] = counts.get(w, 0) + 1`

Example Inputs (to test)

- `word_count("hi hi bye")` → `{ "hi": 2, "bye": 1 }`

File: `f57_word_count.py`

### 58. Keys With Count At Least k

Problem: Return a sorted list of keys whose value is >= k.

Function Name: `keys_at_least` Import: none

Inputs

- `d: dict[str, int]`
- `k: int`

Output

- `list[str]`  # keys with value >= k, sorted

Hint

- Make a list of keys that match:
  - `out = []`
  - `for key, val in d.items(): if val >= k: out.append(key)`
- Sort before returning:
  - `out.sort()`

Example Inputs (to test)

- `keys_at_least({"a": 2, "b": 5, "c": 1}, 2)` → `["a", "b"]`

File: `f58_keys_at_least.py`

### 59. Invert Dictionary (Unique Values)

Problem: Invert a dictionary where all values are unique.

- Example: {"a": 1, "b": 2} becomes {1: "a", 2: "b"}

Function Name: `invert_unique` Import: none

Inputs

- `d: dict[str, int]`

Output

- `dict[int, str]`  # inverted dict

Hint

- Create a new dictionary `out = {}`
- Loop through items:
  - `for key, val in d.items(): out[val] = key`

Example Inputs (to test)

- `invert_unique({"a": 1, "b": 2})` → `{ 1: "a", 2: "b" }`

File: `f59_invert_unique.py`

### 60. Histogram Bars

Problem: Return a dictionary mapping each number to a string of `*` repeated count times.

Function Name: `histogram` Import: none

Inputs

- `nums: list[int]`

Output

- `dict[int, str]`  # number → "\*" repeated

Hint

- Step 1: Reuse Ex51 to get counts.
- Step 2: Build the output dictionary:
  - For each number `x` in counts, set:
    - `out[x] = "*" * counts[x]`

Example Inputs (to test)

- `histogram([2, 2, 5, 5, 5])` → `{ 2: "**", 5: "***" }`

File: `f60_histogram.py`
