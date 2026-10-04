# Studio 12

## Types and Generic Programming

In this studio, you will explore type declaration and usage issues that arise when specifying and using different expressions, variables, and parameters. The exercises look at how `const` applies to integers and pointers, and how `auto`, `decltype`, and type aliases interact with top-level and low-level `const`. These issues are essential to the generic programming paradigm, and addressing them establishes foundations for managing type-related issues in C++ that later topics build on.

## Collaboration

You may complete this studio individually or in a small group.

## Reference

If you need a refresher on the environment setup steps from the previous studios, see [Studio 0](https://github.com/cse4208-wustl/studio0).

## Exercises

Record your answers in `ANSWERS.md` as you work. Include the names of everyone who worked on the studio in your first answer, and number your responses so they are easy to match to the exercises.

1. List the names of the people who worked together on this studio.

2. SSH into `shell.cec.wustl.edu` using your WUSTL Key credentials, then use `qlogin` to connect to one of the Linux Lab machines and confirm that the version of `g++` there is correct, as you did in [Studio 0](https://github.com/cse4208-wustl/studio0).

   Clone your `studio12` repo using SSH:

   ```bash
   git clone git@github.com:cse4208-wustl/studio12.git
   cd studio12
   ```

   The repo already includes a starter `studio12.cpp` and a `Makefile`. Update them as needed so the repo builds an executable named `studio12`.

   In `main`, declare the following variables on separate lines of code:

   1. A `const int` variable initialized with the value `0`
   2. A non-`const` `int` variable initialized with the value `1`
   3. A `const` pointer to a `const int` variable, initialized with the address of the `const int` variable
   4. A `const` pointer to a `const int` variable, initialized with the address of the non-`const` `int` variable
   5. A `const` pointer to a non-`const` `int` variable, initialized with the address of the `const int` variable
   6. A `const` pointer to a non-`const` `int` variable, initialized with the address of the non-`const` `int` variable
   7. A non-`const` pointer to a `const int` variable, initialized with the address of the `const int` variable
   8. A non-`const` pointer to a `const int` variable, initialized with the address of the non-`const` `int` variable
   9. A non-`const` pointer to a non-`const` `int` variable, initialized with the address of the `const int` variable
   10. A non-`const` pointer to a non-`const` `int` variable, initialized with the address of the non-`const` `int` variable

   Then, in separate lines of code, have `main` print to `cout` the values of the `const int` and non-`const` `int` variables, and for each of the pointers the address it contains followed by the value of what it points to.

   Try to build your program, and comment out any lines that will not compile. In your answers, show the lines that had to be commented out, and for each of them explain briefly why it could not be compiled.

3. In `main`, after the output statements that remain, write separate statements (on separate lines of code) that use the prefix `++` operator (which is built in for `int` and pointer types) to modify the value of each of the variables whose declarations were not commented out. For the pointer variables, add a separate statement that modifies what the pointer points to.

   Try to build your program, and again comment out any of the newly added lines that will not compile. In your answers, show the lines that had to be commented out, and for each of them explain briefly why it could not be compiled.

4. In `main`, after the declaration of each of the integer and pointer variables, add another declaration (on a separate line of code) for another variable that is declared using the `auto` type specifier and is initialized with the original variable.

   For each of the variables declared using the `auto` type specifier, use the prefix `++` operator to determine whether or not it can be modified (and in the case of pointer types, also whether or not what it points to can be modified).

   Try to build your program, and again comment out any of the newly added lines that will not compile. In your answers, explain whether or not either low-level `const` or top-level `const` properties were discarded in any of the declarations that used the `auto` type specifier. If they were, show the declaration and explain briefly which of them was discarded and how you know that.

5. In `main`, replace the `auto` type specifier with the `decltype` type specifier in each of the declarations that you added in the previous exercise.

   For each of the variables in those declarations, again use the prefix `++` operator to determine whether or not it can be modified (and in the case of pointer types, also whether or not what it points to can be modified).

   Try to build your program, and again comment out any of the newly added lines that will not compile. In your answers, explain whether (and if so, how) the use of the `decltype` type specifier differed from the use of the `auto` type specifier, in terms of whether or not either low-level `const` or top-level `const` properties were discarded in any of the declarations.

6. Add typedefs for the following types to your program: `int`, `const int`, `const` pointer to `int`, `const` pointer to `const int`, non-`const` pointer to `int`, and non-`const` pointer to `const int`.

   In `main`, replace the type portion of the declaration of each of the integer and pointer variables with the appropriate one of those type aliases.

   Compile and run your program. In your answers, show the declarations that use those type aliases.

## Deliverables

Commit and push all modified and added files, including `ANSWERS.md`, to the repo.
