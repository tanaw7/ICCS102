# ICCS 102 – Module 3 Assignment v1.0

# Whiteboard Algorithm Function Challenge

## Assignment Type

In-class group assignment

Groups of **3 students**

Students should be placed into **new temporary groups**, not their usual class/project groups.

---

# Activity Overview

Your group will work on **3 randomized programming problems**.

Your group will present **1 problem** on the **whiteboard** and submit **3 solved problems** in the Google Doc.

Each solution should be written as a **function** or Python-like function.

The function should show:

* function name,
* input parameters,
* input data types,
* main algorithm,
* output or return value,
* output data type.

The goal is not perfect Python syntax. The goal is to design a clear function-style algorithm and explain it clearly.

---

# Learning Objectives

By completing this activity, students should be able to:

* understand a problem and identify useful inputs,
* write a function-style solution,
* identify input and output data types,
* use repeated steps and decisions in an algorithm,
* explain how an algorithm progresses step by step,
* manually trace an algorithm using test cases,
* present a programming solution clearly as a group.

---

# Time Plan

This activity may take **1–2 class sessions**, depending on the number of groups.

Flow:

* Group formation and naming, and problem assignment: **5 minutes**
* Group discussion and rough planning: **10–15 minutes**
* Whiteboard rounds: **3 groups write on the board at the same time**
* Whiteboard solution writing: **about 5 minutes per round**
* Group presentation: **about 5 minutes per presenting group**
* Audience Bug Bounty: **up to 5 minutes per presenting group**
* Instructor feedback and wrap-up: **5–10 minutes**

If not all groups present in one class session, the activity will continue in the next class.

---

# Main Whiteboard Task

For the whiteboard presentation, your group should present **1 problem**.

On the whiteboard, your group should show:

1. **Function signature**

Example:

```python
calculate_budget(items: list, budget: float) -> str
```

2. **Algorithm / pseudocode / Python-like code**

Your solution may be written as pseudocode, Python-like code, actual Python. It should still look like a function-based solution.

3. **One quick test case**

Show at least one example input and expected output on the board.

You may write the test case as a small table.

Example:

| Test Case | Problem | Input                                                                 | Important Step / Check                 | Expected Output                                       |
| --------- | ------- | --------------------------------------------------------------------- | -------------------------------------- | ----------------------------------------------------- |
| 1         | a       | `items = [("rice", 40), ("drink", 25)]`, `budget = 100`               | total = 65, total <= budget            | `Within budget, 35 baht left`                         |
| 2         | a       | `items = [("rice", 40), ("drink", 25), ("cake", 50)]`, `budget = 100` | total = 115, total > budget            | `Over budget by 15 baht`                              |
| 3         | b       | `temperatures = [18, 30, 35]`                                         | 18 = cool, 30 = warm, 35 = hot         | `1 hot day`                                           |
| 4         | c       | `boxes = [12, 17]`, `students = 5`                                    | 12 // 5 = 2 left 2; 17 // 5 = 3 left 2 | `Each student gets 5 snacks total, 4 leftovers total` |

For problems with repeated steps, show at least one row that explains what happens during the loop.

4. **Explanation**

During the presentation, explain what happens step by step as your algorithm runs.

Do not only read the code. Explain the logic.

Example explanation style:

> First, the function starts with a total of 0. Then it checks each item one by one. After adding an item, it compares the total with the budget. If the total is over budget, it changes the message. At the end, it returns the final result.

---

# Audience Bug Bounty

During another group's presentation, any individual student may point out a possible issue or suggest a fix.

Examples:

* missing input,
* unclear output,
* wrong data type,
* missing condition,
* missing repeated step,
* calculation mistake,
* test case that would break the algorithm.

This is **first come, first serve**.

A useful comment or fix may earn **+0.5 individual bonus point**. (Max accumulative 3 pts)

The instructor has the final say on whether the bonus point is awarded.

Collaborative effort: If the help is successful, the presenting group gets 0.5 pts as well.

---

# Google Doc Submission

Submit one short Google Doc as a PDF.

The document should contain **3 solved problems**.

The problem presented on the whiteboard may be one of the 3 submitted problems.

The document should be clear but does **not** need to be long.

## Required Sections

Keep this document concise. It should record your solution clearly, not become a long report.

### 1. Group Information

* group name,
* group members,
* the 3 selected problem numbers and titles,
* the problem presented on the whiteboard.

### 2. Function Design

