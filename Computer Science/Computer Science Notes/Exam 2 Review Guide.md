#### Chapter 5: Iteration, Iteration, Iteration...  

- **Define what is repetition in programs**
	- Allows for a group of operations to be performed multiple times

- **Apply and implement the 3 looping constructs supported in C**
	- for ( ), while ( ), do-while ( ) 
	- Recall these loop constructs may be transformed into one another  

- **Identify, apply, and implement the 5 major loop patterns **
	- Counting or counter-controlled loop, used with `for ( )` and `while ( )`  
		- Indicates number of loop repetitions required are known before loop execution, i.e. `while (count < 10)`
	- Sentinel-controlled loop, used with for ( ) and while ( )  
		- Indicates loop until a special value is encountered, i.e. while  (`array[i] != ‘\0’`)  
	- Endfile-controlled loop, best suited to be used with for ( ) and while ( )  
		-Indicates loop until the end of a file is reached, i.e. `while (status  != EOF)` or `while (!feof (infile))`  
	- Input validation loop, used with `do-while ( )` 
		- Indicates loop until a value within valid range is entered by user, i.e. `do {//something} while (input != valid)`
	- General conditional loop, used with for ( ) and while ( )  
		- Indicates processing of data until a condition is met 

- **Define what is one iteration**
	- Discuss how loops are defined based on iterations

- **Apply and implement nested loops**
	- Walking through a 2-dimensional array requires the use of nested loops  

- **What is an infinite loop?**
	- A loop which will execute “forever”  

- **Describe and apply compound assignment operators** 
	- These include: `+=, -=, *=, /=, %=`
	- These operators set the variable modified to the modifier performed on itself 
	- i.e
```c
int num = 5;
num %= 2; //num is set to 5 mod 2
printf("%d", num); //returns 1
```

- **Describe and apply the increment and decrement operators**  
	- Post-increment (`i++`), pre-increment (`++i`), post-decrement (`i--`), and pre-decrement (`--i`). 

- **Provide an example of an off-by-one loop error**
```c
char *name = "CharlesL"; //The characters in the first name are indexed from 0 to 6, not 1 to 7.

//get first name
for (int i = 1; i <= 7; i++) {
	printf("%c", name[i]);
}
//This will return harlesL, not Charles
```

___

#### Chapter 6: Modular Programming and Pointers  

- **Define what is a pointer**
	- A variable that contains the address of another variable  
	- Used as output parameters which send back results from functions  
- **Distinguish between output and input parameters**  
	- input is what you give the algorithm, output is what the algorithm gives you after you give it an input
	- i.e. `int out = func(in)`, `in` is the input parameter, `out` is the output parameter
- **Declare and apply pointers**  
- **Distinguish between the multiple usages of the * operator with pointers**  
	- `int *ptr` – indicates the declaration of a pointer  
	- `*result = i + j` – indicates the dereferencing of a pointer (the operator is called the dereference or indirection operator)  
- **Define what is a direct value**
- **Define what is an indirect value**  
	- Accessed via the dereference operator – meaning “follow the pointer”  
**Apply logical memory diagrams of pointers and how they relate to their indirect  
values**  

____

#### Chapter 7: Simple Data Types, Enumerated Types, and Arrays  

- **Identify the integer types in C**  
	- short, unsigned short, int, unsigned, long, unsigned long  
		- signed indicates negative and positive numbers are supported, this is the default type  
		- short consumes 16 bits, long int consumes 32 bits

- **Identify the floating-point types in C** 
	- float, double, long double  

- **Discuss problems with applying floating-point numbers to loop conditions**  


- **Declare and apply enumerated types in C**  
	-  One example includes a Boolean type, where FALSE and TRUE may be assigned a variable of this type  

- **Describe what is an array**  
	- A collection of contiguous or adjacent memory cells associated with one variable name and one type  
	- An array is considered a data structure  
	- A data structure is a way of storing and organizing information; a composite of related data items  

- **Define what is a subscript and index**  
	- Recall array indexing in C starts at 0. Why?  

- **Declare and apply single and 2-dimensional arrays**  
	- Use an initializer list to initialize each item in an array  
	- Use loops to traverse through arrays  

- **Write functions which accept arrays (single and 2-dimensional) as parameters**  
```c
void accept_arr(int arr_1[], int arr_2[][10]) {
	//function algorithm here
}
```

- **What happens when an array is passed to a function?**  
	- The address of the 0th element, only, is copied and passed into the  function  

- **How are arrays and pointers related?**  
	- Is array notation and pointer notation interchangeable?  
		- Pointer notation may always be used with arrays; array notation may replace pointer notation only if the pointer points to the start of an array  
**Declare and apply parallel arrays**  
o Parallel arrays may be replaced by an array of structs  

___

#### Chapter 8: Strings  

**Define what is a string in C**  
o A character array which contains alphabetic, numeric, and special  
characters, and is terminated by the null character (‘\0’)  
**Declare and apply strings**  
**Declare and apply an array of strings**  
o An array of strings is simply a 2-dimensional array of characters where  
each row represents a string and the max length of each string is  
determined by the max number of columns

**Apply string library functions <string.h>**  
o strlen ( ) – returns the length of a string, not including the null character  
o strcpy ( ) – makes a fresh character-by-character copy of a string  
o strcat ( ) – appends one string to the end of another string  
o strcmp ( ) – performs a character-by-character comparison based on ASCII values  
▪ returns 0 if the strings are equal (case does matter), < 0 if string1 is less than string2, or > 0 if string1 > string2  
**Write functions which mimic the four listed string library functions above, without calling the string library functions**  
o Apply array and/or pointer notation to these functions  
**Declare and apply arrays of pointers, i.e. `char *array_ptrs[10]`** 
**Distinguish between scanf ( ) and gets ( ) related to strings**  
**Apply the character operations found in `<ctype.h> `** 
o These include: `isalpha ( )`, `isdigit ( )`, `islower ( )`, `isupper ( )`, `toupper ( )`,  
`tolower ( )`, `ispunct ( )`, `isspace ( )`, `isalnum ( )`  

___

#### Chapter 10: Structs  

**Define what is a structure in C**  
o A collection of related fields or variables under one name  
o May be used to describe real world objects  
**Define what is encapsulation**  
**Declare and apply structs**  
o Declare, initialize, and print out struct information  
- **Declare and apply arrays of structs**  
- **What is the . operator and what is the -> operator?**  
- **Can the assignment (=) operator be applied to structs?**  
	- Yes, the assignment operator copies one struct to another  

___
#### Other Topics  

**Apply pointer arithmetic**  
o For example, ptr++, ptr + index, --ptr, etc.