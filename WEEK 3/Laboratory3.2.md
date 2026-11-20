# Laboratory Activity 5.2: C# Exception and File Handling

**Teacher:** Engr. EJ S. Ramirez  
**Subject:** NET Technology 2  
**Week:** 7

## Laboratory Objectives

At the end of this laboratory activity, students should be able to:

1. Use `try`, `catch`, and `finally` blocks in a C# console application.
2. Handle different exception types using nested `try-catch` statements.
3. Create and write text files using `File.WriteAllText()`.
4. Append text to an existing file using `File.AppendAllText()`.
5. Handle file-related exceptions without allowing the program to terminate unexpectedly.
6. Translate a problem statement into pseudocode before writing C# code.
7. Test a program and compare its actual output with the expected output.

## Directions

1. Create a C# console application for this laboratory activity.
2. Create and run the four source files: `Laboratory5.2Problem1.cs` through `Laboratory5.2Problem4.cs`.
3. Read the corresponding problem statement and pseudocode before coding.
4. Use the exception-handling structure specified in each problem.
5. For Problems 3 and 4, run the program in a folder where it has permission to create and modify files.
6. Compare the actual console output and generated file contents with the expected results.
7. Correct errors, then submit the four `.cs` files and the completed laboratory guide, if required.

## Problem 1: Try-Catch-Finally

### Problem Statement

Create a C# program that converts the text `"25"` to an integer. Place the conversion inside a `try` block, display the converted number, and catch a `FormatException` if the text is not a valid integer. Use a `finally` block to display a message indicating that the conversion attempt is complete.

### Pseudocode

```text
START
    SET inputText to "25"
    TRY
        SET number to Convert.ToInt32(inputText)
        DISPLAY "Converted number: " followed by number
    CATCH FormatException
        DISPLAY "Error: The input is not a valid integer."
    FINALLY
        DISPLAY "Conversion attempt complete."
    END TRY-CATCH-FINALLY
END
```

### Test Case and Expected Output

| Test Case | Input | Expected Output |
|---|---|---|
| Valid integer | `"25"` | The converted number and completion message are displayed. |

```text
Converted number: 25
Conversion attempt complete.
```

## Problem 2: Nested Catch

### Problem Statement

Create a C# program with an outer `try-catch` block and an inner `try-catch` block. In the inner block, convert `"10"` to an integer and divide it by zero. Catch the `DivideByZeroException` inside the inner block and display an error message. Use the outer `catch` block to handle any unexpected exception, and display a completion message after the nested blocks finish.

### Pseudocode

```text
START
    TRY
        TRY
            SET numerator to Convert.ToInt32("10")
            SET denominator to 0
            SET result to numerator divided by denominator
            DISPLAY "Result: " followed by result
        CATCH DivideByZeroException
            DISPLAY "Inner error: Cannot divide by zero."
        END INNER TRY-CATCH
    CATCH Exception
        DISPLAY "Outer error: An unexpected error occurred."
    END OUTER TRY-CATCH

    DISPLAY "Nested exception handling complete."
END
```

### Test Case and Expected Output

| Test Case | Numerator | Denominator | Expected Output |
|---|---:|---:|---|
| Division by zero | `10` | `0` | The inner catch handles the exception. |

```text
Inner error: Cannot divide by zero.
Nested exception handling complete.
```

## Problem 3: Write File with Exception Handling

### Problem Statement

Create a C# program that writes the text `"This is the first line in the file."` to a file named `laboratory5.2.txt` using `File.WriteAllText()`. Place the file operation in a `try` block and catch an `IOException` if the file cannot be written. Display a success message when the operation is completed.

### Pseudocode

```text
START
    SET fileName to "laboratory5.2.txt"
    SET content to "This is the first line in the file."

    TRY
        CALL File.WriteAllText(fileName, content)
        DISPLAY "File written successfully."
    CATCH IOException
        DISPLAY "Error: The file could not be written."
    END TRY-CATCH
END
```

### Test Case and Expected Output

| Test Case | File | Content | Expected Output |
|---|---|---|---|
| Write a new file | `laboratory5.2.txt` | `This is the first line in the file.` | A success message and the specified file content. |

```text
File written successfully.
```

**Expected file content:**

```text
This is the first line in the file.
```

## Problem 4: Append File with Exception Handling

### Problem Statement

Create a C# program that appends the text `"This line was appended."` to `laboratory5.2.txt` using `File.AppendAllText()`. Place the file operation in a `try` block and catch an `IOException` if the file cannot be modified. Display a success message when the operation is completed. Run Problem 3 before Problem 4 so that the original line already exists.

### Pseudocode

```text
START
    SET fileName to "laboratory5.2.txt"
    SET content to a new line followed by "This line was appended."

    TRY
        CALL File.AppendAllText(fileName, content)
        DISPLAY "Text appended successfully."
    CATCH IOException
        DISPLAY "Error: The file could not be updated."
    END TRY-CATCH
END
```

### Test Case and Expected Output

| Test Case | Existing File Content | Text to Append | Expected Output |
|---|---|---|---|
| Append to the file created in Problem 3 | `This is the first line in the file.` | `This line was appended.` | A success message and both lines in the file. |

```text
Text appended successfully.
```

**Expected file content after Problems 3 and 4:**

```text
This is the first line in the file.
This line was appended.
```

## Definition of Terms

| Term | Definition |
|---|---|
| exception | An error or unexpected event that occurs while a program is running. |
| exception handling | The process of responding to runtime errors so a program can continue or end safely. |
| `try` block | A block that contains code that may cause an exception. |
| `catch` block | A block that runs when a matching exception occurs in a `try` block. |
| `finally` block | A block that runs after `try` and `catch`, whether an exception occurs or not. |
| nested `try-catch` | A `try-catch` statement placed inside another `try` or `catch` structure. |
| `Exception` | The base class for many runtime errors in .NET. |
| `FormatException` | An exception that occurs when a value has an invalid format for the requested conversion. |
| `DivideByZeroException` | An exception that occurs when an integer is divided by zero. |
| `IOException` | An exception related to input and output operations, including file access. |
| file | A named collection of data stored on a computer. |
| `File.WriteAllText()` | A method that creates or overwrites a file with specified text. |
| `File.AppendAllText()` | A method that adds specified text to the end of a file, creating it if needed. |
| `try-catch-finally` | A complete exception-handling structure containing protected code, error handling, and cleanup or final actions. |
| pseudocode | A readable, language-independent description of an algorithm. |
| output | Information displayed by a program. |