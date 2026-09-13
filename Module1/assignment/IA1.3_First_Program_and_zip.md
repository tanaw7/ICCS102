# Assignment 1.3: Creating, Running, and Submitting a Python File in a ZIP Folder

## Assignment Type

Individual practical computer-skills assignment

## Learning Objectives

By completing this assignment, students should be able to:

* open PyCharm on a Windows computer in the computer lab,
* create or open a working folder in a location they can find again,
* create a new Python source file,
* save and recognize a file with the correct `.py` extension,
* write and run a very small Python program,
* locate the Python file using Windows File Explorer,
* distinguish a Python source file from a Word document, PDF, screenshot, or plain-text document,
* organize assignment files inside a folder,
* compress the folder into a `.zip` file,
* inspect the ZIP file before submission,
* submit the correct file type using the required naming format.

## Duration

Recommended working time: **30–45 minutes**

## Task Description

Some assignments in this course will require you to submit Python source files.

A Python program should normally be saved as an actual **`.py` file**. Putting Python code inside a Word document, PDF, screenshot, or another document does **not** create an executable Python source file.

In this exercise, you will use **PyCharm on a Windows computer in the computer lab** to create a very small Python program, run it, find the actual `.py` file on the computer, and submit it inside a ZIP folder.

### Step 1 – Create Your Assignment Folder

On the Windows computer, create a new folder in a location you can easily find again, such as the **Desktop**.

Use this naming format:

```text
ICCS102_Week1_Zip_[YourFirstName]_[threeLeftMostLettersOfLastName]
```

Example:

```text
ICCS102_Week1_Zip_Somchai_Jai
```

Remember where you created this folder.

### Step 2 – Open PyCharm

1. Open the Windows **Start Menu**.
2. Search for:

```text
PyCharm
```

3. Open PyCharm.

Depending on the version installed in the computer lab, the first screen may look slightly different.

### Step 3 – Open Your Assignment Folder in PyCharm

From the PyCharm welcome screen, choose:

```text
Open
```

Select the assignment folder you created in Step 1.

If PyCharm is already open, use:

```text
File → Open
```

and select the same folder.

If PyCharm asks whether you trust the project or folder, confirm that you trust it because this is the folder you created yourself.

PyCharm may create its own project settings files or folders. You do not need to edit them.

### Step 4 – Create a New Python File

In the **Project** panel on the left side of PyCharm:

1. Right-click your assignment folder.
2. Select:

```text
New → Python File
```

3. Enter:

```text
hello_name
```

PyCharm should create:

```text
hello_name.py
```

The `.py` extension identifies it as a Python source file.

### Step 5 – Write Your Program

Inside `hello_name.py`, type:

```python
print("Hello World")
print("My name is Somchai")
```

Replace `Somchai` with your own first name.

Your final program should contain at least these two `print()` statements.

Do not paste the program into Word, Google Docs, or a PDF. The program belongs inside the `.py` file.

### Step 6 – Save the File

PyCharm normally saves your work automatically, but you should still know how to save manually.

Use:

```text
File → Save All
```

or press:

```text
Ctrl + S
```

Your file should remain inside the assignment folder you opened in PyCharm.

### Step 7 – Run the Python Program

Run `hello_name.py`.

You can usually do this by:

1. Right-clicking inside the Python file and choosing:

```text
Run 'hello_name'
```

or

2. Using the green **Run** button in PyCharm.

If PyCharm asks you to configure or choose a Python interpreter, follow the instructor's directions in class.

Your output should be similar to:

```text
Hello World
My name is Somchai
```

Your own name should appear in the second line.

If the program does not run, check:

* that the file is named `hello_name.py`,
* that both `print()` statements contain matching quotation marks,
* that the parentheses are correct,
* that you have saved the file,
* that PyCharm is running the correct file.

### Step 8 – Find the Actual `.py` File in Windows

You should know where your own work is stored.

1. Open **Windows File Explorer**.
2. Navigate to the assignment folder you created earlier.
3. Find:

