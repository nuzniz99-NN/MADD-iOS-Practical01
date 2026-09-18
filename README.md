# SE4041 – Mobile Application Design & Development  
## Practical 01 – Swift Fundamentals

**Duration:** 2 Hours  
**Module:** SE4041 – Mobile Application Design & Development   
**Language:** Swift

---

## Practical Overview

In this practical, you will begin programming with **Swift**, the programming language used throughout this module for native iOS application development.

This practical focuses on the fundamental concepts introduced in Lecture, including constants and variables, Swift data types, type inference, type conversion, operators, strings, string interpolation, and optional.

You will complete a series of guided exercises and finish the practical with an individual programming task that combines the concepts you have learned.

At the end of the practical, you must commit and push your completed work to your GitHub repository.

---

## Learning Objectives

By the end of this practical, you should be able to:

- Declare constants and variables using `let` and `var`.
- Use common Swift data types.
- Explain type inference and type safety.
- Perform explicit type conversion.
- Use arithmetic, comparison, and logical operators.
- Work with strings and string interpolation.
- Declare and use optional values.
- Safely unwrap optionals using `if let`.
- Use the nil-coalescing operator `??`.
- Combine multiple Swift concepts in a simple program.

---

## Practical Environment

You may complete this practical using either of the following options.

### Option 1 – Xcode Playground

Open **Xcode** on a Mac.

Create a new Swift Playground using:

**File → New → Playground**

Choose a blank Playground.

A Playground allows you to run Swift code immediately without creating a complete iOS application.

### Option 2 – Swift Playgrounds

You may also complete the practical using **Swift Playgrounds** on a supported Apple device.

Open or create a **blank playground book/page** that allows free-form Swift code, and complete the same exercises. Where available, use **File → New Blank Playground** on Mac or the **Blank** playground template. Menu names and available templates can vary by version; if you cannot find a blank code page, ask your instructor to help you open a suitable playground book.

Use a code page that runs `print("Hello, Swift!")` and shows its output. A **New App** template is intended for app development and is not the code-page setup used by this sheet.

The Swift code used in this practical is the same in both environments. No complete iOS application is required.

