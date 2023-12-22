## [[1.1 Introduction to Algorithms]]
#### Abstract Thinking
> Setting a general foundation/outline to solve a solution


#### Algorithm
> A sequence of clearly ordered instructions that helps reach a solution in a finite amount of time

___
## [[8.1 Arrays I]]

### Arrays

- A sequence of items that are contiguously allocated in memory

- All items in the array are of the same data type and of the same size

- All items are accessed by the same name, but a different index

>An `array` is a data structure
- A data structure is a way of storing and organizing data in memory so that it may be accessed and manipulated efficiently

Store related information (i.e., Student ID numbers, Names of players on the Seattle Mariners roster, Scores for each combination in Yahtzee, etc.)

### Dimensions of an Array

- A single dimensional array is logically viewed as a linear structure
- A two dimensional array is logically viewed as a table consisting of rows and columns
- What about three, four, etc., dimensions? Same idea.

### Array Declaration

Arrays are declared in the same way as variables:

```c
int a[6];
```
declares an array `a` with 6 cells that hold integers:

| `a[0]` | `a[1]` | `a[2]` | `a[3]` | `a[4]` | `a[5]` | 
| -------- | -------- | -------- | -------- | -------- | -------- |
| `10` | `12`| `0` | `89` | `1`| `91` |
Notice that array indexing begins at 0.

We can declare arrays alongside simple variables
```c
int students[100], count, teachers[50];
double gpa[100], average;
char ch, name[100]; //name still gets set to a string
```

Assuming the previous array:

| `a[0]` | `a[1]` | `a[2]` | `a[3]` | `a[4]` | `a[5]` | 
| -------- | -------- | -------- | -------- | -------- | -------- |
| `10` | `12`| `0` | `89` | `1`| `91` |

all of the following statements are valid:

```c
a[0] = 4; //changes a[0] from 10 to 4
a[2] += 2; //changes a[2] to value of a[2] + 2 or 0
a[5] = a[3] - a[4]; // sets the value of a[5] to 88
```

We can initialize arrays at the same time we declare them

like we can do 
```c
int count = 0;
```

is valid, so too is

```c
int student_id[] = {3423, 8794, 4595, 1423, 4311};
```

Notice how you can omit the size of the array. The compiled deduces the size from the number of values listed.

### Array Subscripts

We can do arithmetic on array subscripts! Assume this array:

| `a[0]` | `a[1]` | `a[2]` | `a[3]` | `a[4]` | `a[5]` | 
| -------- | -------- | -------- | -------- | -------- | -------- |
| `10` | `12`| `0` | `89` | `1`| `91` |

Then all of the following are valid:

```c
int x = 2;
printf("%d", a[x + 2]); //a[4] == 1
printf("%d", a[2 * x - 1]); //a[3] == 89
printf("%d", a[x] - a[x - 1]); // -12
printf("%d", a[++x]); //a[3] == 89; x == 3
a[x - 1] = a[x - 2]; // assigns 12 to a[2]
printf("%d", a[x + 4]); // Does a[7] exist
```

Write a segmented of code that creates an array of 10 doubles values, populates the array with the values 1.0 through 10.0, and finally exchanges the 1st and 10th values.

```c
double arr_double[10];
for (int i = 0; i < 10; i++) {
	arr_double[i] = (double) i+1;
}
int temp = 0;
temp = arr_double[0];
arr_double[0] = arr_double[9];
arr_double[9] = temp;
```


___

## [[9.1 Strings I]]


A string is a sequence of characters terminated by the null character `'\0'`.

- A string may include letters, digits, and special characters
- A string is accessed via a pointer to the first character in it

>**NOTE:** A string may always be represented by a character array, but a character array is not a string

```c
char my_string[10] = ['m', 'y', '_', 's', 't', 'r', 'i', 'n', 'g' '\0'];
// string and character array

char my_string[9] = ['m', 'y', '_', 's', 't', 'r', 'i', 'n', 'g']; 
//character array only
```

String length in declaration must always account for the null terminator!

```c
char my_string[10] = "my_string"; // correct
char my_string[9] = "my_string"; // incorrect
```

We can specify a *field width* in a `printf` statement involving a string (`%s`). By default the string is right justified within that field, e.g.,

```c
printf("string value: |%11s|\n", my_string);
```

*Right justified* aligns to the right side (field length i.e., `11` is greater than 0).
Since in the code above `11` is bigger than the string length of `10`, it outputs the string and `11-10 = 1` extra spaces to the left of the displayed string.

```c
// result:
//| my_string|
```

For left justification,
```c
printf("string_value: |-11%s|\n", my_string);
```

*Left justified* aligns to the left side (field length i.e., `-11` is less than 0).
Since in the code above, `11` is bigger than the string length of `10`, it outputs `11-10 = 1` extra spaces to the right of the displayed string.

```c
// result:
//|my_string |
```

### Arrays of Strings

```c
char* name[5] = {"string1", "string2", "string3", "string4", "string5"};
```

