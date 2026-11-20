# Laboratory Activity 3.1: C# Multidimensional and Jagged Arrays

**Teacher:** Engr. EJ S. Ramirez  
**Subject:** NET Technology 2 (C# Fundamentals)  
**Week:** 3

## Laboratory Objectives

At the end of this laboratory activity, students should be able to:

1. Declare and initialize single-dimensional, two-dimensional, three-dimensional, and jagged arrays in C#.
2. Use the `Length` property to determine the number of elements in an array.
3. Use `for` loops to access and display values in a single-dimensional array.
4. Use nested `for` loops to process two-dimensional and three-dimensional arrays.
5. Use nested loops to process the rows of a jagged array.
6. Interpret array indexes and dimensions correctly.
7. Translate a problem statement into pseudocode before coding.
8. Test a C# program and compare its output with the expected result.

## Directions

1. Create a C# console application for this laboratory activity.
2. Use the corresponding source file for each problem: `Problem1.cs` through `Problem4.cs`.
3. Read the problem statement and pseudocode before writing or modifying the program.
4. Use the array type and loop structure specified in each problem.
5. Use clear variable names, correct indexes, and proper C# indentation.
6. Run every problem using the provided test case.
7. Compare the actual output with the expected output and correct any errors.
8. Submit the four `.cs` source files and a screenshot or copy of the console output, if required.

## Problem 1: Student Grades and Average

### Problem Statement

Create a C# program that stores the grades of five students in a single-dimensional integer array named `grades`. Display each grade with its corresponding zero-based index using a `for` loop and the array's `Length` property. Then, use a second `for` loop to calculate the total of all grades, calculate the average as a decimal value, and display the average formatted to two decimal places.

### Hint

Use an integer array, the `Length` property, two `for` loops, an integer `total`, a `double` `average`, and `Console.WriteLine()`. Cast `total` to `double` before dividing by `grades.Length` to avoid integer division.

### Pseudocode

```text
START
    SET grades to [90, 85, 92, 88, 95]

    DISPLAY "Student Grades:"

    FOR index from 0 through the last position in grades
        DISPLAY "Grade at index " followed by index and grades[index]
    END FOR

    SET total to 0
    FOR index from 0 through the last position in grades
        ADD grades[index] to total
    END FOR

    SET average to total converted to a decimal value divided by grades.Length
    DISPLAY "Average grade: " followed by average formatted as F2
END
```

### Test Case and Expected Output

| Test Case | Array Values | Expected Output |
|---|---|---|
| Given grades | `90, 85, 92, 88, 95` | Grades displayed by index and an average of `90.00` |

```text
Student Grades:
Grade at index 0: 90
Grade at index 1: 85
Grade at index 2: 92
Grade at index 3: 88
Grade at index 4: 95
Average grade: 90.00
```

## Problem 2: Monthly Sales Report

### Problem Statement

Create a C# program that stores the monthly sales of three employees for two months in a two-dimensional integer array named `sales`. Use nested `for` loops to display each employee's monthly sales in a tabular format.

### Hint

Use a two-dimensional integer array, `GetLength(0)` for the rows, `GetLength(1)` for the columns, nested `for` loops, `Console.Write()`, and `Console.WriteLine()`.

### Pseudocode

```text
START
    SET sales to the following rows and columns:
        [1500, 2000]
        [1800, 2200]
        [1200, 1700]

    DISPLAY "Monthly Sales Report:"

    FOR employee from the first row to the last row
        DISPLAY "Employee " followed by employee number and ": "

        FOR month from the first column to the last column
            DISPLAY sales[employee, month] on the same line
            IF month is not the last column
                DISPLAY a space on the same line
            END IF
        END FOR

        MOVE to the next line
    END FOR
END
```

### Test Case and Expected Output

| Test Case | Sales Data | Expected Output |
|---|---|---|
| Given sales | Employees 1–3, two months | `1500 2000`, `1800 2200`, and `1200 1700` |

```text
Monthly Sales Report:
Employee 1: 1500 2000
Employee 2: 1800 2200
Employee 3: 1200 1700
```

## Problem 3: Classroom Examination Scores

### Problem Statement

Create a C# program that stores the examination scores of students from two sections. Each section has two students, and each student has two examination scores. Use a three-dimensional integer array named `scores` and three nested `for` loops to display each section, student, examination, and score.

### Hint

Use a three-dimensional integer array, `GetLength(0)`, `GetLength(1)`, and `GetLength(2)` for the three dimensions, three nested `for` loops, and `Console.WriteLine()`.

### Pseudocode

```text
START
    SET scores by section, student, and examination:
        Section 1: [ [85, 90], [88, 92] ]
        Section 2: [ [80, 86], [89, 94] ]

    DISPLAY "Examination Scores:"

    FOR section from the first section to the last section
        DISPLAY "Section " followed by section number and ":"

        FOR student from the first student to the last student
            FOR examination from the first examination to the last examination
                DISPLAY the student number, examination number,
                    and scores[section, student, examination]
            END FOR
        END FOR
    END FOR
END
```

### Test Case and Expected Output

| Test Case | Array Dimensions | Expected Output |
|---|---|---|
| Given scores | 2 sections × 2 students × 2 examinations | Scores from `85` through `94` displayed with their labels |

```text
Examination Scores:
Section 1:
Student 1, Exam 1: 85
Student 1, Exam 2: 90
Student 2, Exam 1: 88
Student 2, Exam 2: 92
Section 2:
Student 1, Exam 1: 80
Student 1, Exam 2: 86
Student 2, Exam 1: 89
Student 2, Exam 2: 94
```

## Problem 4: Movie Theater Showtimes

### Problem Statement

Create a C# program that stores the showtimes for three movie theaters in a jagged integer array named `showtimes`. Theater 1 has two showtimes, Theater 2 has four showtimes, and Theater 3 has three showtimes. Use nested `for` loops to display every theater and its showtimes on one line. The times are represented using the 24-hour format.

### Hint

Use a jagged integer array, the `Length` property for the theaters and each theater's showtimes, nested `for` loops, `Console.Write()`, and `Console.WriteLine()`.

### Pseudocode

```text
START
    SET showtimes as separate lists:
        [10, 13]
        [11, 14, 17, 20]
        [9, 12, 15]

    DISPLAY "Movie Theater Showtimes:"

    FOR theater from the first theater to the last theater
        DISPLAY "Theater " followed by theater number and " showtimes:"

        FOR showtime from the first showtime to the last showtime
            DISPLAY a space and showtimes[theater][showtime]
                on the same line
        END FOR

        MOVE to the next line
    END FOR
END
```

### Test Case and Expected Output

| Test Case | Showtimes | Expected Output |
|---|---|---|
| Given showtimes | Theater 1: `10, 13`; Theater 2: `11, 14, 17, 20`; Theater 3: `9, 12, 15` | Each theater's showtimes displayed on one line |

```text
Movie Theater Showtimes:
Theater 1 showtimes: 10 13
Theater 2 showtimes: 11 14 17 20
Theater 3 showtimes: 9 12 15
```

## Definition of Terms

| Term | Definition |
|---|---|
| array | A collection of values of the same type stored under one variable name. |
| element | One individual value stored in an array. |
| index | The zero-based position of an element in an array. |
| single-dimensional array | An array that stores values in one sequence or row. |
| two-dimensional array | An array organized into rows and columns. |
| three-dimensional array | An array organized across three indexes or dimensions. |
| jagged array | An array whose elements are arrays that can have different lengths. |
| dimension | One level of organization in an array. |
| row | A horizontal group of values in a multidimensional array. |
| column | A vertical group of values in a multidimensional array. |
| nested loop | A loop placed inside another loop. |
| `for` loop | A loop commonly used when the starting value, ending value, and update step are known. |
| `Length` property | A property that returns the number of elements in an array or array dimension. |
| 24-hour format | A time representation in which hours range from `0` to `23`. |
| pseudocode | A readable, language-independent description of an algorithm. |
| output | Information displayed by a program. |