For each of the 3 problems, write your function signature and identify inputs/outputs.

Example format:

| Name         | Meaning         | Type          | Example         |
| ------------ | --------------- | ------------- | --------------- |
| `items`      | item prices     | list of float | `[35, 40, 25]`  |
| `budget`     | available money | float         | `100.0`         |
| return value | final summary   | str           | `Within budget` |

### 3. Algorithm Explanation

For each of the 3 problems, briefly explain how your algorithm works in **5–8 steps**.

### 4. Whiteboard Solution

Include a photo, screenshot, or typed copy of your whiteboard solution for the problem your group presented.

### 5. Manual Trace

Show at least **2 test cases per submitted problem**.

For each test case, include:

* input,
* important repeated steps or decision checks,
* expected output.

Make a table for the test cases and their inputs, checks, outputs.

---

# Suggested Python Ideas

You may use:

```python
function definition
parameters
return
print()
if / elif / else
for loop
while loop
list
append()
len()
range()
int()
float()
str()
%      # remainder / modulus
//     # integer division
+ - * /
```

You may write Python-like pseudocode if you are not sure about exact syntax.

---

# Randomized Problem Options

The instructor will assign or approve 3 problems for your group. One of these problems will be presented on the whiteboard.

Each problem is designed to require repeated checking and decision-making. The problem statement does not directly tell you what variables, loops, or conditions to use. Your group must infer those from the situation.

---

## Problem 1: Canteen Budget Tracker

A student visits the campus canteen with a fixed amount of money. They buy several food or drink items one by one. Each item has a name and price. After each item, the student wants to know whether they are still within budget or whether they have already spent too much.

At the end, the student wants a final summary of total spending and remaining money, or how much extra money would be needed.

Stretch challenge:

* Apply a 10% discount if the total spending reaches at least 100 baht.

---

## Problem 2: Rainy Week Campus Planner

A student checks the weather forecast for several school days. For each day, the forecast includes the chance of rain, umbrella status, and walking distance to class.

The student wants a daily recommendation such as walking normally, walking with caution, leaving earlier, or finding another way to class.

For this problem, a day is considered risky for walking if the rain chance is **70% or higher** and the student has no umbrella. A walking distance above **800 meters** should also trigger advice to leave earlier.

At the end, the student wants to know how many days were risky for walking.

Stretch challenge:

* Add temperature to each day and warn about very hot days. A temperature of **35°C or higher** counts as very hot.

---

## Problem 3: MRT Card Trip Checker

A student plans several MRT rides in one day. The card starts with a balance. Each ride has a fare. Before each ride, the student may or may not top up the card.

The card balance should be updated as the rides happen. Each ride should be checked to see whether it can be paid for.

At the end, the student wants to know the final balance and how many rides were successfully paid.

Stretch challenge:

* Warn whenever the balance drops below 20 baht.

---

## Problem 4: Snack Box Divider

A class has several snack boxes to divide among students. Each box may contain a different number of snacks. For every box, the snacks should be divided equally among the students, and leftovers should be recorded.

At the end, the class wants to know the total snacks each student received and the total leftovers from all boxes.

Stretch challenge:

* Print `Perfectly divided!` for any box with no leftovers.

---

## Problem 5: Coffee Queue Estimator

A cafe has a queue of several drink orders. Each order is one of these types: simple, blended, or special.

A simple drink takes **2 minutes**, a blended drink takes **4 minutes**, and a special drink takes **5 minutes**.

The cafe wants to estimate the total waiting time and identify any orders that take longer than a simple drink.

At the end, the cafe wants a message saying whether the queue is short, manageable, or long. Use these categories: **under 10 minutes = short**, **10–20 minutes = manageable**, and **more than 20 minutes = long**.

Stretch challenge:

* Convert the total waiting time into hours and minutes if it is more than 60 minutes.

---

## Problem 6: Fitness Streak Tracker

A student records exercise minutes for several days. For each day, the student wants to know whether it counts as an active day.

A day counts as active if the student exercised for **20 minutes or more**.

At the end, the student wants to know the total exercise time, the number of active days, and whether their weekly exercise goal was achieved. The weekly goal is reached if there are at least **4 active days**.

Stretch challenge:

* Track the longest streak of active days.

---

## Problem 7: Dragon Toll Gate

Several travelers arrive at a bridge guarded by a dragon. Each traveler has some gold coins, may or may not bring a snack, and faces a dragon with a mood level from **1 to 10**.

