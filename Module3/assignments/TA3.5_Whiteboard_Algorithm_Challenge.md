# ICCS102 — Module 3 Team Assignment 3.5
# Whiteboard Algorithm Function Challenge

**10 points + up to 1 stretch bonus point**  
**Temporary groups of 3, assigned or approved by the instructor**

## Your Task

Write Python functions for **three different problems**:

- **One assigned by the instructor:** prepare it for the whiteboard.
- **Two others of your choice:** include them in your Google Sheet.

You have **30 minutes initially** to discuss, write and test the assigned problem. Afterward, groups explain their solutions at the board. Complete the other two problems and submit all three by the deadline announced in class.

Use class materials, your notes, Python and discussion within your group. **No AI assistance or online solutions.**

## Python Requirements

- Write a Python function for each problem, with parameter type hints and a return type.
- Use the parameter names and types specified in the problem; choose a clear function name.
- Use **one-dimensional lists** for collections. Ordinary numbers, strings and Boolean values may also be inputs.
- When lists describe the same entries, they have matching lengths: values at the same index belong together. Use that index to access each list.
- Assume inputs have the stated types and meet the problem's conditions. Input lists are nonempty.
- Supply test data directly as function arguments. Do not use `input()` or imports.
- Return a **list of strings** (`list[str]`) containing the requested results. Choose clear message wording and use it consistently. Use `append()` to add messages.
- Keep `print()` outside the function when testing. Run your code and check its returned results before submitting.

## Whiteboard Explanation

Show your **assigned problem** with:

1. The problem number and title.
2. Your Python function, including its signature and return statement.
3. One small, valid test input and the expected returned list.
4. A manual trace showing the important checks and changing values.

Use three board areas: **inputs**, **Python function**, and **trace/output**. Use 2–3 input entries where the problem allows it. Write matching lists on separate lines.

Up to three groups write at the same time. You are allowed about **5 minutes to write** and **3 minutes per group to explain**. Each member explains part of the solution. Be ready to explain why a condition is true or false and how values change during the loop.

## Google Sheet Submission

Record your section, group name, members and assigned board problem in your team's tab or area of the designated Google Sheet.

For **each of the three problems**, include:

| Required part | What to include |
|---|---|
| Problem | Number and title. |
| Inputs and output | Parameter meanings and types, and what the returned list contains. |
| Python function | Complete, tested code with indentation preserved. |
| Explanation | 5–8 short steps explaining how the function works. |
| Two manual test cases | Inputs, intermediate loop values or decision checks, expected returned results, and whether the actual output matches. |

For each problem:

1. **Test case 1:** Use the provided inputs.
2. **Test case 2:** Create your own valid inputs to check a different outcome or a boundary value. Briefly explain what this case checks.

For both cases, work out the expected results manually before running your function, then compare them with its actual output. If they differ, investigate and correct your code or manual trace, then check again.

For the assigned problem, also include a readable board photo or typed copy of your board work. Briefly note any correction made afterward.

Use line breaks and text wrapping to keep code and traces readable. For short test inputs, trace every entry. **Six test cases are required in total.**

One coordinator submits the **Google Sheet link in Google Classroom** by the announced deadline. Ensure the instructor has access.

---

# Worked Example — Library Late-Return Fees

This example shows the expected level of code and explanation. It does not count as one of your three problems.

A library checks several returned books. Each late day costs **5 baht**, but the fee for one book cannot exceed **20 baht**. A book returned on time has zero late days. Report each book's fee, the total fees and how many books reached the maximum fee.

**Inputs:** `titles: list[str]` and `days_late: list[int]`. The lists have matching lengths. Late-day counts are nonnegative.

**Return:** A list of messages containing each book's fee and the two totals.

## Python Solution

```python
def calculate_library_fees(
    titles: list[str], days_late: list[int]
) -> list[str]:
    results = []
    total_fees = 0
    maximum_count = 0

    for i in range(len(titles)):
        fee = days_late[i] * 5

        if fee >= 20:
            fee = 20
            maximum_count += 1

        total_fees += fee
        results.append(f"{titles[i]}: {fee} baht")

    results.append(f"Total fees: {total_fees} baht")
    results.append(f"Books at maximum fee: {maximum_count}")
    return results
```

## Explanation