>**NOTE:** You have to use the indirection operator (\*) for defining arrays of strings. This is because you want the address of the beginning of each of the strings in your array, so you have an array of addresses.


## [[9.2 Strings II]]


Standard operators such as (`==`, `>`, `<`, `>=`, `<=`) *cannot* be applied to strings in C.
#### String Manipulation in C

>The string-handling library `<string.h>` provides many powerful functions which may be used in place of standard operators

- `strcpy(destination, source)` replaces the assignment operator *\=*
- `strcat(destination, source)` replaces the *+* or operator
- `strcmp(destination, source)` replaces relational operator *\==*
- `strtok(destination, soruce)` replaces the next occurrence of a delimiter with the null character `'\0'`
- `memset(row of 2-D array, value you want to set it to, length of the row);` often used to set values to null character
- etc.

`strtok(my_str, ',');` can be used to replace the commas in the string to the null character (Great for `.csv` data manipulation!)

>**NOTE**: If delimiter does not exist in the string, it will go to the null character, stop, and return first address of the string

To access these functions, we have to include the `string.h` library

```c
#include <string.h>
```

Examples of using `<string.h>` functions

`strcpy()`.
```c
char string1[20] = "Charles Liu";
char string2[20];
strcpy(string2, string1);
puts(string2); //displays: Charles Liu
//string2 is now "Charles Liu\0"
```

Similar function `strncpy()`.
```c
char string1[20] = "Charles Liu";
char string2[20];
strncpy(string2, string1, 7);
puts(string2); //displays: Charles
//string2 is now "Charles\0"
```

We have to be careful when using these functions to make sure we don't put too many characters in an array that can't take that many.

```c
char string1[20] = "Charles Liu";
char string2[4] = "Mir";
strncpy(string2, string1, 7); //breaks
//string 2 can only take 4 characters, but strncpy() put in 7!
```

We can use the following method to guard against this situation:
```c
strncpy(destination, source, destination_length - 1);
destination[dest_length - 1] = '\0'
```
### Substrings 

We can start `strncpy()` from the middle of a string to copy parts of it.

```c
char string1[25] = "Charles Liu";
char string2[4];
strncpy(string2, &string1[9]);
puts(string2); //displays Liu
//string2 is now "Liu\0"
```

___

`strtok()`
Suppose I want to extract the first name `"Charles"`, last name `"Liu"`, status `"Cool"`, and grade `"11"` from "`Charles, Liu, Cool, 11`"

```c
char info[25] = "Charles, Liu, Cool, 11";
char info_copy[25];
char *first_name, *last_name, *status, *grade;
strcpy(info_copy, info);
first_name = strtok()
```

If we supply only one parameter in a 2-D array, it gives the starting point of the unknown parameter.

___
## [[10.1 Structures I and Enumerated Types]]


### C Supported Datatypes

C supports a variety of different *integer* formats

| **Type** | **# of bits in Microsoft Visual C** |
| -------- | -------- |
| `Short` | `16`|
| `unsigned short` | `16` | 
| `int` | `32`| 
| `unsigned int` | `32` | 
| `long` | `32` | 
| `unsigned long` | `32` |

> **NOTE:** *unsigned* just means the variable only supports *non-negative* values.

C also supports a variety of different *double* formats

| **Type** | **# of bits in Microsoft Visual C** |
| -------- | -------- |
| `float` | `32`|
| `double` | `64` | 
| `long double` | `64`|

___

>Do **NOT** use floating point values for things like for loop conditions!

This may result in **round-off errors**!

- Don't rely on two floating-point values being equal:
```c
//NO!
for (trial = 0; trial != 10.00; trial += 0.1) {
	//code here
}
//dangerous...
```

- Even the following may not execute the same number of times on all computers:
```c
for (trial = 0; trial < 10.0; trial += 0.1) {
	//code here
}
//BAD!
```

>**Remark:** Its better to use integers as loop counters.

____
### Conversions between `int` and `double`

When we assign an `int` to a `double` or a `double` to an `int`, C performs an automatic conversion:

```c
int k = 5, m = 4, n;
double x = 2.5, y = 4.1, z;
z = k + x; // 7.5: k is converted to double PRIOR to +
z = k \ m // k / m is evaluated first, 5 / 4 = 1 after integer division, 1 is converted to double. Result: 1.0
n = x * y;  // x * y is evaluated first 2.5 * 4.1 = 10.25. Result converted to integer. Result = 10.
```

>**NOTE:** Explicit casting is always an option. They don't change the internal representation of the variable however.

___

### Conversions between `char` and `int`

Converting between `char` and `int` just uses the ASCII table to convert.

___
### Enumerated Types

> Define custom data types (i.e., days of the week, months of the year, household budget categories, business inventory categories, etc.)

We can do this with C *enumerated* types.

```c
typedef enum {
	clothing, household, electronics, garden, health_beauty, sporting_goods
}
```

>**NOTE:** `clothing` assigned to integer value 0, `household` gets integer value 1, ...`sporting_goods` gets integer value 5.

