#### Chapter 5: Iteration, Iteration, Iteration...  

>[!book] **Define what is repetition in programs**
> - Allows for a group of operations to be performed multiple times

>[!book] **Apply and implement the 3 looping constructs supported in C**
> - `for( )`, `while( )`, `do-while ( )` 
> - Recall these loop constructs may be transformed into one another  

- **Identify, apply, and implement the 5 major loop patterns **
	- Counting or counter-controlled loop, used with `for( )` and `while( )`  
		- Indicates number of loop repetitions required are known before loop execution, i.e. `while(count < 10)`
	- Sentinel-controlled loop, used with `for ( )` and `while ( )`  
		- Indicates loop until a special value is encountered, i.e. while  (`array[i] != ‘\0’`)  
	- Endfile-controlled loop, best suited to be used with for ( ) and while ( )  
		- Indicates loop until the end of a file is reached, i.e. `while (status  != EOF)` or `while (!feof (infile))`  
		- EOF usually integer value `-1`
	- Input validation loop, used with `do-while ( )` 
		- Indicates loop until a value within valid range is entered by user, i.e. `do {//something} while (input != valid)`
	- General conditional loop, used with for ( ) and while ( )  
		- Indicates processing of data until a condition is met 

- **Selection Sort**
	- Read all indices of array, find minimum, swap with first element. Repeat but don't check the sorted index
```c
int arr[n] = {//numbers here};
for (int i = 0; i < n-1; i++) {
	int end_index = i;
	for (int j = i + 1; j < n; j++) {
		if (arr[j] < arr[end_index]) {
			end_index = j;
		}
		int temp = arr[i];
		arr[i] = arr[end_index];
		arr[end_index] = temp;
	}
}
```

- **Bubble Sort**
	- Check two consecutive indices, swap if next is smaller then earlier. Go to second to last index, repeat, lose an index each time.
```c
int arr[n] = {//numbers here};
for (int i = 0; i < n; i++) {
	int temp = 0;
	for (int j = 0; j < n-i-1; j++) {
		if (arr[j] < arr[j+1]) {
			temp = arr[j];
			arr[j] = arr[j+1];
			arr[j+1] = temp;
		}
	}
}
```

- **String to integer code**
```c
char my_str[n] = //"string here";
//remember, string length includes null terminator
int result = 0;
for (int i = 0; i < n - 1; i++) {
	int value = my_str[i] - '0';
	result *= 10;
	result += value;
}
printf("result: %d", result);
```

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
	- Declaration `type* ptr (i.e. int* ptr)`
	- Pointers are often applied when you want to modify multiple values in a function. If you pass the memory address of a value through a *pointer* into the function, you can manipulate it within the function by calling the address, and when you exit the function, the values are changed accordingly.

- **Distinguish between the multiple usages of the * operator with pointers**  
	- `int *ptr` – indicates the declaration of a pointer  
	- `*result = i + j` – indicates the dereferencing of a pointer (the operator is called the dereference or indirection operator). Dereferencing just means taking the contents of the address itself.

- **Define what is a direct value**
	- When not using a pointer and accessing a value, we are accessing a *direct* value. 
	- i.e. `int num = 50;` 50 is the direct value

- **Define what is an indirect value**  
	- Accessed via the dereference operator – meaning “follow the pointer”  

**Apply logical memory diagrams of pointers and how they relate to their indirect  
values**  

____

#### Chapter 7: Simple Data Types, Enumerated Types, and Arrays  

- **Identify the integer types in C**  
	- short, unsigned short, int, unsigned, long, unsigned long  
		- signed indicates negative and positive numbers are supported, this is the default type.
		- short consumes 16 bits, long int consumes 32 bits

- **Identify the floating-point types in C** 
	- float, double, long double  

- **Discuss problems with applying floating-point numbers to loop conditions**  
	- Floating point numbers are not completely precise, so they may lead to rounding errors, errors in comparisons such as `==`, etc.

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
	- The address of the 0th element, only, is copied and passed into the function  

- **How are arrays and pointers related?**  
	- Is array notation and pointer notation interchangeable?  
		- Pointer notation may always be used with arrays; array notation may replace pointer notation only if the pointer points to the start of an array  
- **Declare and apply parallel arrays**  
	- Parallel arrays may be replaced by an array of structs  

___

#### Chapter 8: Strings  

- **Define what is a string in C**  
	- A character array which contains alphabetic, numeric, and special characters, and is terminated by the null character (‘\0’).

- **Declare and apply an array of strings**  
	- An array of strings is simply a 2-dimensional array of characters where each row represents a string and the max length of each string is  determined by the max number of columns
	- `char* = "my_str";` declares an immutable string (contents cannot be edited)
	- `char[7] = "my_str";` declares a mutable string.

- **Apply string library functions <string.h>**  
	- `strlen ( )` – returns the length of a string, not including the null character  
	- `strcpy ( )` – makes a fresh character-by-character copy of a string  
	- `strcat ( )` – appends one string to the end of another string  
	- `strcmp ( )` – performs a character-by-character comparison based on ASCII values (remember, lowercase ASCII is bigger then uppercase)
		- returns 0 if the strings are equal (case does matter), < 0 if string1 is less than string2, or > 0 if string1 > string2  
- **Write functions which mimic the four listed string library functions above, without calling the string library functions**  
	- Apply array and/or pointer notation to these functions  
- **Declare and apply arrays of pointers, i.e. `char *array_ptrs[10]`** 
- **Distinguish between scanf ( ) and gets ( ) related to strings**  
- **Apply the character operations found in `<ctype.h> `** 
	- These include: `isalpha ( )`, `isdigit ( )`, `islower ( )`, `isupper ( )`, `toupper ( )`,  
`tolower ( )`, `ispunct ( )`, `isspace ( )`, `isalnum ( )`  

___

#### Chapter 10: Structs  

- **Define what is a structure in C**  
	- A collection of related fields or variables under one name  
	- May be used to describe real world objects  

- **Define what is encapsulation**  
	- Encapsulation is the grouping of multiple datatypes and various data under one name into the struct.
- **Declare and apply structs**  
	- Declare, initialize, and print out struct information  
```c
//Struct Declaration
struct my_struct {
	int my_int;
	double my_double;
	char my_char;
}
```

- **Declare and apply arrays of structs**  
	
- **What is the . operator and what is the -> operator?**  
	`.` operator allows you to access items and modify items in a struct
	
```c
typedef struct _my_struct {
	int my_int;
	double my_double;
	char my_char;
} my_struct

my_struct Hello = {0, 3, 'c'};
printf("%d", Hello.my_int);
//returns 0
```
- **Can the assignment (=) operator be applied to structs?**  
	- Yes, the assignment operator copies one struct to another  

___
#### Other Topics  

- **Apply pointer arithmetic**  
	- For example, `ptr++`, `ptr + index`, `--ptr`, etc. 