# Laboratory Activity 2.1: C# Conditional Statements and Loops

**Teacher:** Engr. EJ S. Ramirez  
**Subject:** NET Technology (C# Fundamentals)
**Week:** 2

## Laboratory Objectives

At the end of this laboratory activity, students should be able to:

1. Create a C# console application that accepts numeric input from the user.
2. Compare values using relational operators and conditional statements.
3. Combine conditions using logical operators.
4. Use a `for` loop to repeat instructions a specified number of times.
5. Use the conditional (ternary) operator to select one of two results.
6. Convert program requirements into pseudocode before writing C# code.
7. Test a program using different inputs and compare the actual output with the expected output.

---

## Directions

1. Create a C# console application for this laboratory activity.
2. Implement each problem in a separate C# file or project, as instructed by your teacher.
3. Read each problem statement and its pseudocode before writing the program.
4. Use `Console.Write()` or `Console.WriteLine()` to display prompts and results.
5. Use `Console.ReadLine()` to accept input and convert the entered text to integers.
6. Use clear variable names and follow proper C# naming conventions.
7. Run each program using all the provided test cases.
8. Compare the actual output with the expected output. Correct any errors before submitting.
9. Submit the source code and a screenshot or copy of the console output, if required by your teacher.

> **Input assumption:** For this activity, the user enters valid whole-number values whenever the program requests an age, mark, or number.

---

## Problem 1: Who's Older?

### Problem Statement

Create a C# console program named `Act4_1Problem1` that determines which of two people is older.

The program must:

1. Ask the user to enter your age.
2. Ask the user to enter your friend's age.
3. Read both ages as whole numbers.
4. Compare the two ages using `if`, `else if`, and `else`.
5. Display `You are older.` when your age is greater than your friend's age.
6. Display `Your friend is older.` when your friend's age is greater than your age.
7. Display `Both have the same age.` when the two ages are equal.

The comparison must be based on the numeric values, not on the order in which the values are entered.

### C# Pseudocode

```text
START
    DISPLAY "Enter your age: "
    INPUT yourAge

    DISPLAY "Enter your friend's age: "
    INPUT friendAge

    IF yourAge is greater than friendAge
        DISPLAY "You are older."
    ELSE IF friendAge is greater than yourAge
        DISPLAY "Your friend is older."
    ELSE
        DISPLAY "Both have the same age."
    END IF
END
```

### Test Cases and Expected Output

| Test Case | Your Age | Friend's Age | Expected Output |
|---|---:|---:|---|
| You are older | `20` | `18` | `You are older.` |
| Friend is older | `17` | `19` | `Your friend is older.` |
| Same age | `21` | `21` | `Both have the same age.` |
| Both are young | `5` | `3` | `You are older.` |

---

## Problem 2: Exam Result Checker

### Problem Statement

Create a C# console program named `Act4_1Problem2` that checks whether a student passed two subjects.

The passing mark for each subject is **40**. The program must:

1. Ask the user to enter the mark for the first subject.
2. Ask the user to enter the mark for the second subject.
3. Read both marks as whole numbers.
4. Use logical operators to check whether both marks are at least `40`.
5. Display `Passed.` only when the first subject mark and the second subject mark are both greater than or equal to `40`.
6. Display `Failed.` when either mark is below `40`.

A mark of exactly `40` is a passing mark. The program must not display `Passed.` if only one subject meets the passing requirement.

### C# Pseudocode

```text
START
    SET passingMark to 40

    DISPLAY "Enter the mark for Subject 1: "
    INPUT subject1Mark

    DISPLAY "Enter the mark for Subject 2: "
    INPUT subject2Mark

    IF subject1Mark is greater than or equal to passingMark
       AND subject2Mark is greater than or equal to passingMark
        DISPLAY "Passed."
    ELSE
        DISPLAY "Failed."
    END IF
END
```

### Test Cases and Expected Output

| Test Case | Subject 1 | Subject 2 | Expected Output |
|---|---:|---:|---|
| Both marks pass | `75` | `80` | `Passed.` |
| First mark is exactly 40 | `40` | `65` | `Passed.` |
| Second mark is below 40 | `70` | `39` | `Failed.` |
| Both marks fail | `25` | `35` | `Failed.` |
| First mark is below 40 | `39` | `40` | `Failed.` |

---

## Problem 3: Countdown Timer

### Problem Statement

Create a C# console program named `Act4_1Problem3` that displays a countdown.

The program must:

1. Begin the countdown at `5`.
2. Use a loop to display each number from `5` down to `0`.
3. Decrease the displayed value by `1` after each repetition.
4. Display each countdown number on a separate line.
5. Display `Countdown Finished!` on a new line after `0` has been displayed.

Use a loop rather than writing six separate output statements. The loop condition must allow `0` to be printed.

### C# Pseudocode

```text
START
    FOR count from 5 DOWN TO 0
        DISPLAY count
    END FOR

    DISPLAY "Countdown Finished!"
END
```

### Test Case and Expected Output

| Test Case | Starting Value | Expected Output |
|---|---:|---|
| Given countdown | `5` | `5`<br>`4`<br>`3`<br>`2`<br>`1`<br>`0`<br>`Countdown Finished!` |

---

## Problem 4: Odd or Even?

### Problem Statement

Create a C# console program named `Act4_1Problem4` that identifies whether a whole number is odd or even.

The program must:

1. Ask the user to enter a whole number.
2. Read the number as an integer.
3. Use the modulus operator (`%`) to determine the remainder after division by `2`.
4. Use the conditional (ternary) operator (`?:`) to choose the result.
5. Display `The number is even.` when the remainder is `0`.
6. Display `The number is odd.` when the remainder is not `0`.

The program should work for positive numbers, zero, and negative whole numbers. Do not replace the ternary operator with an `if` statement for this problem.

### C# Pseudocode

```text
START
    DISPLAY "Enter a whole number: "
    INPUT number

    IF number modulus 2 is equal to 0
        SET result to "The number is even."
    OTHERWISE
        SET result to "The number is odd."
    END IF

    DISPLAY result
END
```

> **Implementation note:** In C#, write the decision represented above with the conditional operator:
> `result = number % 2 == 0 ? "The number is even." : "The number is odd.";`

### Test Cases and Expected Output

| Test Case | Input | Expected Output |
|---|---:|---|
| Positive even number | `8` | `The number is even.` |
| Positive odd number | `7` | `The number is odd.` |
| Zero | `0` | `The number is even.` |
| Negative even number | `-6` | `The number is even.` |
| Negative odd number | `-5` | `The number is odd.` |

---

## Definition of Terms

| Term or Operator | Definition |
|---|---|
| conditional statement | A statement that selects which instructions to execute based on whether a condition is true or false. |
| `if` statement | A C# statement that executes a block of code when its condition is true. |
| `else if` statement | A conditional branch checked when the preceding `if` condition is false. |
| `else` statement | A block executed when all preceding conditions in the same decision structure are false. |
| condition | An expression that produces either `true` or `false`. |
| relational operator | An operator used to compare values, such as `>`, `<`, `>=`, `<=`, `==`, and `!=`. |
| logical operator | An operator used to combine or modify conditions, such as `&&` (AND), `||` (OR), and `!` (NOT). |
| `&&` operator | The logical AND operator. It produces `true` only when both conditions are true. |
| loop | A control structure that repeats a block of instructions while a specified rule is followed. |
| `for` loop | A loop commonly used when the starting value, ending value, and step of a repetition are known. |
| counter | A variable whose value changes during a loop to track the current repetition or value. |
| decrement | The process of reducing a value, usually by one. |
| modulus operator (`%`) | An operator that returns the remainder after one number is divided by another. |
| conditional (ternary) operator (`?:`) | A compact operator that evaluates a condition and returns one of two expressions. |
| integer | A whole number that may be positive, negative, or zero. |
| input | Data supplied to a program, usually by a user through the keyboard. |
| output | Information displayed by a program after processing its input. |
| `Console.ReadLine()` | A C# method that reads a line of text entered by the user. |
| `Console.WriteLine()` | A C# method that displays text or a value and then moves the cursor to the next line. |
| `int.Parse()` | A C# method that converts a string containing a valid whole number into an `int`. |
| pseudocode | A language-independent, readable description of an algorithm. |
| algorithm | A finite, ordered set of steps used to solve a problem. |
