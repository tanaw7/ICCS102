# ICCS102 / ICCT111 Term Project Instructions

This assignment applies to both **ICCS102** and **ICCT111**.

---

## 1. Project Overview

For the **ICCS102 / ICCT111** term project, you will create a complete Python program that demonstrates what you have learned in this course.

Your project should be a small but working program. It may be a game, utility, simulation, interactive tool, or another suitable Python program approved by the instructor.

The goal is not to create a professional software product. The goal is to show that you can design, build, run, explain, and reflect on a real Python program.

A major part of the score will come from your individual written report. The report is important because it shows your planning, understanding, testing, reflection, use of resources, and personal coding contribution. 

---

## 2. Learning Goals

By completing this project, you should demonstrate that you can:

* write a working Python program
* use Python fundamentals such as variables, data types, conditionals, loops, functions, function signature with correct input and output data types, and data structures
* break a program into smaller parts or features
* use clear names, comments, and basic code organization
* test whether your program works as intended
* explain your own work clearly in a written report
* acknowledge outside resources, AI tools, libraries, and any adapted code honestly
* contribute meaningfully to the actual code of the project

---

## 3. Project Requirements

Your final project must be a **complete Python program** that works and produces the intended results.

* The full project codebase should contain approximately **600–2000 meaningful lines of Python code** in total across all source files.

  The line-count requirements refer to meaningful project code. Blank lines, purely decorative comments, copied code that the student cannot explain, or generated code that the student does not understand should not be counted as meaningful contribution.
* Each student must contribute **at least 100 meaningful lines of code** to the project.
* **Every student must code.**

Your program should include several course concepts that may include:

* variables and data types, input and output, arithmetic or logical expressions, conditionals, loops, strings, lists, tuples, dictionaries, s, readable code structure, comments, and simple header documentation

You may use Python standard libraries or simple beginner-friendly libraries where appropriate.

Examples include:

* `random, math, time, datetime, os`, etc.
* beginner-friendly GUI or game libraries, such as `tkinter`, `turtle`, or `pygame`, if appropriate for the project

Advanced external libraries are not required. Do not choose a project that depends on complex infrastructure or difficult setup.

---

## 4. Suggested Project Types

Possible project types include, but are not limited to:

* a simple game
* a command-line arcade collection
* a memory or matching game
* a slot-machine or chance-based game
* a cooking/order/recipe game
* a survival or movement-based game
* a calculator or converter
* a quiz system
* a simple tracker or organizer
* a simulation
* another Python project approved by the instructor


I also encourage you to build your project based on what you want to do. Feel free to use your full creativity and imagination for this work.

However, it must still be a project that is realistic in scope and can be completed within the term.

---

## 5. Group Work and Individual Contribution

You may work in groups for the project code. The **code may be shared within the group**, but the **final report is individual**.

If a student cannot clearly explain their own coding contribution, or if their contribution is below the required minimum, this may seriously affect their individual project score.

---

## 6. Testing Expectations

You must test your program before submission.

Your report must include **at least 3 manual test cases**. Each test case should show:

* the test case name
* the input or action
* the expected result
* the actual result

You may include more than 3 test cases if needed. Good test cases usually include:

* a normal case
* an edge case
* an invalid or unexpected input case
* a case that checks whether a bug was fixed correctly

You may present your test cases in a table like this:

| Test Case         | Input / Action                               | Expected Result                                   | Actual Result                                       |
| ----------------- | -------------------------------------------- | ------------------------------------------------- | --------------------------------------------------- |
| Start the program | Run `main.py`                                | The main menu appears without errors              | The main menu appeared correctly                    |
| Valid input       | Enter `5` in the menu                        | The program accepts the input and continues       | The program accepted the input and continued        |
| Invalid input     | Enter `abc` instead of a number              | The program shows an error message and asks again | The program showed an error message and asked again |
| Bug fix check     | Load a saved game after fixing file handling | The saved game loads correctly without crashing   | The saved game loaded correctly                     |

Formal automated test files are not required unless specifically requested by the instructor. Simple manual test cases are acceptable for this course.

---

## 7. Required Final Report Structure

Your report must include **all** of the following sections. Missing or very weak sections may reduce your individual report score.

### 1. Project Overview

This section must include:

* the project title
* the group name or group members
* a short description of what the program does
* the purpose or goal of the project
* the main features of the program

### 2. Design and Planning

This section must include:

* a breakdown of the program into different parts (main parts, functions, function input and output data types, features).
* a short explanation of the main program logic
* important data structures, files, variables, images, or other assets used
* **at least 3 test cases** in table form

