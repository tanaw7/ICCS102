# ICCS102 Python Basics Part 2 In-Class Assessment — Worked Solutions

This document shows one clean and simple way to solve each exercise.

## Before You Look at the Solutions

For this assessment, correctness was not only about the logic. It also depended on:

* exact **file names**
* exact **function / class names**
* correct **type hints**
* using **return** when the exercise expects a returned value
* following the **exact output format**

A program can be logically close but still lose points if it does not match the required interface.

---

## Exercise 1 — `point_message`

### Goal

Take a point as a tuple `(x, y)` and return the message in this exact format:

`Point: (x, y)`

### Correct Code

```python
def point_message(point: tuple[int, int]) -> str:
    x, y = point
    return f"Point: ({x}, {y})"
```

### What is happening

* `point` is a tuple with 2 values.
* `x, y = point` unpacks the tuple.
* The function returns one formatted string.

### Test Cases

| Input         | Expected Output      |
| ------------- | -------------------- |
| `(3, 5)`      | `Point: (3, 5)`      |
| `(0, 0)`      | `Point: (0, 0)`      |
| `(-2, 7)`     | `Point: (-2, 7)`     |
| `(10, -4)`    | `Point: (10, -4)`    |
| `(999, 1000)` | `Point: (999, 1000)` |
| `(-8, -9)`    | `Point: (-8, -9)`    |

### Common Mistakes

* printing instead of returning
* missing type hints
* wrong text format such as missing space after comma
* using square brackets or other formatting instead of parentheses

### Key Lesson

A small formatting requirement still matters. Read the required output carefully.

---

## Exercise 2 — `unique_numbers`

### Goal

Return the unique numbers from a list as a set.

### Correct Code

```python
def unique_numbers(numbers: list[int]) -> set[int]:
    return set(numbers)
```

### What is happening

* A set keeps only unique values.
* Converting a list to a set removes duplicates automatically.

### Test Cases

| Input                | Expected Output |
| -------------------- | --------------- |
| `[1, 2, 2, 3]`       | `{1, 2, 3}`     |
| `[5, 5, 5]`          | `{5}`           |
| `[4, 1, 4, 2, 1]`    | `{1, 2, 4}`     |
| `[]`                 | `set()`         |
| `[-1, -1, 0, 2]`     | `{-1, 0, 2}`    |
| `[3, 2, 1, 3, 2, 1]` | `{1, 2, 3}`     |

### Important Note

Sets are **unordered**, so the display order may vary. For example, `{1, 2, 4}` and `{4, 1, 2}` represent the same set.

### Common Mistakes

* returning a list instead of a set
* manually removing duplicates but still returning the wrong type
* forgetting that an empty set is written as `set()`, not `{}`

### Key Lesson

Choose the data structure that matches the task. Here, `set` is the right tool.

---

## Exercise 3 — `get_price`

### Goal

Look up a product name in a dictionary and return its price.
If the product is not found, return `-1`.

### Correct Code

```python
def get_price(products: dict[str, int], product_name: str) -> int:
    if product_name in products:
        return products[product_name]
    return -1
```

### What is happening

* `products` is a dictionary of product names and prices.
* If the key exists, return the value.
* If the key does not exist, return `-1`.

### Test Cases

| Input                                     | Expected Output |
| ----------------------------------------- | --------------- |
| `({"water": 10, "coffee": 45}, "water")`  | `10`            |
| `({"water": 10, "coffee": 45}, "coffee")` | `45`            |
| `({"water": 10, "coffee": 45}, "tea")`    | `-1`            |
| `({}, "water")`                           | `-1`            |
| `({"tea": 0, "cake": 30}, "tea")`         | `0`             |
| `({"A": 100, "a": 1}, "a")`               | `1`             |

### Common Mistakes

* trying to access `products[product_name]` without checking first
* returning `0` or `None` instead of `-1`
* confusing keys and values

### Key Lesson

When working with dictionaries, always think about the case where the key might not exist.

---

## Exercise 4 — `top_student`

### Goal

Return the name of the student with the highest score.

### Correct Code

```python
def top_student(students: dict[str, int]) -> str:
    best_name = ""
    best_score = None

    for name, score in students.items():
        if best_score is None or score > best_score:
            best_name = name
            best_score = score

    return best_name
```

### What is happening

* Start with no best student yet.
* This solution uses `None` as the starting value for `best_score`. That is only one possible approach.
* Loop through each `(name, score)` pair.
* Whenever a higher score is found, update both the name and the score.
* Return the final best name.

### Test Cases

| Input                                  | Expected Output |
| -------------------------------------- | --------------- |
| `{"Alice": 92, "Bob": 85, "Cara": 95}` | `Cara`          |
| `{"Dan": 70, "Eve": 88}`               | `Eve`           |
| `{"Mina": 100}`                        | `Mina`          |
| `{"A": 0, "B": 1}`                     | `B`             |
| `{"Ann": 80, "Ben": 81, "Cam": 79}`    | `Ben`           |
| `{"Low": 1, "High": 99, "Mid": 50}`    | `High`          |

### Common Mistakes

* updating the best score but forgetting to update the best name
* returning the last name in the loop instead of the true top student
* assuming the highest value is always the last one

### Key Lesson

When you track a “best” value, you usually need to track the related information too.

---

## Exercise 5 — `Student` class and `student_summary`

### Goal

Create a `Student` object with a name and score, then return a summary string.

### Correct Code

```python
class Student:
    def __init__(self, name: str, score: int) -> None:
        self.name = name
        self.score = score


def student_summary(student: Student) -> str:
    return f"{student.name} scored {student.score}"
```

### What is happening