For each traveler, the dragon decides whether to let them pass. A traveler may pass if they have at least **50 gold coins**, or if they brought a snack and the dragon mood is at least **7**.

At the end, the dragon wants to know how many travelers passed and how many were blocked.

Stretch challenge:

* Print different messages for friendly dragon, neutral dragon, and angry dragon. Mood **7–10** is friendly, **4–6** is neutral, and **1–3** is angry.

---

## Problem 8: Password Strength Batch Checker

A website checks several new passwords created by users. Each password must be judged as too short, acceptable, or strong.

A password is **too short** if it has fewer than **6 characters**, **acceptable** if it has **6–9 characters**, and **strong** if it has **10 or more characters**.

For every password, the website gives feedback.

At the end, the website wants to know how many passwords were strong.

Stretch challenge:

* Add a special label for passwords containing `!`, `?`, or a number.

---

## Problem 9: Movie Ticket Discount Counter

A cinema sells tickets to several customers. Each customer may have a different age and student status. Each customer receives at most one discount.

Children under **12** receive a **50% discount**. Students receive a **20% discount**. Seniors aged **60 or above** receive a **30% discount**. If a customer qualifies for more than one discount, use only the largest discount.

For every customer, the cinema calculates the final ticket price.

At the end, the cinema wants to know the total revenue and how many customers received a discount.

Stretch challenge:

* Add a weekend surcharge of 30 baht per ticket.

---

## Problem 10: Food Delivery Fee Log

A delivery app processes several orders. Each order has an order value, delivery distance, and weather condition.

The delivery fee starts at **20 baht**. Add **10 baht per kilometer**. If it is raining, add **15 baht**. If the order value is at least **300 baht**, subtract **20 baht** from the delivery fee.

For each order, the app calculates the delivery fee and final amount.

At the end, the app wants to know the total delivery fees collected.

Stretch challenge:

* Make sure no delivery fee becomes negative after discounts.

---

## Problem 11: Grade Rescue Calculator

A student checks several subjects. Each subject has a current score, a target score, and possible bonus points.

For each subject, the student wants to know whether the target can be reached after adding the bonus.

At the end, the student wants to know how many subjects were successfully rescued.

Stretch challenge:

* Cap each final score at 100.

---

## Problem 12: Pet Feeding Scheduler

A pet owner prepares food for several pets over several days. Each pet may have a different number of meals per day and a different amount of food per meal.

The owner wants to calculate the total food needed and identify any pet that needs an unusually large amount of food. For this problem, a pet needs an unusually large amount of food if it needs more than **500 grams per day**.

At the end, the owner wants the total food amount in grams and, if the total reaches at least **1000 grams**, also show it in kilograms.

Stretch challenge:

* Add a warning if the total food needed is more than 5 kilograms.

---

## Problem 13: Magic Potion Mixer

A wizard wants to make several potions. Each potion requires **2 red herbs**, **3 blue crystals**, and **1 empty bottle**. The wizard has limited ingredients.

For each potion attempt, the algorithm checks whether enough ingredients remain. If yes, the potion is made and ingredients are used. If not, the attempt fails.

At the end, the wizard wants to know how many potions were successfully made and which ingredient or ingredients caused the first failed attempt.

Stretch challenge:

* Track leftover ingredients after all attempts.

---

## Problem 14: Campus Room Direction Helper

Several students need directions to different rooms. Each room code contains a building letter, floor number, and room number.

For each room, the helper gives a direction message. If the floor is **3 or above**, the helper suggests using the elevator. If the floor is **1**, no elevator is needed.

At the end, the helper reports how many rooms required elevator advice.

Stretch challenge:

* Add a warning for rooms above floor 6.

---

## Problem 15: Arcade Token Calculator

Several players visit an arcade. Each player has a number of tokens, each game costs a certain number of tokens, and each completed game gives tickets.

For each player, the arcade wants to know how many full games can be played, how many tokens remain, and how many tickets are won.

At the end, the arcade wants to know how many players earned enough tickets for a prize. A player needs at least **100 tickets** to receive a prize.

Stretch challenge:

* Add different prize levels for 50, 100, and 200 tickets.

---

## Problem 16: Simple Chatbot Response Classifier

A chatbot receives several user messages. Each message may be a greeting, a help request, a long message, or a normal message.

For this problem, `hi` and `hello` count as greetings. Any message containing the word `help` counts as a help request. A message with more than **50 characters** counts as a long message.

For every message, the chatbot chooses a suitable response.