1. Create an empty results list and set both totals to zero.
2. Visit each book using its index in the matching lists.
3. Multiply its late-day count by 5 to calculate the fee.
4. If the calculated fee is at least 20, set it to 20 and count the book as reaching the maximum.
5. Add the fee to the running total and record the book's message.
6. After the loop, append both summary messages and return the list.

## Test Case 1 — On Time, Below the Cap and Above the Cap

```python
calculate_library_fees(
    ["Python", "History", "Space"], [0, 2, 6]
)
```

| Book | Days late | Fee before cap | Fee >= 20? | Final fee | Running total | Maximum count |
|---|---:|---:|---|---:|---:|---:|
| Python | 0 | 0 | False | 0 | 0 | 0 |
| History | 2 | 10 | False | 10 | 10 | 0 |
| Space | 6 | 30 | True | 20 | 30 | 1 |

**Expected return:**

```python
[
    "Python: 0 baht",
    "History: 10 baht",
    "Space: 20 baht",
    "Total fees: 30 baht",
    "Books at maximum fee: 1"
]
```

## Test Case 2 — Exactly at the Cap

```python
calculate_library_fees(["Art", "Music"], [4, 1])
```

| Book | Days late | Fee before cap | Fee >= 20? | Final fee | Running total | Maximum count |
|---|---:|---:|---|---:|---:|---:|
| Art | 4 | 20 | True | 20 | 20 | 1 |
| Music | 1 | 5 | False | 5 | 25 | 1 |

**Expected return:**

```python
[
    "Art: 20 baht",
    "Music: 5 baht",
    "Total fees: 25 baht",
    "Books at maximum fee: 1"
]
```

The second case checks that a fee of exactly 20 baht counts toward the maximum-fee total. Notice that `fee` is calculated again for each book, while `total_fees` and `maximum_count` accumulate across the loop.

---

# Problem Options

The examples below define the **input structure**, not the complete solution. Use the listed parameter names and types, choose a clear function name, and return `list[str]`. Keep all entries in their original order. Stretch tasks are optional and do not replace the main requirements.

## 1. Canteen Budget Tracker

A student buys several items. Track spending after each purchase and say whether the student is within budget or over budget. Process all items even if the budget is exceeded. Finish with total spending and either the money remaining or the amount overspent. Spending exactly the budget is within budget, with zero left.

**Inputs:** `prices: list[int]`, `budget: int`. Prices and budget are nonnegative whole baht; item names are not needed.

```python
prices = [40, 25, 50]
budget = 100
```

**Return:** One spending/status message per item, then the final summary.

**Optional stretch:** After all purchases, apply a 10% discount if the original total is at least 100 baht. Add a revised final summary; keep the earlier running-spending messages unchanged.

## 2. Rainy Week Campus Planner

For each day, give one main recommendation:

- Rain chance at least 70% and no umbrella: find another way to class.
- Rain chance at least 70% with an umbrella: walk with caution.
- Otherwise: walk normally.

If the distance is above 800 metres, add “leave earlier” to that day's recommendation. Count risky days: those with at least 70% rain chance and no umbrella.

**Inputs:** `rain_chances: list[int]` (0–100), `umbrellas: list[bool]`, `distances: list[int]` (nonnegative metres). Matching positions describe one day.

```python
rain_chances = [30, 80, 70]
umbrellas = [False, False, True]
distances = [400, 900, 800]
```

**Return:** One recommendation per day, then the risky-day count.

**Optional stretch:** Add a matching `temperatures: list[float]` and include a heat warning for temperatures at least 35°C.

## 3. MRT Card Trip Checker

Process planned rides in order. Before each ride, add that ride's top-up amount to the balance. If the resulting balance covers the fare, pay it and count a successful ride. Otherwise, skip that ride without deducting its fare. Continue to the next ride either way.

**Inputs:** `balance: int`, `fares: list[int]`, `top_ups: list[int]`. All amounts are nonnegative whole baht. A top-up of zero means no top-up. Matching positions describe one ride.

```python
balance = 40
fares = [25, 30, 20]
top_ups = [0, 0, 50]
```

**Return:** Each ride's paid/skipped status and balance afterward, then final balance and successful-ride count.

**Optional stretch:** Include a low-balance warning whenever the balance after processing a ride is below 20 baht.

## 4. Snack Box Divider

Divide each box equally among the same students. Record how many snacks each student receives from that box and the leftovers. Treat boxes separately: do not combine leftovers and redistribute them.