* `__init__` runs when a new `Student` object is created.
* `self.name` and `self.score` store the values inside the object.
* `student_summary()` reads those values and returns one string.

### Test Cases

| Input                  | Expected Output   |
| ---------------------- | ----------------- |
| `Student("Alice", 92)` | `Alice scored 92` |
| `Student("Bob", 0)`    | `Bob scored 0`    |
| `Student("Mina", 100)` | `Mina scored 100` |
| `Student("Nok", -1)`   | `Nok scored -1`   |
| `Student("A B", 77)`   | `A B scored 77`   |

### Common Mistakes

* forgetting `self`
* forgetting to store the values as attributes
* writing the class correctly but printing instead of returning in `student_summary`
* missing type hints in `__init__` or the function

### Key Lesson

A class stores related data together. The function then uses that object in a simple, readable way.

---

## Exercise 6 — `menu_combinations`

### Goal

Return all food-drink combinations in this format:

`Food - Drink`

### Correct Code

```python
def menu_combinations(food: list[str], drinks: list[str]) -> list[str]:
    result = []

    for item in food:
        for drink in drinks:
            result.append(f"{item} - {drink}")

    return result
```

### What is happening

* Use a nested loop.
* The outer loop goes through each food item.
* The inner loop goes through each drink.
* Each pair is added to the result list.

### Test Cases

| Input                                     | Expected Output                                                      |
| ----------------------------------------- | -------------------------------------------------------------------- |
| `(["Rice", "Noodles"], ["Tea", "Water"])` | `["Rice - Tea", "Rice - Water", "Noodles - Tea", "Noodles - Water"]` |
| `(["Burger"], ["Juice", "Soda"])`         | `["Burger - Juice", "Burger - Soda"]`                                |
| `([], ["Tea"])`                           | `[]`                                                                 |
| `(["Rice"], [])`                          | `[]`                                                                 |
| `([], [])`                                | `[]`                                                                 |
| `(["A", "B", "C"], ["X"])`                | `["A - X", "B - X", "C - X"]`                                        |
| `(["A"], ["X", "Y", "Z"])`                | `["A - X", "A - Y", "A - Z"]`                                        |

### Common Mistakes

* forgetting to use nested loops
* returning only one combination
* using the wrong format such as `Food, Drink` instead of `Food - Drink`
* reusing one variable incorrectly and overwriting earlier results

### Key Lesson

Nested loops are useful when every item from one list must pair with every item from another list.

---

## Exercise 7 — `matrix_values`

### Goal

Take a 2D list (matrix) and return all values in one flat list, row by row.

### Correct Code

```python
def matrix_values(matrix: list[list[int]]) -> list[int]:
    result = []

    for row in matrix:
        for value in row:
            result.append(value)

    return result
```

### What is happening

* `matrix` is a list of rows.
* First loop: go through each row.
* Second loop: go through each value in that row.
* Add each value to one final list.

### Test Cases

| Input               | Expected Output |
| ------------------- | --------------- |
| `[[1, 2], [3, 4]]`  | `[1, 2, 3, 4]`  |
| `[[5, 6, 7]]`       | `[5, 6, 7]`     |
| `[[1], [2], [3]]`   | `[1, 2, 3]`     |
| `[]`                | `[]`            |
| `[[], [1, 2], []]`  | `[1, 2]`        |
| `[[0, -1], [2, 3]]` | `[0, -1, 2, 3]` |

### Common Mistakes

* appending the whole row instead of each value
* returning the original matrix unchanged
* using only one loop

### Key Lesson

A 2D list usually needs nested loops when you want to visit every value.

---

## Exercise 8 — `find_target_in_matrix`

### Goal

Search for a target number in a matrix, **but skip any row that contains `0`**.
Return `True` if the target is found in a row that is not skipped. Otherwise return `False`.

### Correct Code

```python
def find_target_in_matrix(matrix: list[list[int]], number: int) -> bool:
    for row in matrix:
        if 0 in row:
            continue

        for value in row:
            if value == number:
                return True

    return False
```

### What is happening

* Go through the matrix one row at a time.
* If a row contains `0`, skip the whole row with `continue`.
* Otherwise, search that row normally.
* If the target is found, return `True` immediately.
* If the loop finishes without finding it, return `False`.

### Test Cases

| Input                                                                    | Expected Output |
| ------------------------------------------------------------------------ | --------------- |
| `([[1, 0], [3, 2]], 2)`                                                  | `True`          |
| `([[5, 0], [1, 2]], 5)`                                                  | `False`         |
| `([[1, 2], [0, 4]], 4)`                                                  | `False`         |
| `([[1, 2, 3, 4], [5, 0, 7, 11], [9, 10, 11, 12], [13, 14, 15, 16]], 11)` | `True`          |
| `([], 1)`                                                                | `False`         |
| `([[0], [1], [2, 3]], 1)`                                                | `True`         |
| `([[1, 2], [3, 0], [4, 5]], 3)`                                          | `False`          |
| `([[1, 2], [3, 4]], 9)`                                                  | `False`         |

### Common Mistakes

* searching inside rows that should be skipped
* returning `False` too early inside the loop
* only checking whether the row contains the target, but forgetting the “skip row if it has 0” rule
* confusing `continue` with `break`

### Key Lesson

Read the condition carefully. This exercise is not just about finding a number. It is about finding a number **under a rule**.

---

## Final Reminders

When you prepare for similar exercises, always check these things before submitting:

1. Is the **function name** exactly correct?
2. Is the file name exactly correct?
3. Are the **parameter names and type hints** correct?
4. Does the function **return** the answer instead of printing it?
5. Does the output match the **exact required format**?
6. Did you test more than one case, including empty or unusual input?

In programming, correct logic is important, but so is precision.
