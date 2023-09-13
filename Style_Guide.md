# ERAU VEX Robotics Style Guide

This document outlines the Coding Style Guide for the Embry-Riddle Aeronautical University – Prescott Campus VEX Robotics team.

Any text within angle brackets `<like_so>` should be considered placeholder values for what the text means. For example, `<your_name>` would be a placeholder for a person’s name. An ellipsis (…) is a placeholder for a block of code, whose exact specifics are unimportant to the example.

## Terminology

Terminology for various programming concepts can vary between programming languages. This section defines what we mean when we use a specific term. This guide is only concerned with C/C++, so if a term is not defined here, assume that the C/C++ definition applies.

- Parameter: A variable in a function whose value must be passed in when the function is called
- Argument: A value passed to a function
- Struct: short of structure, a custom data type that is composed of one or more other data types.

## Formatting

This section deals with how code should be formatted, including how to indent code, how things should be named, and how to comment.

All club repositories should include a `.clang-format` file with the following content:

```
BasedOnStyle: LLVM
UseTab: Always
IndentWidth: 4
TabWidth: 4
BreakConstructorInitializers: BeforeColon
```

This enforces use of the LLVM Style guide formatting by default. However, it also sets the formatter to use tabs instead of spaces. This allows individual programmers to set the tab width they desire, instead of enforcing a constant indentation width. The last one is C++ specific.

## Naming

In general, names should be in snake case – all letters are lowercase, and words in names are separated by underscores (e.g. `this_is_snake_case`).

Names should be reasonably descriptive of the purpose of the variable/constant/function, i.e. an array containing the ports for the left side of the drivetrain should be called `drive_left_ports`, or something similar.

### Constants

For any constant value (whether a` #define` or a `const`), all letters should be in uppercase (e.g. `THIS_IS_A_CONSTANT`).

### Types

Custom types, whether structs or classes, should be in `Title_Snake_Case` (like so). For example, a struct for telemetry data should be defined as so:
```
typedef struct {
	…
} Telem_Data;
```
## Comments
Comments that take 1 or 2 lines should use `//` (“C++ style” comments) to indicate comments, like so:

```
// This is a short comment
// Not a lot needs to be said here
```

Longer comments should be formatted using `/**/` (“C-style” comments) like so:

```
/**
 * This is a multiline comment
 * More text
 * Even more text
 */
 ```

## Documentation
This section details how various parts of the code should be commented to ensure that everyone reading the code understands the code.

### Files

Every file should start with a multiline comment in the following format:

```
/**
 * File; <file_name>
 * <explanation of what the file is for>
 * ...
 */
```

### Variables

No matter the type, variable declarations should be preceded by a comment explaining what the variable is.

```
// <A description of what the variable is for>
<type> <variable_name>
```

If a variable's value is initialized separate from the declaration, place this comment with the declaration.

### Functions
Functions should be preceded by a multiline comment in the following format:

```
/**
 * Function: <function_name>
 * A description of the function’s purpose
 * 
 * @param <param_name> A description of a parameter to the function
 *
 * @return A description of what the function returns
 */
<return_type> <function_name>(<param_name>);
```

However, if the purpose of the function is extraordinarily clear and the function itself is relatively simple, you may use a simpler description. To be considered simple, a function must be around or below 15 lines in its implementation, take no arguments, and return `void`. If the function meets these criteria, you may describe the function like so:
```
// Description of the function's purpose
void <function_name>(void);
```

### General Code Documentation

Wherever the exact purpose of a block of code isn't obvious, a comment should be included explaining what the code is supposed to do.
```
<return_type> <function_name>(<param_name>) {
    ...

    /**
     * <An explanation of what the following block of code does>
     */
    <complex algorithm inside a function>
}
```

Whether the comment should use `//` or `/**/` is governed by the general comment guidelines.