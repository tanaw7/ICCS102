# Review Questions

The list below can be used to help you study for the first module. All questions in RAT will be drawn from these questions and their answers. However, beware that the actual wording may vary from the list here. In addition, **do adhere to the mandatory resources** whenever possible when answering questions as your classmates are depending on you to provide good and usable answers for the quiz.

However, be prepared to search for more information from the Web when a term or a topic is not sufficiently addressed in the mandatory resources. In addition, **a question may require additional information resources** than our main ones to answer. When you give reference(s), please specify where corresponding information resides on that particular resource for the benefit of your classmates.

1. **Branching (aka Decision)**
   A. What is branching in programming?
   B. Give a real-life example of branching that can also be applied to real-life activities?

2. **Syntax of if statements in Python**
   A. What is the syntax of a basic if statement?
   B. What is an if-else statement, and how does it differ from a single if statement?
   C. What is an elif statement?

3. Why is **indentation** is very important in the branching syntax of Python?

4. Can we nest if-else statements? Provide an example if possible.

5. **Boolean logic**
   A. What are Booleans?
   B. Why are they essential in decision-making statements?

6. **Logical operators**
   A. What are logical operators?
   B. What are common logical operators in Python. Give code examples to illustrate them.
   C. Why are they essential in decision-making statements?

7. **Comparison (relational) operators**
   A. What is a comparison in programming?
   B. What are common relational operators in Python. Give code examples to illustrate them.
   C. What is the relationship between **Boolean expressions** and comparisons?

8. What is the difference between the `==` and `is` operators?

9. **Boolean functions for string objects**
   A. List additional string functions that return Boolean values.
   B. Give an example for each operator/function listed in (a) along with possible results returned from your examples.

10. Is it a good idea when we use nested branching to solve the [three (not twenty) questions example](https://open.cs.uwaterloo.ca/python-from-scratch/6/6/transcript)? Justify.

11. Provide three sets of values for the parameters `a`, `b`, and `c` that make the code below to return `a`, `b`, and `c`, respectively.

```python
def min_3(a, b, c):
    if a <= b and a <= c:
        return a

    elif b <= a and b <= c:
        return b

    else:
        return c
```

12. What is the process (recipe) discussed in the assigned resource of writing branching statement(s) from a word problem? Explain this in your own words; do not copy the resource.

13. What are examples of iteration/repetition in real life?

14. **Decision VS Repetition**
    A. What is the role of conditions in branching (decision) and iteration (repetition) statements?
    B. In this sense, what are similarities and differences between these two types of statements?

15. How many ways can we make a loop stop (making the condition false)?

16. Trace the execution of the [quotient algorithm](https://open.cs.uwaterloo.ca/python-from-scratch/8/3/transcript) by using the tracing table shown at the end of [Iteration using while (Part 2)](https://open.cs.uwaterloo.ca/python-from-scratch/8/2/transcript). Let's adjust the table a bit to fit this problem. Do the tracing for two sets of input values, one for a couple of loop attempts, and another for 7 attempts or more.

| Loop attempt number | counter before body | Does it enter the loop? | `first` after body | counter after body |
| ------------------- | ------------------- | ----------------------- | ------------------ | ------------------ |
| 1                   |                     |                         |                    |                    |
| 2                   |                     |                         |                    |                    |
| 3                   |                     |                         |                    |                    |
| ...                 |                     |                         |                    |                    |

17. Trace the execution of the [searching in a string](https://open.cs.uwaterloo.ca/python-from-scratch/8/3/transcript) by using the tracing table shown at the end of [Iteration using while (Part 2)](https://open.cs.uwaterloo.ca/python-from-scratch/8/2/transcript). Let's adjust the table a bit to fit this problem. Do the tracing for two sets of input values, one for a couple of loop attempts, and another for 7 attempts or more.

| Loop attempt number | `index` before body | Does it enter the loop? | `word[index]` after body | `index` after body |
| ------------------- | ------------------- | ----------------------- | ------------------------ | ------------------ |
| 1                   |                     |                         |                          |                    |
| 2                   |                     |                         |                          |                    |
| 3                   |                     |                         |                          |                    |
| ...                 |                     |                         |                          |                    |

18. What are possible anatomies of iteration in Python? (There should be at least 2.) Give examples.

19. What is the process (recipe) discussed in the assigned resource of writing iteration statement(s) from a word problem? Explain this in your own words; do not copy the resource.

20. What are similarities and differences of strings and sequences (such as lists) in Python in the concept?

21. The resource has suggested that
    "Using an index will return an item.
    Using slice will return a list."
    Demonstrate this caution with Python code.

22. When should we use one between while and for loops? In the other words, when would a while loop be more suitable than a for loop and vice versa?