You do **not** need a professional software-engineering design document. However, this section must show that you thought about how the program should work, not only what the final result looks like.

### 3. Implementation

This section must include:

* the programming language used
* the libraries or modules used
* the main files in the project and what each file does
* important functions or sections of code
* major problems, bugs, or challenges encountered
* how those problems were fixed or handled

You should state the programming language and libraries/modules used in the report. Full run instructions, required Python version, and setup requirements must be placed in `README.md`.

### 4. Individual Coding Contribution

This section must include:

* a clear explanation of what you personally coded
* the files, functions, or features you worked on
* the approximate meaningful lines of code you contributed
* a short explanation of how your contribution works

This section must include a contribution table like this:

| File / Function / Feature                | What I personally coded      | Approx. meaningful lines |
| ---------------------------------------- | ---------------------------- | ------------------------ |
| `example_file.py` / `example_function()` | Explain what you implemented | 40                       |
| `another_file.py` / feature name         | Explain what you implemented | 60                       |
| **Total**                                |                              | **100**                  |

### 5. Results and Reflection

This section must include:

* what parts of the program work successfully
* any known limitations or unfinished parts that you decide to remove from scope
* a short summary of the testing results
* what you learned from the project
* what could be improved in the future

### 6. References and Resources Used

This section must include:

* websites, tutorials, videos, documentation, or class materials used
* Python libraries or modules used
* AI tools used, if any
* borrowed or adapted code, if any
* a clear explanation of what was changed and what you personally contributed

You must write the references using proper citation format such as **ACM, MLA, APA, IEEE, Chicago, and CSE** styles, etc.

---

## 8. Submission Instructions

Each student must submit their own zip file. The code may be the shared group code, but the report must be the student's own individual report.

Your individual final report should be approximately **3–10 pages**, not including appendix material. It may be submitted as **PDF** or **Markdown**. The report should be clear, organized, and written in your own words.

Name your zip file:

```text
[FullName]_[three_leftmost_letters_of_LastName]_Final_Project.zip
```

For example, if your name is **Barnabas Smith**, your zip file should be named:

```text
Barnabas_Smi_Final_Project.zip
```

The zip file should include:

* your final report, as PDF or Markdown
* all Python source code files
* all external assets needed by the program, such as images, audio, text files, or data files
* a `README.md` file containing sufficient instructions for how to run the program, the required Python version, and any required libraries

The submitted project must be runnable.

Make sure that no required file is missing. If the program depends on images, sounds, data files, or other assets, include them in the zip file.

---

## 9. Detailed Rubric

This assignment is graded out of **100 points** for the submitted **code + report**. 

The point levels below are anchor examples. During actual grading, the instructor may award midway points or partial credit depending on the quality of the work.

Criteria **1–5** are graded individually based on each student's report and explanation. Criteria **6–7** are mainly based on the shared group code. However, each student must still meet the individual coding contribution requirement; weak or unclear personal contribution can affect the student's individual score, especially in Criterion 3.

