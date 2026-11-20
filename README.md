# C# Fundamentals for Beginners

This repository contains beginner-friendly learning materials and laboratory activities for learning the fundamentals of C# and .NET console programming.

## Learning goals

By the end of the course, you should be able to:

- Create and run a basic C# console application.
- Use variables, data types, operators, and expressions.
- Write conditional statements and repetition statements.
- Define and use classes, methods, and objects.
- Work with single-dimensional, multidimensional, and jagged arrays.
- Handle common runtime errors with exceptions.
- Create, write, and append text files.
- Translate problem requirements into pseudocode and test cases.

## Course outline

### Week 1: C# fundamentals

| Lesson | Topics |
|---|---|
| [1. Introduction to C#](./WEEK%201/1.%20Introduction%20to%20C%23.pdf) | C# and .NET, basic program structure, console applications, and program execution |
| [2. Data Types and Variables in C#](./WEEK%201/2.%20Data%20Types%20and%20Variables%20in%20C%23.pdf) | Variables, constants, primitive data types, declarations, assignments, and input/output |
| [3. C# Operators](./WEEK%201/3.%20C%23%20Operators.pdf) | Arithmetic, relational, logical, assignment, increment/decrement, and conditional operators |

### Week 2: Statements, control flow, and objects

| Lesson | Topics |
|---|---|
| [4. C# Statements](./WEEK%202/4.%20C%23%20Statements.pdf) | Expressions, declarations, blocks, input/output statements, and basic program flow |
| [5. C# Control Statements](./WEEK%202/5.%20C%23%20Control%20Statements.pdf) | `if`, `else`, `switch`, `for`, `foreach`, `while`, and `do while` |
| [6. Class, Methods, and Objects in C#](./WEEK%202/6.%20Class,%20Methods,%20and%20Objects%20in%20C%23.pdf) | Classes, methods, fields, properties, constructors, objects, and encapsulation |

Laboratory activities:

- [Laboratory 2.1](./WEEK%202/Laboratory2.1.md)
- [Laboratory 2.2](./WEEK%202/Laboratory2.2.md)

### Week 3: Arrays, exceptions, and files

| Lesson | Topics |
|---|---|
| [7. Arrays in C#](./WEEK%203/7.%20Arrays%20in%20C%23.pdf) | Array declaration and initialization, indexes, loops, multidimensional arrays, and jagged arrays |
| [8. Exception Handling in C#](./WEEK%203/8.%20Exception%20Handling%20in%20C%23.pdf) | `try`, `catch`, `finally`, common exception types, and nested exception handling |
| [9. File Handling in C#](./WEEK%203/9.%20File%20Handling%20in%20C%23.pdf) | Creating, writing, reading, appending, and safely managing text files |

Laboratory activities:

- [Laboratory 3.1](./WEEK%203/Laboratory3.1.md)
- [Laboratory 3.2](./WEEK%203/Laboratory3.2.md)

## Recommended setup

- [.NET SDK](https://dotnet.microsoft.com/download)
- [Visual Studio Code](https://code.visualstudio.com/) or Visual Studio
- The **Code Runner** and **C# Dev Kit** extensions for Visual Studio Code

If you are using VS Code with Code Runner:

1. Open **Settings** and find **Code-runner: Executor Map**.
2. Add or update the C# executor with this value:

   ```json
   "csharp": "cd $dir && dotnet run $fileName"
   ```

3. Enable **Code-runner: Run In Terminal**.

Verify that .NET is installed:

```bash
dotnet --version
```

## Suggested learning sequence

1. Read each lesson in order.
2. Reproduce the examples in a small console project.
3. Write pseudocode before attempting each laboratory problem.
4. Run the program with normal, boundary, and invalid inputs where appropriate.
5. Compare the actual output with the expected output and revise the code.

## Repository structure

```text
.
├── WEEK 1/
│   ├── 1. Introduction to C#.pdf
│   ├── 2. Data Types and Variables in C#.pdf
│   └── 3. C# Operators.pdf
├── WEEK 2/
│   ├── 4. C# Statements.pdf
│   ├── 5. C# Control Statements.pdf
│   ├── 6. Class, Methods, and Objects in C#.pdf
│   ├── Laboratory2.1.md
│   └── Laboratory2.2.md
└── WEEK 3/
    ├── 7. Arrays in C#.pdf
    ├── 8. Exception Handling in C#.pdf
    ├── 9. File Handling in C#.pdf
    ├── Laboratory3.1.md
    └── Laboratory3.2.md
```

## Reference

- [Complete C# Tutorial](https://www.completecsharptutorial.com/)