so:
```c
printf("clothing: %d\n", clothing);           // Outputs: 0
printf("household: %d\n", household);         // Outputs: 1
printf("electronics: %d\n", electronics);     // Outputs: 2
printf("garden: %d\n", garden);               // Outputs: 3
printf("health_beauty: %d\n", health_beauty); // Outputs: 4
printf("sporting_goods: %d\n", sporting_goods); // Outputs: 5`
```
```c
type def enum inv_type {
	clothing, household, electronics, garden, health_beauty, sporting_goods
} inv_type;
```

Once we've defined an `enumerated` type, we can declare variables of that type

`inv_type inv_kind;`

and use the type in `switch` statements

```c
void print_inventory(inv_type inv_kind) {
	switch (inv_kind) {
		case clothing:
			printf("clothing");
			break;
		case household:  
			printf("household");  
			break;  
		case electronics:  
			printf("electronics");  
			break;  
		case garden:  
			printf("garden");  
			break;  
		case health_beauty:  
			printf("health and beauty");  
			break;  
		case sporting_goods:  
			printf("sporting goods");  
			break;  
	}
}
```

We can cast `enumerated` types to `int`.
```c
int household_val;
inv_type this_inv;
household_val = (int) household
```

and cast integers to the enumerated type:
```c
this_inventory = (inv_type)(electronics + 1);
```

### Common Enum - Boolean

```c
typedef enum boolean {
	FALSE, TRUE
} Boolean;

typedef enum month {
	JAN = 1, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP OCT, NOV, DEC
} Month;
```

___
### Struct Type

C supports another kind of user-defined type: the `struct`.
`structs` are a way to combine multiple variables into a single package (*"encapsulation"*)

Suppose we want to create a database of students in a course. We could define a student `struct` as follows:

```c
typedef enum {freshman, sophomore, junior, senior} class_type; // class standing

typedef enum {anthropology, biology, chemistry, english, compsci, polisci, psychology, physics, engineering, sociology} major_type; //major

typedef struct {
	int id_number;
	class_t class_standing;
	major_t major;
	double gpa;
	int credits_taken;
} student_type;
```

We can define some students:

```c
student_type student_1, student_2;
student1.id_num = 123456789;
student.class_standing = freshman;
student.major = anthropology;
student1.gpa = 3.5;
student1.credits_taken = 15;
student2.id_num = 321123456;
student2.class_standing = senior;
student2.major = biology;
student2.gpa = 3.2;
student2.credits_taken = 100;
```

We can copy a whole `struct` by using the assignment operator

```c
student_type student3 = student1;
```

___

### Recursion

The *process* in which a function calls itself either directly or indirectly through another function

The function that is called is known as *recursive* function
i.e.,
```c
int recursive_function (int r, int s) {
	//...
	recursive_function(r, s-1) //recursive call
	//...
}
```

### Nature of Recursion

Problems that may be solved using recursion have these attributes
- One or more simple cases have a straightforward, non-recursive solution
- The other cases may be defined in terms of problems that are closer to simple cases
- Through a series of calls to a recursive function, the problem eventually is stated in terms of the simple cases

As described by Wirth:
```c
"The power of recursion evidently lies in the possibility of defining an infinite set of objects by a finite statement. In the same manner, an infinite number of computations can be described by a finite recursive program, even if this program contains no explicit repititions".
```

- A divide and conquer approach
- A fresh copy of a function goes to work on a similar, but simpler problem than the original
- May be used as an alternative to iteration

### Properties of Recursion

- Recursive solution have at least two cases:
	- The simple or *base* case(s)
	- The *recursive* case(s) or step(s)

### Example of Recursive Solution

```c
int multiply (int m, int n) {
	int ans;
	if (n == 1) {
		ans = m;
	}
	else {
		ans = m + multiply (m, n - 1); //recursive step
	}
	return ans;
}
```

___

### Recursive Functions

### Recall

>A recursive function is one that calls itself either directly or indirectly through another function
>Recursion may be replaced by an iterative (loops) solution

### Advantages of Recursion

May provide a simpler solution than an iterative one
- Sometimes iterative solutions lend themselves to complex algorithms
May lead to reduction in *code size*
May lead to reduction in *time complexity*

### Disadvantages of Recursion

May require large amounts of memory
- For each call to the function more memory is allocated for local variables
- Call stack continues to grow for each call; may lead to stack overflow
	- Recall the call stack keeps track of a point to which each active function or subroutine should return control when finished
Difficult to test and debug

### Factorial Example

The factorial of a positive number $\large{n}$ (including zero) is represented as $\large{n!}$ 
$\large{n!}$ is the product of all of the positive integers less than or equal to $\large{n}$ (not including zero)

i.e. $\large{3! = 3 \times 2 \times 1 = 6}$

Below is a recursive solution to $\large{n!}$

```c
int rec_factorial(int n){ 
	int result = 0;
	if (n == 0 || n == 1) { //base case
		result == 1;
	}
	else { //recursive step
		result = n * rec_factorial(n - 1);
	}
	return result;
}
```