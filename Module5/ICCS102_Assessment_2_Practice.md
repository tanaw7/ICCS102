# ICCS102 — Coding Assessment 2: Practice Set B

## Python Basics Part 2

Complete these eight exercises to practise combining conditions, loops, collections, and objects. The assessment will require you to apply these skills to different problems.

## Working rules

- Write one Python file per exercise, using the filename and function or class names shown.
- Keep the parameter names and order shown. Infer and add suitable type hints and return types to every function and method. `self` needs no annotation; `__init__` returns `None`.
- Receive data through parameters and return the requested result. Keep supplied collections and objects unchanged.
- Do not use imports or `input()`. Use `print()` for testing, then remove or comment out test calls.
- Helper functions are allowed in the same file. Use Python 3.9 or later.
- Assume inputs follow the conditions stated. Handle every valid input, including the stated empty cases.
- For exam-style practice, work independently using your slides, notes, and the official Python documentation, without AI or search engines.

## Required type hints

**Correct results alone are not enough for full marks. Every function and method must include correct input parameter type hints and a return type annotation, including helper functions and constructors.**

- Annotate every parameter except `self`.
- Write the return type after `->`. For `__init__`, write `-> None` and annotate all other parameters.
- Specify collection contents, such as `list[int]`, `tuple[int, int]`, or `dict[str, int]`; a bare `list`, `tuple`, `set`, or `dict` is insufficient when the contents are specified.
- For a parameter that receives an object, use the required class name as its type.
- Infer the types from each question. The supplied outlines deliberately omit annotations; you must complete them.

For example, a function receiving a whole-number quantity and a whole-number unit price and returning a whole-number cost would have this signature:

```python
def calculate_cost(quantity: int, unit_price: int) -> int:
    ...
```

## Checking your work

Result columns show how returned values look when printed. Return the values from your functions. For each exercise, try the examples and at least two additional inputs of your own, including a boundary or empty case where allowed. Check the result's type as well as its value.

## Exercises

### 1. Clamp a Reading

A reading and its allowed bounds are integers. `bounds` is a tuple `(minimum, maximum)`, where minimum is less than or equal to maximum. Return the reading if it is inside the inclusive bounds. If it is below the minimum, return the minimum; if above the maximum, return the maximum.

Values and bounds may be negative, zero, or positive. Return an integer.

**Function:** `clamp_reading(value, bounds)`

```python
def clamp_reading(value, bounds):
    ...
```

| Function call | Result when printed |
|---|---|
| `clamp_reading(7, (2, 10))` | `7` |
| `clamp_reading(-3, (0, 8))` | `0` |
| `clamp_reading(12, (0, 8))` | `8` |
| `clamp_reading(4, (4, 4))` | `4` |

**File:** `p01_clamp_reading.py`

### 2. Count Labels

Given a list of strings, return a dictionary mapping each distinct label to the number of times it occurs. Ignore empty strings. Labels are case-sensitive; do not change their spelling or remove spaces.

The list may be empty. Use a loop to build the dictionary. Dictionary order does not matter.

**Function:** `count_labels(labels)`

```python
def count_labels(labels):
    ...
```

| Function call | Result when printed |
|---|---|
| `count_labels(["red", "blue", "red", ""])` | `{'red': 2, 'blue': 1}` |
| `count_labels(["A", "a", "A"])` | `{'A': 2, 'a': 1}` |
| `count_labels(["", ""])` | `{}` |
| `count_labels([])` | `{}` |

**File:** `p02_count_labels.py`

### 3. Repeated IDs

Given a list of integer IDs, return a set containing only IDs that occur at least twice. An ID occurring three or more times still appears once in the result.

Use a loop and sets to keep track of IDs already seen and IDs repeated. The list may be empty. Set order does not matter; `set()` represents an empty set.

**Function:** `repeated_ids(ids)`

```python
def repeated_ids(ids):
    ...
```

| Function call | Result when printed |
|---|---|
| `repeated_ids([4, 2, 4, 4, 3, 2])` | `{2, 4}` |
| `repeated_ids([1, 2, 3])` | `set()` |
| `repeated_ids([0, -1, 0, -1])` | `{0, -1}` |
| `repeated_ids([])` | `set()` |

**File:** `p03_repeated_ids.py`

### 4. Reading Progress

Create a class named `Reading` whose constructor receives `title`, `total_pages`, and `pages_read`, and stores attributes with those exact names. Title is a string; page counts are nonnegative integers, and pages read never exceeds total pages.

Write `pages_left(reading, extra_pages)`, which returns how many pages would remain after reading `extra_pages` more pages. Extra pages is a nonnegative integer. The answer cannot be negative. Leave the object unchanged.

Add type hints to this structure:

```python
class Reading:
    def __init__(self, title, total_pages, pages_read):
        ...

def pages_left(reading, extra_pages):
    ...
```

Use the object's attributes in the calculation and annotate `reading` using the `Reading` class.

