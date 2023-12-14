####  Chapter 2: Overview of C

- **What is an algorithm?**
	- We should specify algorithms with pseudocode before we implement them in C

- **Define what is a variable**
	- Memory is allocated when a variable is declared
- **Define what is a datatype**
- **List three types supported by C**
	- integer (`int`)
	- Double precision floating-point (`double`)
	- Character (`char`)
- **Define the role of preprocessor directives**
- **Define and apply escape sequences (the newline (\n) is an example of an escape sequence)**
	- Other escape sequences include horizontal tab (`\t`), backslash (`\\`), and double quote (`\”`)
- **Describe the role of main ( ) in every C program**
**Explain the purpose of the { and } curly braces used with main ( ) (and any function for that matter)**
	- Every function body must begin with a { and end with a }
- **List an example of a literal string**
	- `“CptS 121 is amazing!”`
	- Literal strings are used in `printf ( )`
- **Explain the role of return 0 in main ( )**
	- Indicates the program terminated successfully
- **Describe what is a syntax error; which software tool reports these errors?**
- **Explain what is a logic error**
- **Describe the rules for naming an identifier; consider C constraints and naming conventions used in the class C is case sensitive**
- **Define and apply Boolean expressions**
- **Apply operators to C types**
	- Arithmetic operators include: `+`, `-`, `*`, `/`, and `%`
- **Construct and evaluate valid numerical expressions, including mixed-type expressions**
- **Apply operator precedence**
	- `*`,` /`, `%` have the same precedence
	- `+`, `-` have the same precedence, but lower than `*`, `/`, `%`
- **Distinguish between = and == **
- **Compare implicit type casting to explicit type casting**
- **Apply printf ( ) and scanf ( )**
- **Describe what is a prompt**
- **Describe and apply elements of “good” C style and “best” programming practices**
- **Provide logical memory diagrams that represent variables**
- **What is the general algorithm applied to problems in this course?**
	- Get inputs
	- Perform computations
	- Output results
___

#### Chapter 3: Top-Down Design with Functions
Apply top-down design principles
o Divide and conquer
o Structure charts
Apply bottom-up design principles
o We apply bottom-up implementation frequently in the course; we
implement solutions to the sub-problems before we implement main ( )
Define what is a function in C
o General rule-of-thumb is 1 function = 1 algorithm = 1 task
What is cohesion and coupling?
Construct functions that solve sub-problems
Define formal parameter, actual argument, local variable, function header
Describe what is a function prototype
o Declaration to compiler of newly defined function; name, order of
arguments and corresponding types, and return type are very important
Cite advantages of defining functions in C
What are the 3 parts to a function header?
What is a function call? How do actual arguments relate to function calls?
Define what is scope
How do functions communicate with main ( ) and vice versa?
What is a calling function? What is a called function?
Apply C math library functions
o Some of these include: sqrt ( ), pow ( ), floor ( ), ceil ( ), sin ( ), cos ( ),
etc.
Define and apply test drivers
Arguments in C are passed-by-value (copies)
What is functional decomposition and abstraction?
___

#### Chapter 4: Selection Structures
What is a conditional statement?
Describe what is short circuit evaluation?
o Applies to conditional statements with compound logic
Construct flowcharts for a particular problem
List and apply relational operators
o These include: <, >, <=, >=, ==, !=
List and apply logical operators
o These include: !, &&, ||
Construct if-else statements in C
Construct nested if statements
How is false defined in C? How about true?
Apply Boolean operator precedence
File Processing
What is a file stream?
Apply fopen ( ), fclose ( ), fscanf ( ), and fprintf ( )
o You should be able to open files for read and write modes
Which standard streams are created when a C program executes?
Other Topics
What is the three file format?
What is a model? How do they apply to software development?