For environment guidance, see [Apple's playground setup instructions](https://www.apple.com/au/education/docs/app-design-workbook-AU.pdf) and [Xcode Playgrounds](https://developer.apple.com/videos/play/wwdc2020/10096/).

---

## Exercise 0 – GitHub Repository Setup

Before beginning the programming exercises:

1. Log in to your GitHub account.
2. Open the GitHub Classroom link provided by your instructor.
3. Accept the assignment.
4. Open or clone your practical repository.
5. Create the files required for this practical, following the structure below.

If you are working on a Mac with Git, copy your assignment repository's clone URL from GitHub. In Terminal, replace the example URL below with that URL:

```bash
git clone [https://github.com/YOUR-CLASSROOM/YOUR-ASSIGNMENT-REPOSITORY.git SE4041-Practical-01
cd SE4041-Practical-01](https://github.com/nuzniz99-NN/MADD-iOS-Practical01.git)
```

If you already cloned the repository, open its folder instead of cloning it again. Keep all submission files inside that folder.

If you are using Swift Playgrounds without a local Git workflow, use your repository's **Add file → Create new file** or **Upload files** options to save your Swift source files and screenshots, then commit the changes in GitHub.

Recommended repository structure:

```text
SE4041-Practical-01/
│
├── README.md
├── Exercise01.swift
├── Exercise02.swift
├── Exercise03.swift
├── Exercise04.swift
├── Exercise05.swift
├── Exercise06.swift
├── FinalChallenge.swift
│
└── screenshots/
```

### How to Work Through the Exercises

1. Run each exercise in its own Playground or Playground page. Use the code editor and show the console/output area to view `print()` results.
2. When a step repeats an existing declaration, **replace the earlier example** rather than pasting both versions together. This avoids “invalid redeclaration” errors.
3. Predict the output, run the example, and then complete the activity yourself.
4. Save a working version of each exercise's code as the corresponding `.swift` file listed above. For an Xcode Playground, copy the page's source code into that file; for Swift Playgrounds, copy the editable page's code into a plain-text Swift file or GitHub's file editor.
5. Keep separate exercises independent. The `.swift` files are your source-code submissions; simply placing them in a Playground's `Sources` folder does not run them as separate exercises.
6. Remove or comment out intentional error examples before saving your final version. Add brief comments recording what you observed.

You should commit your work as you progress through the practical.

Example commit messages:

```text
Complete Exercise 01
Complete Exercise 02
Complete optional exercises
Complete Practical 01 final challenge
```

---

## Exercise 01 – Constants and Variables

### Suggested Time: 10 Minutes

Swift provides two main ways of storing values:

```swift
let
```

and

```swift
var
```

`let` creates a **constant**.

A constant receives a value once and cannot later be reassigned.

`var` creates a **variable**.

A variable can change while the program is running.

---

## Step 1 – Create Your First Values

Create `Exercise01.swift`.

Enter the following code:

```swift
let campus = "Malabe"
var studentCount = 40

print(campus)
print(studentCount)
```

Run the program.

Expected output:

```text
Malabe
40
```

---

## Step 2 – Change a Variable

Modify the program:

```swift
let campus = "Malabe"
var studentCount = 40

studentCount = 45

print(campus)
print(studentCount)
```

Expected output:

```text
Malabe
45
```

This works because `studentCount` was created using `var`.

---

## Step 3 – Experiment with a Constant

Try adding:

```swift
campus = "Metro"
```

Run the program.

You should receive a compiler error.

Why?

Because `campus` was declared using:

```swift
let
```

The value of a constant cannot be reassigned.

Remove the incorrect line before continuing.

---

## Activity 1

Create suitable variables or constants for the following:

```text
Module Code
Module Name
Student Name
Student Age
Number of Students
```

Use:

```swift
let
```

for values that should not change and:

```swift
var
```

for values that may change.

Increase the number of students by `5`.

Print all values.

---

## Exercise 02 – Swift Data Types and Type Inference

### Suggested Time: 10 Minutes

Create `Exercise02.swift`.

Every value in Swift has a type.

Some common Swift data types are:

| Type | Purpose | Example |
|---|---|---|
| `Int` | Whole numbers | `25` |
| `Double` | Decimal numbers | `3.75` |
| `Bool` | `true` or `false` | `true` |
| `String` | Text | `"Swift"` |
| `Character` | A single character | `"A"` |

These are the core value types introduced in Lecture 02.

---

## Step 1 – Type Inference

Enter:

```swift
let studentName = "Kamal"
let studentAge = 22
let gpa = 3.65
let isRegistered = true

print(type(of: studentName))
print(type(of: studentAge))
print(type(of: gpa))
print(type(of: isRegistered))
```

Expected output:

```text
String
Int
Double
Bool
```

You did not explicitly specify the data types.

Swift identified the types automatically.

This is called **type inference**.

Swift is also **type safe**, meaning that once a variable has a type, Swift will not allow an incompatible type to be assigned to it.

---

## Step 2 – Type Annotations

You can also specify a type manually.

```swift
let studentName: String = "Kamal"
let studentAge: Int = 22
let gpa: Double = 3.65
let isRegistered: Bool = true
let grade: Character = "A"
```

The syntax is:

```text
variableName: DataType
```

---

## Activity 2

Create variables to represent:

```text
Student ID
Student Name
Year
GPA
Registered Status
Grade
```

Use an explicit type annotation for at least **three** of the values. Represent Student ID as a `String` and Grade as a `Character`.

Print all values.

---

## Exercise 03 – Type Conversion and Operators

### Suggested Time: 15 Minutes

Create `Exercise03.swift`.

Swift does not automatically mix different numeric types.

For example:

```swift
let students = 42
let average = 3.75
```

The following will not work:

```swift
// let result = students + average
```

because:

```text
students → Int
average  → Double
```

You need to explicitly convert one of the values.

```swift
let result = Double(students) + average

print(result)
```

Expected output:

```text
45.75
```

Swift deliberately requires explicit conversion when working with different numeric types.

---

## Step 1 – Arithmetic Operators

Try the following:

```swift
let a = 17
let b = 5

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a % b)
```

Expected output:

```text
22
12
85
3
2
```

The operators are:

```text
+    Addition
-    Subtraction
*    Multiplication
/    Division
%    Remainder
```

Notice:

```swift
17 / 5
```

produces:

```text
3
```

not:

```text
3.4
```

This happens because both values are integers. Integer division produces an integer result.

To obtain a decimal result:

```swift
let result = Double(a) / Double(b)

print(result)
```

Expected:

```text
3.4
```

---

## Step 2 – Calculate an Average

Create:

```swift
let mark1 = 75
let mark2 = 82
let mark3 = 68
```

Calculate the total:

```swift
let total = mark1 + mark2 + mark3
```

Then calculate the average:

```swift
let average = Double(total) / 3.0
```

Print both.

Expected:

```text
Total: 225
Average: 75.0
```

---

## Step 3 – The Remainder Operator

Create:

```swift
let number = 28
```

Use:

```swift
number % 2
```

to determine whether the number is even.

Example:

```swift
print(number % 2)
```

Expected:

```text
0
```

If the remainder after dividing by `2` is `0`, the number is even.

---

## Exercise 04 – Comparison and Logical Operators

### Suggested Time: 10 Minutes

Create `Exercise04.swift`.

Comparison operators compare two values and produce a Boolean result.

Try:

```swift
let mark = 72

print(mark == 72)
print(mark != 72)
print(mark > 50)
print(mark < 50)
print(mark >= 50)
print(mark <= 100)
```

Try predicting the results before running the program.

---

## Logical Operators

Three important logical operators are:

```text
&&    AND
||    OR
!     NOT
```

Consider:

```swift
let mark = 68
let submittedAssignment = true

let passed = mark >= 50 && submittedAssignment

print(passed)
```

Expected:

```text
true
```

For this expression to be `true`:

```swift
mark >= 50
```

and:

```swift
submittedAssignment
```

must both be true.

---

## Try OR

```swift
let hasStudentID = false
let hasTemporaryPass = true

let canEnter = hasStudentID || hasTemporaryPass

print(canEnter)
```

Expected:

```text
true
```

Only one condition needs to be true when using `||`.

---

## Try NOT

```swift
let isAbsent = false

print(!isAbsent)
```

Expected:

```text
true
```

`!` reverses a Boolean value.

---

## Activity 3

Create:

```swift
let examMark = 60
let attendance = 85
```

Create a Boolean called:

```swift
eligible
```

A student is eligible when:

```text
Exam Mark >= 50
AND
Attendance >= 80
```

Print the final result.

---

## Exercise 05 – Strings and String Interpolation

### Suggested Time: 10 Minutes

Create `Exercise05.swift`.

A `String` stores text.

Example:

```swift
let firstName = "Kamal"
let lastName = "Perera"
```

Strings can be combined:

```swift
let fullName = firstName + " " + lastName

print(fullName)
```

Expected:

```text
Kamal Perera
```

---

## String Interpolation

Swift provides an easier way to include values inside text.

```swift
let name = "Kamal"
let age = 22

print("My name is \(name) and I am \(age) years old.")
```

Expected:

```text
My name is Kamal and I am 22 years old.
```

The syntax:

```swift
\(value)
```

inserts the value into the string.

---

## Try This

```swift
let module = "SE4041"
let mark = 78

print("The student received \(mark) marks for \(module).")
```

Expected:

```text
The student received 78 marks for SE4041.
```

---

## Activity 4

Create the following:

```swift
let name = "Your Name"
let year = 4
let semester = 2
let gpa = 3.65
```

Display a sentence similar to:

```text
Kamal is a Year 4 Semester 2 student with a GPA of 3.65.
```

You must use **string interpolation**.

---

## Exercise 06 – Understanding Optionals

### Suggested Time: 20 Minutes

Create `Exercise06.swift`.

Optionals are an important part of Swift.

Sometimes a variable may contain a value.

Sometimes that value may not exist.

Swift represents this using an **optional**.

An optional type is written using:

```swift
?
```

Example:

```swift
var middleName: String?
```

This means:

```text
middleName may contain a String,
or it may contain no value.
```

No value is represented using:

```swift
nil
```

---

## Step 1 – Create an Optional

Try:

```swift
var middleName: String? = "Nimal"

print(middleName as Any)
```

You may see:

```text
Optional("Nimal")
```

Swift is showing that the value is stored inside an optional. Here, `as Any` lets us inspect the optional without a warning about printing it directly; use `if let` or `??` when displaying its value to a user.

---

## Step 2 – Set the Optional to nil

Change it to:

```swift
var middleName: String? = nil

print(middleName as Any)
```

The optional now contains no value.

---

## Why Are Optionals Needed?

Consider:

```swift
let number = Int("25")
```

Swift can convert:

```text
"25"
```

into an integer.

But consider:

```swift
let number = Int("Hello")
```

Swift cannot convert `"Hello"` into a valid integer.

Therefore, `Int()` returns an optional because the conversion might succeed or might fail.

Lecture 02 specifically introduces this example when explaining explicit conversion and optionals.

---

## Force Unwrapping

Suppose:

```swift
var studentName: String? = "Kamal"
```

You can access the value using:

```swift
print(studentName!)
```

Expected:

```text
Kamal
```

The `!` tells Swift:

> I am certain that this optional contains a value.

Consider this unsafe example (keep the final line commented out):

```swift
var studentName: String? = nil

// print(studentName!) // Would crash: the optional contains nil.
```

Uncommenting that line would cause a runtime error.

Therefore, force unwrapping should be used very carefully.

---

## Safe Unwrapping with `if let`

A safer method is **optional binding**.

```swift
var studentName: String? = "Kamal"

if let name = studentName {
    print("Student Name: \(name)")
} else {
    print("Student name is not available")
}
```

Expected:

```text
Student Name: Kamal
```

Now change:

```swift
studentName = nil
```

Make this change **before** the `if let` statement, then run the program again.

Expected:

```text
Student name is not available
```

The program continues safely.

---

## Unwrapping Multiple Optionals

Create:

```swift
var firstName: String? = "Kamal"
var lastName: String? = "Perera"
```

Now:

```swift
if let first = firstName, let last = lastName {
    print("Full Name: \(first) \(last)")
} else {
    print("Complete name is not available")
}
```

Run the program.

Then change:

```swift
lastName = nil
```

Make this change before the `if let` statement, then run it again.

Observe what happens.

---

## Nil-Coalescing Operator

Sometimes you do not need to know whether a value existed.

You simply want to provide a default value.

Swift provides:

```swift
??
```

Example:

```swift
var nickname: String? = nil

let displayName = nickname ?? "No Nickname"

print(displayName)
```

Expected:

```text
No Nickname
```

Now try:

```swift
var nickname: String? = "Kama"

let displayName = nickname ?? "No Nickname"

print(displayName)
```

Expected:

```text
Kama
```

The expression:

```swift
optionalValue ?? defaultValue
```

means:

> Use the optional value if it exists. Otherwise, use the default value.

---

## Activity 5 – Optional Student Details

Create:

```swift
var firstName: String? = "Kamal"
var lastName: String? = "Perera"
var email: String? = nil
```

Your program should:

1. Safely unwrap `firstName` and `lastName`.
2. Display the full name.
3. Display the email address.
4. If no email exists, display:

```text
Email: Not Provided
```

Use `??` for the email address.

---

## Knowledge Check

**Suggested time: 5 minutes.** Record brief answers as comments at the end of `Exercise06.swift`.

Before attempting the final task, make sure you can answer the following questions yourself:

1. What is the difference between `let` and `var`?
2. What does type inference mean?
3. What is the difference between `Int` and `Double`?
4. Why does Swift require explicit type conversion?
5. What does `%` calculate?
6. What is string interpolation?
7. What does `String?` mean?
8. What does `nil` mean?
9. Why can force unwrapping be dangerous?
10. What is the purpose of `if let`?
11. What does `??` do?

If you are unsure about any question, return to the relevant exercise before continuing.

---

## Final Practical Task – Student Result Analyzer

### Suggested Time: 25 Minutes

Create:

```text
FinalChallenge.swift
```

This is the final task that must be submitted.

You are required to combine the concepts learned throughout Practical 01.

---

## Scenario

You have been asked to create a simple Swift program that stores and displays a student's result for a university module.

Your program must store basic student information, calculate the student's final result, and safely handle optional contact information.

---

## Requirements

## Part A – Student Information

Create suitable variables/constants for:

```text
Student Name
Student ID
Module Code
Assignment Mark
Exam Mark
Email Address
```

Use appropriate Swift data types.

Use `let` for values that should not change.

---

## Part B – Calculate the Final Mark

Assume:

```text
Assignment = 40%
Exam       = 60%
```

Calculate:

```text
Final Mark = Assignment Mark × 0.40
           + Exam Mark × 0.60
```

Example:

```swift
let assignmentMark = 75.0
let examMark = 68.0
```

The calculated final mark should be:

```text
70.8
```

---

## Part C – Determine Pass Status

A student passes the module when:

```text
Final Mark >= 50
```

Create a Boolean variable:

```swift
let passed = ...
```

Display:

```text
Passed: true
```

or:

```text
Passed: false
```

---

## Part D – Student Email

Declare the email address as an optional:

```swift
var email: String?
```

Test your program twice.

### Test 1

Assign an email address:

```swift
email = "kamal@example.com"
```

Display the email safely.

### Test 2

Set:

```swift
email = nil
```

Your program must display:

```text
Email: Not Provided
```

Your program must **not crash**. Use `if let` or `??` to handle the email safely, and use string interpolation for the report. Demonstrate both safe techniques across your submitted exercises.

---

## Expected Output

Your output should be similar to:

```text
================================
       STUDENT RESULT
================================

Student Name : Kamal Perera
Student ID   : ITXXXXXXXX
Module       : SE4041

Assignment Mark : 75.0
Exam Mark       : 68.0
Final Mark      : 70.8

Passed : true

Email : kamal@example.com
```

When the email is unavailable:

```text
================================
       STUDENT RESULT
================================

Student Name : Kamal Perera
Student ID   : ITXXXXXXXX
Module       : SE4041

Assignment Mark : 75.0
Exam Mark       : 68.0
Final Mark      : 70.8

Passed : true

Email : Not Provided
```

You may use your own sample student information. Assume marks are between 0 and 100. Small differences in decimal display are acceptable; no special number-formatting API is required.

Also check the pass boundary: using 50.0 for both marks should produce `true`; using 49.0 for both should produce `false`. Save your final sample and take screenshots of both email cases.

---

## Additional Challenge

Complete this section if you finish the main task early.

Create another optional:

```swift
var phoneNumber: String?
```

Use the nil-coalescing operator to display:

```text
Phone: Not Provided
```

when no phone number is available.

Then create:

```swift
let attendance = 82
```

A student is considered fully eligible when:

```text
Final Mark >= 50
AND
Attendance >= 80
```

Store the result in:

```swift
let eligible = ...
```

Display the result using string interpolation.

---

## Submission Requirements

Your GitHub repository must contain the completed practical files:

```text
Exercise01.swift
Exercise02.swift
Exercise03.swift
Exercise04.swift
Exercise05.swift
Exercise06.swift
FinalChallenge.swift
```

You must also create:

```text
screenshots/
```

and include screenshots showing:

```text
01-Practical-Exercises.png
02-Final-Challenge.png
03-Final-Challenge-No-Email.png
```

- `01-Practical-Exercises.png`: readable code and successful output from the guided exercises, including a safe optional example. Add more exercise screenshots if needed.
- `02-Final-Challenge.png`: the complete final report with an email address.
- `03-Final-Challenge-No-Email.png`: the complete final report with `Email : Not Provided`.

Capture the actual output after running your code. On a Mac, use **Shift + Command + 4** to capture an area, then rename and save the image in `screenshots/`. On an iPad, use its screenshot controls and save/upload the image to the same folder.

After uploading the images, you can add this Markdown to your repository README to display your evidence:

```markdown
## My Practical Evidence

![Guided exercise output](screenshots/01-Practical-Exercises.png)
![Final report with email](screenshots/02-Final-Challenge.png)
![Final report without email](screenshots/03-Final-Challenge-No-Email.png)
```

Keep this lab sheet in `README.md` and add your student name, student ID, chosen environment, and evidence section below it. Submit the repository link through the channel specified by your instructor.

---

## GitHub Submission

Before completing the practical, check your repository.

If you are using Git locally, run these commands inside your cloned repository folder:

```bash
git status
git add .
git commit -m "Complete SE4041 Practical 01"
git push
git status
```

Open your GitHub repository after pushing and verify that the latest files and screenshots are available and readable. If you used GitHub's browser editor or upload workflow, verify that every change has been committed there.

---

## Final Submission Checklist

Before leaving the practical session, confirm that:

- [ ] All exercises have been completed.
- [ ] The code runs without compiler errors.
- [ ] Meaningful variable names have been used.
- [ ] `let` and `var` have been used appropriately.
- [ ] Appropriate Swift data types have been used.
- [ ] Type conversion has been demonstrated.
- [ ] Arithmetic and comparison operators have been used correctly.
- [ ] String interpolation has been demonstrated.
- [ ] At least one optional has been used.
- [ ] The optional has been safely handled.
- [ ] The program has been tested with the optional containing `nil`.
- [ ] The Final Practical Task has been completed.
- [ ] Required screenshots have been added.
- [ ] All files have been committed and pushed to GitHub.

---

## Practical 01 – Suggested Time Plan

| Activity | Time |
|---|---:|
| Environment + GitHub Setup | 10 min |
| Exercise 01 – Constants & Variables | 10 min |
| Exercise 02 – Data Types & Type Inference | 10 min |
| Exercise 03 – Conversion & Arithmetic Operators | 15 min |
| Exercise 04 – Comparison & Logical Operators | 10 min |
| Exercise 05 – Strings & Interpolation | 10 min |
| Exercise 06 – Optionals | 20 min |
| Knowledge Check | 5 min |
| Final Practical Task | 25 min |
| Screenshots + Final GitHub Check | 5 min |
| **Total** | **120 min** |

The additional challenge is optional and is intended for students who finish early. Follow the time targets and ask for help when an error prevents you from progressing.

---

## End of Practical 01

By completing this practical, you have covered the fundamental Swift concepts required before moving into collections and control flow.

In **Practical 02**, you will build on this knowledge using:

**Arrays → Sets → Dictionaries → `if` → `switch` → Ranges → Loops**

which follows the progression of Lecture 03.