**Inputs:** `boxes: list[int]` (nonnegative snack counts), `students: int` (at least 1).

```python
boxes = [12, 17]
students = 5
```

**Return:** Each box's snacks-per-student and leftovers, then the total received by each student and total leftovers. Use integer division `//` and remainder `%`.

**Optional stretch:** Add “Perfectly divided!” to the message for each box with zero leftovers.

## 5. Coffee Queue Estimator

Process drink orders in order. A `"simple"` drink takes 2 minutes, `"blended"` takes 4, and `"special"` takes 5. One worker makes drinks sequentially. Record each drink's preparation time and the cumulative time until it is ready. Identify drinks taking longer than a simple drink.

**Input:** `orders: list[str]`, containing only the three types above.

```python
orders = ["simple", "blended", "special"]
```

**Return:** One message per order, then total queue time and its category: under 10 minutes is short; 10–20 inclusive is manageable; above 20 is long.

**Optional stretch:** If the total exceeds 60 minutes, also show whole hours and remaining minutes using `//` and `%`.

## 6. Fitness Streak Tracker

A student records exercise minutes for seven days. A day is active if it includes at least 20 minutes of exercise. The weekly goal is at least four active days.

**Input:** `minutes: list[int]`, exactly seven nonnegative values.

```python
minutes = [20, 0, 30, 15, 25, 20, 0]
```

**Return:** Each day's active/inactive status, then total minutes, active-day count and whether the goal was achieved.

**Optional stretch:** Also report the longest run of consecutive active days. An inactive day breaks the run.

## 7. Dragon Toll Gate

A traveler passes if they have at least 50 gold coins, **or** if they brought a snack **and** the dragon's mood is at least 7. Otherwise, they are blocked. Evaluate each traveler independently; do not update anyone's gold or the mood.

**Inputs:** `gold: list[int]` (nonnegative), `snacks: list[bool]`, `moods: list[int]` (1–10). Matching positions describe one traveler and the dragon's mood when they arrive.

```python
gold = [50, 10, 40]
snacks = [False, True, True]
moods = [2, 7, 6]
```

**Return:** Each traveler's pass/blocked result, then the two totals.

**Optional stretch:** Include the mood category in each message: 7–10 friendly, 4–6 neutral, 1–3 angry.

## 8. Password Strength Batch Checker

Classify each password by length: fewer than 6 characters is too short, 6–9 is acceptable, and at least 10 is strong. These labels describe this exercise's length rule, not a complete security check.

**Input:** `passwords: list[str]`. Individual passwords may be empty strings.

```python
passwords = ["cat", "python", "abcdefghij"]
```

**Return:** Each password's classification, identified by its position, then the count classified as strong.

**Optional stretch:** Also label passwords containing `!` or `?`. Hint: `"!" in password` checks whether that character occurs.

## 9. Movie Ticket Discount Counter

Each customer gets at most one discount: under age 12 gets 50%; age 60 or above gets 30%; a student gets 20%. Use the largest applicable discount. A customer qualifying for none pays the base price.

**Inputs:** `ages: list[int]` (nonnegative), `students: list[bool]`, `base_price: int` (positive whole baht). Matching positions describe one customer.

```python
ages = [10, 20, 65, 35]
students = [True, True, True, False]
base_price = 200
```

**Return:** Each customer's ticket price, then total revenue and number of discounted customers. Decimal results are allowed; no special money formatting is required.

**Optional stretch:** Add a `weekend: bool` parameter. On weekends, add 30 baht to each ticket **after** applying its discount; do not discount the surcharge.

## 10. Food Delivery Fee Log

For each order, start the delivery fee at 20 baht, add 10 baht per kilometre, and add 15 if it is raining. If the order value is at least 300 baht, subtract 20 from the delivery fee. The final amount is the order value plus its delivery fee.

**Inputs:** `values: list[int]`, `distances: list[int]`, `raining: list[bool]`. Values and distances are nonnegative whole numbers. Matching positions describe one order.

```python
values = [200, 300, 450]
distances = [2, 0, 3]
raining = [False, False, True]
```

**Return:** Each order's delivery fee and final amount, then total delivery fees collected.

**Optional stretch:** Add a matching `coupons: list[int]` of nonnegative amounts. Subtract each coupon from its delivery fee after the other rules, but do not let the fee fall below zero.

## 11. Grade Rescue Calculator