At the end, the chatbot reports how many messages were help requests.

Stretch challenge:

* Convert each message to lowercase before checking.

---

## Problem 17: Mini Inventory Checker

A small shop has a list of items in stock. Several customers ask for items one by one.

For each requested item, the shop reports whether the item is available. If it is not available, the shop records it in a requested-items list.

At the end, the shop wants to see all unavailable items that customers asked for.

Stretch challenge:

* Avoid adding the same unavailable item more than once.

---

## Problem 18: Temperature Reporter

A weather app records temperatures for several days. Each temperature is in Celsius.

For each day, the app converts the temperature to Fahrenheit and classifies the weather. Below **20°C** is cool, **20°C to 32°C** is warm, and above **32°C** is hot.

At the end, the app reports how many hot days occurred.

Formula:

```text
F = C * 9 / 5 + 32
```

Stretch challenge:

* Print a hydration warning for hot days.

---

## Problem 19: Attendance Streak Checker

A student records attendance for several class sessions. Each session is marked as present or absent.

For each session, the algorithm updates the attendance count and tracks whether the current attendance streak continues or breaks.

At the end, the student wants to know total presents, total absences, and the longest streak of consecutive present sessions.

Stretch challenge:

* Print `Good attendance` if the student was present for at least 80% of the sessions.

---

## Problem 20: Lucky Number Pattern

A student wants to print a lucky number pattern using a chosen number and number of rows.

Example:

```text
lucky number = 7
rows = 4
```

Possible output:

```text
7
77
777
7777
```

The pattern should grow row by row. If the number of rows is less than **1**, the algorithm should show a warning instead of printing a pattern.

Stretch challenge:

* Print the pattern backward after printing it forward.

Example:

```text
7
77
777
7777
777
77
7
```

---

# Submission Format

Submit one group Google Doc as a **PDF**.

Your submission should include **3 solved problems**.

## File Naming Format

```text
ICCS102_Week6_FunctionChallenge_GroupName.pdf
```

Example:

```text
ICCS102_Week6_FunctionChallenge_GroupDragon.pdf
```

---

| Criteria                             | Excellent                                                                                                                     | Good                                                                                    | Satisfactory                                                                     | Not Acceptable                                             |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| Whiteboard function and presentation | 4 pts: Function-style solution is clear, organized, and explained step by step as the algorithm progresses.                   | 3 pts: Mostly clear function-style solution and understandable explanation.             | 2 pts: Some clear ideas, but board solution or explanation has important gaps.   | 0 pts: No meaningful board solution or presentation.       |
| Inputs and outputs                   | 2 pts: Clearly identifies function parameters, input types, output/return value, and output type.                             | 1.5 pts: Mostly identifies inputs and outputs with minor missing details.               | 1 pt: Inputs/outputs are present but types or meanings are unclear.              | 0 pts: Inputs and outputs are missing or mostly incorrect. |
| Algorithm logic                      | 2 pts: Logic is sound, handles repeated work and decision-making appropriately, and would likely work if converted to Python. | 1.5 pts: Logic is mostly correct but has minor gaps.                                    | 1 pt: Some useful logic is present but important parts are missing or incorrect. | 0 pts: Algorithm is missing or not understandable.         |
| Manual trace and Google Doc          | 2 pts: Google Doc is readable and includes 2 useful test cases with inputs, key steps/checks, and expected outputs.           | 1.5 pts: Google Doc is mostly complete, but test cases or explanation could be clearer. | 1 pt: Google Doc is incomplete or test cases are weak.                           | 0 pts: Google Doc is missing or not usable.                |
| Stretch challenge bonus              | +1 pt: Awarded if the group meaningfully attempts and completes the stretch challenge.                                        |                                                                                         |                                                                                  |                                                            |
| Presenting group correction bonus    | +0.5 pt: Awarded if the presenting group successfully corrects or improves their solution after useful feedback.              |                                                                                         |                                                                                  |                                                            |
| Individual Bug Bounty bonus          | +0.5 pt per useful comment or fix accepted by the instructor. First come, first serve. Maximum +3 pts per individual student. |                                                                                         |                                                                                  |                                                            |

Main score: **10 points**

Bonus:

* Stretch challenge: **+1 group bonus**
* Presenting group correction: **+0.5 group bonus**
* Individual Bug Bounty: **+0.5 per accepted help, up to +3 per individual student**

---

* Can you trace it with one example?
* What would the function return or print exactly?
