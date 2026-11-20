# Laboratory Activity 2.2: C# Repetition Statements

**Teacher:** Engr. EJ S. Ramirez  
**Subject:** NET Technology 2 (C# Fundamentals)  
**Week:** 2

## Laboratory Objectives

At the end of this laboratory activity, students should be able to:

1. Explain the purpose of repetition statements in C#.
2. Use a `for` loop when the number of repetitions is known.
3. Use a `foreach` loop to process each item in an array.
4. Use a `while` loop when repetition depends on a condition.
5. Use a `do while` loop to execute a block at least once.
6. Translate a problem statement into pseudocode before coding.
7. Test a C# program and compare its output with the expected result.

## Directions

1. Create a C# console application for this laboratory activity.
2. Use the corresponding source file for each problem: `Problem1.cs` to `Problem7.cs`.
3. Read the problem statement and pseudocode before writing or modifying the program.
4. Use the loop specified in each problem. Do not replace it with repeated output statements or another loop type.
5. Use clear variable names and proper C# indentation.
6. Run every problem using the provided test case.
7. Compare the actual output with the expected result and correct any errors.
8. Submit the seven `.cs` source files and a screenshot or copy of the console output, if required.

## Problem 1: Even Numbers from 1 to 20

### Problem Statement

Write a C# console program that prints all even numbers from `1` through `20`, inclusive. Use a `for` loop. Display one number per line.

### Pseudocode

```text
START
    FOR number from 1 to 20
        IF number modulus 2 is equal to 0
            DISPLAY number
        END IF
    END FOR
END
```

### Test Case and Expected Result

| Test Case | Range | Expected Result |
|---|---|---|
| Given range | `1` to `20` | `2`, `4`, `6`, `8`, `10`, `12`, `14`, `16`, `18`, `20` |

## Problem 2: First Ten Multiples of 3

### Problem Statement

Write a C# console program that prints the first ten multiples of `3`, beginning with `3` and ending with `30`. Use a `for` loop. Display one multiple per line.

### Pseudocode

```text
START
    FOR multiplier from 1 to 10
        SET multiple to 3 multiplied by multiplier
        DISPLAY multiple
    END FOR
END
```

### Test Case and Expected Result

| Test Case | Base Number | Number of Multiples | Expected Result |
|---|---:|---:|---|
| Given values | `3` | `10` | `3`, `6`, `9`, `12`, `15`, `18`, `21`, `24`, `27`, `30` |

## Problem 3: Display Fruits

### Problem Statement

Create an array containing `Apple`, `Banana`, `Cherry`, and `Date`. Use a `foreach` loop to print each fruit on a separate line.

### Pseudocode

```text
START
    SET fruits to ["Apple", "Banana", "Cherry", "Date"]

    FOR EACH fruit in fruits
        DISPLAY fruit
    END FOR EACH
END
```

### Test Case and Expected Result

| Test Case | Array Values | Expected Result |
|---|---|---|
| Given array | `Apple`, `Banana`, `Cherry`, `Date` | `Apple`, `Banana`, `Cherry`, `Date`, one per line |

## Problem 4: Display Cities

### Problem Statement

Create an array containing `New York`, `London`, `Tokyo`, and `Sydney`. Use a `foreach` loop to print each city on a separate line.

### Pseudocode

```text
START
    SET cities to ["New York", "London", "Tokyo", "Sydney"]

    FOR EACH city in cities
        DISPLAY city
    END FOR EACH
END
```

### Test Case and Expected Result

| Test Case | Array Values | Expected Result |
|---|---|---|
| Given array | `New York`, `London`, `Tokyo`, `Sydney` | `New York`, `London`, `Tokyo`, `Sydney`, one per line |

## Problem 5: Countdown Using a While Loop

### Problem Statement

Write a C# console program that prints the numbers from `5` down to `1`. Use a `while` loop and display one number per line.

### Pseudocode

```text
START
    SET number to 5

    WHILE number is greater than or equal to 1
        DISPLAY number
        DECREASE number by 1
    END WHILE
END
```

### Test Case and Expected Result

| Test Case | Starting Value | Expected Result |
|---|---:|---|
| Given value | `5` | `5`, `4`, `3`, `2`, `1`, one per line |

## Problem 6: Count Up Using a While Loop

### Problem Statement

Write a C# console program that prints the numbers from `1` through `5`. Use a `while` loop and display one number per line.

### Pseudocode

```text
START
    SET number to 1

    WHILE number is less than or equal to 5
        DISPLAY number
        INCREASE number by 1
    END WHILE
END
```

### Test Case and Expected Result

| Test Case | Starting Value | Expected Result |
|---|---:|---|
| Given value | `1` | `1`, `2`, `3`, `4`, `5`, one per line |

## Problem 7: Repeat a Message

### Problem Statement

Write a C# console program that displays `Coding is fun!` exactly three times. Use a `do while` loop. Display each message on a separate line.

### Pseudocode

```text
START
    SET count to 1

    DO
        DISPLAY "Coding is fun!"
        INCREASE count by 1
    WHILE count is less than or equal to 3
END
```

### Test Case and Expected Result

| Test Case | Number of Repetitions | Expected Result |
|---|---:|---|
| Given value | `3` | `Coding is fun!` displayed exactly three times |

## Definition of Terms

| Term | Definition |
|---|---|
| repetition statement | A control structure that executes a block of code more than once. |
| loop | A statement that repeats instructions while a condition or collection rule is satisfied. |
| `for` loop | A loop commonly used when the starting value, ending value, and update step are known. |
| `foreach` loop | A loop that visits each element in an array or other collection. |
| `while` loop | A loop that checks its condition before each repetition; it may execute zero times. |
| `do while` loop | A loop that executes its block first and checks its condition afterward; it executes at least once. |
| iteration | One execution of the body of a loop. |
| counter | A variable used to track the number or position of repetitions. |
| increment | Increasing a value, usually by one. |
| decrement | Decreasing a value, usually by one. |
| condition | An expression that evaluates to `true` or `false`. |
| array | A collection of values of the same type stored under one variable name. |
| element | One individual value stored in an array or collection. |
| modulus operator (`%`) | An operator that returns the remainder after division. |
| pseudocode | A readable, language-independent description of an algorithm. |
| output | Information displayed by a program. |
| infinite loop | A loop that does not reach a condition that becomes false. |