For each subject, add the available bonus to the current score. Report whether the adjusted score reaches or exceeds the target. Count every subject that meets its target after the addition, including those that already met it beforehand.

**Inputs:** `scores: list[int]`, `targets: list[int]` (both 0–100), `bonuses: list[int]` (nonnegative). Matching positions describe one subject.

```python
scores = [45, 60, 72]
targets = [50, 70, 70]
bonuses = [5, 5, 0]
```

**Return:** Each subject's adjusted score and target-met status, then the total meeting their targets. For the main task, do not cap adjusted scores.

**Optional stretch:** Cap adjusted scores at 100 before reporting and checking them.

## 12. Pet Feeding Scheduler

Calculate each pet's daily food needs and its total for the specified number of days. Flag pets needing **more than 500 grams per day**.

**Inputs:** `meals_per_day: list[int]`, `grams_per_meal: list[int]`, `days: int`. All values are positive. Matching positions describe one pet; the same number of days applies to all pets.

```python
meals_per_day = [2, 3]
grams_per_meal = [100, 200]
days = 3
```

**Return:** Each pet's daily amount, period total and any large-portion warning; then total food for all pets across all days. If that total is at least 1,000 grams, also report kilograms using grams divided by 1,000.

**Optional stretch:** Add a warning when the overall total exceeds 5,000 grams.

## 13. Magic Potion Mixer

Each potion requires 2 red herbs, 3 blue crystals and 1 bottle. For every requested attempt, check all three supplies. If enough remain, make one potion and subtract the ingredients. Otherwise, consume nothing and record a failed attempt. No supplies are added between attempts.

**Inputs:** `attempts: list[int]` (positive attempt labels), `red: int`, `blue: int`, `bottles: int` (nonnegative supplies). Each list entry means one attempt; its value is a label, not a quantity.

```python
attempts = [1, 2, 3, 4]
red = 7
blue = 9
bottles = 2
```

**Return:** Each attempt's success/failure, then the success count and **all ingredients insufficient at the first failed attempt**. If every attempt succeeds, say there was no failure. Continue recording remaining attempts after a failure.

**Optional stretch:** Also report remaining red herbs, blue crystals and bottles after all attempts.

## 14. Campus Room Direction Helper

Build directions from separate building, floor and room lists. Do not parse a combined room code. Suggest the elevator for floors 3 or above; for floors 1–2, say the elevator is not needed for this exercise.

**Inputs:** `buildings: list[str]`, `floors: list[int]` (at least 1), `rooms: list[str]`. Matching positions describe one room. Room numbers are strings so leading zeros are preserved.

```python
buildings = ["A", "B", "A"]
floors = [1, 2, 4]
rooms = ["101", "205", "402"]
```

**Return:** Each room's building, floor, room number and advice, then the count receiving elevator advice.

**Optional stretch:** Add a high-floor warning for floors above 6.

## 15. Arcade Token Calculator

Each player spends as many of their tokens as possible on full games. Every game costs the same number of tokens and awards the same number of tickets. A player qualifies for a prize with at least 100 tickets.

**Inputs:** `tokens: list[int]` (nonnegative), `cost_per_game: int` (at least 1), `tickets_per_game: int` (nonnegative).

```python
tokens = [12, 7, 3]
cost_per_game = 4
tickets_per_game = 40
```

**Return:** Each player's full-game count, remaining tokens and tickets earned, then the count qualifying for a prize. Use `//` and `%` for games and remaining tokens.

**Optional stretch:** Report the highest prize level each player qualifies for: bronze at 50, silver at 100, gold at 200 tickets; below 50 means no prize.

## 16. Simple Chatbot Response Classifier

Process lowercase messages using this priority:

1. If the message contains the text `help` anywhere, classify it as a help request and respond `"How can I help?"`.
2. Otherwise, if the entire message is `hi` or `hello`, respond `"Hello!"`.
3. Otherwise, if it has more than 50 characters, respond `"Please send a shorter message."`.
4. Otherwise, respond `"Message received."`.

**Input:** `messages: list[str]`, already lowercase for the main task. Empty messages are allowed and receive the normal response. For simplicity, `help` is a substring check, so `helpful` also qualifies. Hint: use `"help" in message`; no word splitting is needed.

```python
messages = ["hi", "please help me", "see you later"]
```

**Return:** One response per message, then the help-request count.

**Optional stretch:** Accept mixed-case messages by applying `.lower()` before checking them.