| Function call | Result when printed |
|---|---|
| `pages_left(Reading("Python", 100, 30), 20)` | `50` |
| `pages_left(Reading("Python", 100, 30), 80)` | `0` |
| `pages_left(Reading("Notes", 12, 12), 0)` | `0` |
| `pages_left(Reading("Blank", 0, 0), 5)` | `0` |

**File:** `p04_reading_class.py`

### 5. Combine Vote Counts

Two dictionaries map candidate names to vote counts. Return a new dictionary containing every name found in either dictionary. If a name appears in both, add its counts. Otherwise, keep its existing count. Include names with zero votes.

Names are case-sensitive strings and counts are nonnegative integers. Either dictionary may be empty. Use loops and keep both originals unchanged. Dictionary order does not matter.

**Function:** `combine_votes(first, second)`

```python
def combine_votes(first, second):
    ...
```

| Function call | Result when printed |
|---|---|
| `combine_votes({"A": 3, "B": 2}, {"B": 4, "C": 1})` | `{'A': 3, 'B': 6, 'C': 1}` |
| `combine_votes({}, {"A": 0})` | `{'A': 0}` |
| `combine_votes({"A": 2}, {})` | `{'A': 2}` |
| `combine_votes({}, {})` | `{}` |

**File:** `p05_combine_votes.py`

### 6. Matching Positions

Given two lists of strings, return a list of index tuples `(i, j)` for all pairs whose strings are equal: `first[i] == second[j]`. Indices start at zero. Comparisons are case-sensitive.

Process positions in `first` from left to right. For each position, process every position in `second` from left to right. Repeated strings can produce several matching pairs. Either list may be empty.

Use nested loops. Return index pairs, not the matching strings.

**Function:** `matching_positions(first, second)`

```python
def matching_positions(first, second):
    ...
```

| Function call | Result when printed |
|---|---|
| `matching_positions(["A", "B", "A"], ["B", "A"])` | `[(0, 1), (1, 0), (2, 1)]` |
| `matching_positions(["x", "x"], ["x", "x"])` | `[(0, 0), (0, 1), (1, 0), (1, 1)]` |
| `matching_positions(["A"], ["a"])` | `[]` |
| `matching_positions([], ["x"])` | `[]` |

**File:** `p06_matching_positions.py`

### 7. Row Spreads

Return a list containing the spread of each row: its largest value minus its smallest value. Keep the original row order. A row containing one value has spread zero.

The matrix contains integer rows of equal length. Values may be negative. The matrix may be empty; if any rows exist, each contains at least one value. Return `[]` for an empty matrix.

Use nested loops to find each row's smallest and largest values. Do not use `min()`, `max()`, or sorting.

**Function:** `row_spreads(matrix)`

```python
def row_spreads(matrix):
    ...
```

| Function call | Result when printed |
|---|---|
| `row_spreads([[3, 8, 5], [-4, -1, -6]])` | `[5, 5]` |
| `row_spreads([[7], [-2]])` | `[0, 0]` |
| `row_spreads([[4, 4], [0, 9]])` | `[0, 9]` |
| `row_spreads([])` | `[]` |

**File:** `p07_row_spreads.py`

### 8. Most Qualifying Readings

Count how many values in each row are greater than or equal to `threshold`. Return the zero-based index of the row with the largest count. If several rows tie, return the earliest row's index. If every count is zero, return `-1`.

The matrix contains rows of integers, all with the same length. Values and the integer threshold may be negative, zero, or positive. The matrix may have no rows or no columns; return `-1` in either case.

Use nested loops to count qualifying values and compare row counts. Select by count, not by the sum of the values.

**Function:** `best_reading_row(matrix, threshold)`

```python
def best_reading_row(matrix, threshold):
    ...
```

| Function call | Result when printed |
|---|---|
| `best_reading_row([[9, 0, 0], [5, 6, 1]], 5)` | `1` |
| `best_reading_row([[5, 0], [6, 0]], 5)` | `0` |
| `best_reading_row([[1, 2], [3, 4]], 5)` | `-1` |
| `best_reading_row([[-2, -1], [-3, 0]], -1)` | `0` |
| `best_reading_row([], 0)` | `-1` |
| `best_reading_row([[], []], 0)` | `-1` |

**File:** `p08_best_reading_row.py`

## Practice scoring

For a mock assessment, allow 1 hour 40 minutes. Each exercise is worth 10 points; count your seven highest scores after deductions, for a maximum of 70. Work through all eight exercises during revision to practise every topic.

An exercise starts at 10 points if its results are correct for all valid test inputs, including the required type and format. The class exercise must also store its attributes correctly. Incorrect results receive zero for that exercise. Correct results alone do not guarantee full marks.

| Type-hint issue | Deduction |
|---|---|
| Missing or incorrect input parameter type hint, excluding `self` | −0.25 per affected parameter |
| Missing or incorrect return type annotation, including `-> None` for `__init__` | −0.25 per function or method |

These deductions also apply to helper functions and constructor parameters. The real assessment's remaining coding and submission deductions also apply when using this set as a mock assessment. Apply exercise deductions before selecting the best seven scores; no exercise score can fall below zero.