| Criterion                                                         | Excellent                                                                                                                                                                                                                                                                                                                                             | Good                                                                                                                                                               | Satisfactory                                                                                                                                                                                                        | Not Acceptable                                                                                                                                                                     |
| ----------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Project Overview and Purpose — 10 pts**                      | **10 pts** — Clearly explains the project title, group context, purpose, and what the program does. The reader can quickly understand the project and its main features.                                                                                                                                                                              | **8 pts** — Mostly clear explanation with minor missing details. The project goal is understandable.                                                               | **5 pts** — Basic explanation is present, but it may be vague, too short, or not fully clear.                                                                                                                       | **0 pts** — Missing, extremely vague, or the reader cannot understand what the project is.                                                                                         |
| **2. Design and Planning — 20 pts**                               | **20 pts** — Strong planning. Clearly explains the main parts, functions, input and output data types, features, program structure, logic, important data or assets, and includes at least 3 meaningful test cases in table form. Shows thoughtful decomposition before or during coding.                                                                                          | **16 pts** — Good planning. Main features and logic are explained, but some details such as data/assets or test cases may be limited.                              | **10 pts** — Some planning is shown, but it mostly describes the final program rather than explaining design decisions. Test evidence is weak or incomplete.                                                        | **0 pts** — Little or no planning. No clear decomposition, logic explanation, or test consideration.                                                                               |
| **3. Implementation and Individual Coding Contribution — 15 pts** | **15 pts** — Clearly explains how the program was built, the programming language and libraries/modules used, the main files/functions used, input and output data types used in the function signatures, challenges or bugs encountered, and the student's own coding contribution. The contribution table is clear, and the student identifies at least **100 meaningful lines of code** personally contributed. | **12 pts** — Explains implementation and contribution reasonably well, with minor gaps in detail. The contribution table or 100-line contribution is mostly clear. | **8 pts** — Basic implementation explanation is present, functions may lack specified data types, or personal coding contribution is vague, incomplete, or not well connected to specific files/functions. Important implementation details may be missing. | **0 pts** — Implementation section is missing or very weak. Personal coding contribution is unclear, below the 100-line requirement, or the student cannot explain their own code. |
| **4. Results and Reflection — 15 pts**                            | **15 pts** — Clearly explains what works, summarizes testing results, identifies limitations, shows honest reflection, and suggests realistic future improvements.                                                                                                                                                                                    | **12 pts** — Good explanation of results and learning, but testing summary, limitations, or future improvement discussion may be limited.                          | **8 pts** — Basic conclusion is present, but the reflection is generic or shallow.                                                                                                                                  | **0 pts** — Missing or very weak conclusion. Little evidence of learning or reflection.                                                                                            |
| **5. References, Resources, and Academic Honesty — 10 pts**       | **10 pts** — Clearly lists resources, tutorials, documentation, libraries, AI tools, and any borrowed/adapted code. Uses a proper citation style and clearly explains what was changed and what the student personally contributed, or clearly states that no external resources were used.                                                           | **8 pts** — Resources are listed, but some details about citation format, adaptation, AI use, or personal contribution may be slightly unclear.                    | **5 pts** — Some resources are mentioned, but attribution is vague, incomplete, or missing clear explanation of personal contribution. Citation format may be weak or inconsistent.                                 | **0 pts** — Missing references/resources section, unclear source use, or no clear distinction between borrowed/adapted work and the student's own work.                            |
| **6. Code Functionality and Run-ability — 20 pts**                | **20 pts** — Program runs smoothly, major features work correctly, required files/assets are included, and setup is manageable.                                                                                                                                                                                                                       | **16 pts** — Program works with minor issues or small setup problems, but the main features can still be evaluated.                                                | **10 pts** — Program partially works or needs manual fixes before it can be evaluated. Some major features may be incomplete.                                                                                       | **0 pts** — Program does not run, major files are missing, or setup prevents evaluation.                                                                                           |
| **7. Code Organization, Readability, and Style — 10 pts**         | **10 pts** — Code is readable, reasonably organized, uses meaningful names, includes useful comments, and has simple header documentation where appropriate.                                                                                                                                                                                          | **8 pts** — Code is mostly readable and organized, with minor issues in naming, comments, or structure.                                                            | **5 pts** — Code is understandable but messy, repetitive, weakly organized, or has very limited comments.                                                                                                           | **0 pts** — Code is extremely hard to understand, disorganized, or lacks meaningful structure.                                                                                     |

---

## 10. Important Reminders and Final Submission Checklist

This final section is meant to help you avoid common submission problems.

### Important Reminders

* This is a beginner Python course. Your project does not need to be huge or overly complex.
* A smaller project that works correctly is better than an ambitious project that cannot run.
* Each student must contribute at least **100 lines of code**. No exception.
* Your report must explain both the whole group project and your own individual coding contribution.
* Be honest about any resources, tutorials, documentation, AI tools, or borrowed/adapted code used.
* Test your program before submitting. Make sure it runs. Provide in README.md how to run it.
* After creating your zip file, open it again and confirm that all required files are inside.

### Final Submission Checklist

Before submitting, make sure that:

* [ ] Your zip file is named correctly: `[FullName]_[three_leftmost_letters_of_LastName]_Final_Project.zip`
* [ ] Your individual report is included.
* [ ] All Python source code files are included.
* [ ] The full project codebase contains approximately 600–2000 meaningful lines of Python code.
* [ ] All required assets, data files, and external files are included.
* [ ] Instructions for running the program are included in `README.md`.
* [ ] The program runs successfully.
* [ ] Your report clearly explains your individual coding contribution.
* [ ] Your report includes the contribution table.
* [ ] Any resources, AI tools, or adapted code are clearly acknowledged.

---

## 11. Example Folder Structure

Your zip file may be organized in a structure like this:

```text
Barnabas_Smi_Final_Project.zip
│
├── report.pdf
├── README.md
├── main.py
├── game_logic.py
├── player.py
├── utils.py
├── data/
│   ├── levels.json
│   └── scores.txt
├── images/
│   ├── player.png
│   ├── enemy.png
│   └── background.png
└── sounds/
    ├── click.wav
    └── win.wav
```

This is only an example. Your own file names and folders may be different. However, your submission should still be clean, organized, and easy to run.