## 17. Mini Inventory Checker

Check whether each requested item appears in the stock list. Availability does not decrease after a request: this is a catalogue lookup, not a sales simulation. Record every unavailable request, including repeated ones, in a separate list.

**Inputs:** `stock: list[str]`, `requests: list[str]`. Names are lowercase and compared exactly. These lists do **not** need matching lengths.

```python
stock = ["pen", "book", "ruler"]
requests = ["pen", "eraser", "eraser", "book"]
```

**Return:** Each request's available/unavailable status, then a message showing the unavailable-items list. If none are unavailable, show `[]`. Hint: `item in stock` checks membership, and `str(missing_items)` can include a list in a message.

**Optional stretch:** Record each unavailable item only once using a list and a membership check, not a set.

## 18. Temperature Reporter

Convert each temperature from Celsius to Fahrenheit using `F = C * 9 / 5 + 32`. Classify the original Celsius value: below 20 is cool, 20–32 inclusive is warm, and above 32 is hot.

**Input:** `temperatures: list[float]`. Negative temperatures are allowed.

```python
temperatures = [18.0, 30.0, 35.0]
```

**Return:** Each day's Celsius value, Fahrenheit value and category, then the hot-day count. No rounding or fixed decimal formatting is required.

**Optional stretch:** Add a hydration warning to each hot-day message.

## 19. Attendance Streak Checker

Process attendance in session order. Count present and absent sessions and track the longest run of consecutive present sessions. An absence resets the current run, but does not erase the longest run already found.

**Input:** `attendance: list[bool]`, where `True` means present and `False` means absent.

```python
attendance = [True, True, False, True, True, True]
```

**Return:** Each session's status and current streak, then total presents, total absences and longest streak.

**Hint:** Keep separate values for the current streak and longest streak. This is one of the more challenging options.

**Optional stretch:** Add `"Good attendance"` if present sessions are at least 80% of the total; otherwise add `"Attendance needs improvement"`.

## 20. Lucky Number Pattern

Build a pattern that grows by one digit per row. For digit 7 and four rows, return:

```python
["7", "77", "777", "7777"]
```

**Inputs:** `digit: int` (0–9), `rows: int`. If rows is less than 1, return a list containing one warning message instead of a pattern. This problem needs no list input because it generates the list itself.

```python
digit = 7
rows = 4
```

**Return:** A list of pattern rows as strings, or one warning string in a list. Use a loop and grow a string by adding `str(digit)`; nested loops are not required. Do not use string multiplication shortcuts.

**Optional stretch:** After the largest row, add rows in decreasing size without repeating the largest row. With four rows, the lengths should be `1, 2, 3, 4, 3, 2, 1`.

---

# Rubric — 10 Points

The whiteboard criterion assesses the assigned problem. The remaining criteria assess all three submitted problems.

| Criterion | Excellent | Good | Developing | Missing or insufficient |
|---|---|---|---|---|
| Whiteboard solution and explanation — 4 points | **4:** Python function is clearly organized; the group explains the decisions and changing values using a correct trace. All present members contribute. | **3:** Mostly clear code and explanation, with a minor gap in tracing or participation. | **2:** Some useful reasoning, but important steps are unclear or the group mainly reads the code. | **0:** No meaningful board solution or explanation. |
| Inputs and outputs — 2 points | **2:** All three functions use the specified input structures, correct parameter names and type hints, and clearly defined return values. | **1.5:** All three are present with minor type, naming or output-description errors. | **1:** Only one or two are adequately specified, or several input/output details are unclear. | **0:** Inputs and outputs are absent or mostly unusable. |
| Python implementation — 2 points | **2:** All three functions run and correctly implement the core rules, loops, conditions and returns. | **1.5:** All three are attempted and mostly correct, with a limited syntax or logic error. | **1:** At least one meaningful Python solution, but others are missing or contain substantial errors. | **0:** No meaningful Python implementation. |
| Manual traces and Google Sheet — 2 points | **2:** Readable, complete sheet with explanations, board record and two correct manual traces per problem: six in total. | **1.5:** All three problems and six tests are included, but a trace, explanation or board-record detail needs improvement. | **1:** Some useful work, but problems, tests or important trace steps are missing. | **0:** No accessible, usable submission or meaningful traces. |

**Stretch bonus: +1 point per group in total** for correctly completing and tracing one listed stretch challenge. Maximum score including the bonus: **11/10**.