```text
hello_name.py
```

Confirm that the file is physically inside your assignment folder.

If Windows hides file extensions on the lab computer, ask the instructor how to display them. You should still understand that this is a `.py` Python source file.

### Step 9 – Create a Student Information File

Inside the same assignment folder, create a plain-text file named:

```text
student_info.txt
```

Inside the file, write:

```text
Name: Your full name
Student ID: Your student ID
Section: Your ICCS102 section
```

At minimum, your assignment folder should now contain:

```text
ICCS102_Week1_Zip_Somchai_Jai/
├── hello_name.py
└── student_info.txt
```

PyCharm may also have created project-setting files or folders. That is acceptable.

### Step 10 – Compress the Whole Assignment Folder

Close files or PyCharm if necessary.

In Windows File Explorer:

1. Find the assignment folder.
2. Right-click the folder.
3. Choose:

```text
Compress to ZIP file
```

On some Windows versions, this may appear as:

```text
Send to → Compressed (zipped) folder
```

This should create a `.zip` file.

### Step 11 – Check Your ZIP File

Before submitting:

1. Open or extract the ZIP file.
2. Confirm that your assignment folder is inside it.
3. Confirm that `hello_name.py` is present.
4. Confirm that `student_info.txt` is present.
5. Open `hello_name.py` and confirm that your Python code is still there.
6. Confirm that the Python file is an actual `.py` file.

Do not assume that the ZIP file is correct simply because the ZIP file exists.

### Step 12 – Submit the ZIP File

Submit the final `.zip` file to Google Classroom.

Do **not** submit:

* a `.rar` file,
* a `.7z` file,
* a Word document containing Python code,
* a PDF containing Python code,
* a screenshot of Python code,
* only the individual files without the required ZIP,
* a shortcut to the folder,
* an empty ZIP file,
* a ZIP file that does not contain the required `.py` file.

## AI Policy

**No AI assistance is allowed for this assignment.**

Do not use ChatGPT, Gemini, Claude, GitHub Copilot, PyCharm AI Assistant, or any other generative AI tool to write, complete, correct, explain, or rewrite the Python code or assignment contents.

You may use the assignment instructions, class demonstrations, course materials, and ask the instructor or teaching assistants for help.

The purpose of this exercise is for you to perform these basic computer and Python tasks yourself.

## Submission and File Naming Format

Submit **one `.zip` file** to the Google Classroom assignment.

Use this filename:

```text
ICCS102_Week1_Zip_[YourFirstName]_[threeLeftMostLettersOfLastName].zip
```

Example:

```text
ICCS102_Week1_Zip_Somchai_Jai.zip
```

The ZIP file must contain at least:

```text
hello_name.py
student_info.txt
```

## Rubric

| Criteria | Excellent | Good | Satisfactory | Unsatisfactory |
|---|---|---|---|---|
| Python file creation and execution | **2 pts:** `hello_name.py` is a valid Python source file, contains the required program, and runs correctly. | **1.5 pts:** Python file is valid and mostly correct with one minor issue. | **1 pt:** Python file exists but has errors, incorrect content, or was not successfully demonstrated as runnable. | **0–0.5 pts:** Python source file is missing, saved in the wrong format, or substantially unusable. |
| ZIP file and folder structure | **2 pts:** Valid ZIP file contains the correctly organized folder and all required files. | **1.5 pts:** ZIP works and required files are present, with one minor organizational issue. | **1 pt:** ZIP is usable but has several structure or organization problems. | **0–0.5 pts:** ZIP is invalid, substantially incomplete, or required files are missing. |
| Naming and submission requirements | **1 pt:** Folder, ZIP, Python file, and student information follow all instructions correctly. | **0.75 pts:** One minor naming or submission issue. | **0.5 pts:** Several instructions are not followed, but the submission can still be assessed. | **0–0.25 pts:** Naming and submission requirements are largely incorrect or missing. |

**Total: 5 points**x
