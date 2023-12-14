
## Chapter 9: Recursion  

- **Define what is recursion**  
Recursion is the process in which a function/algorithm calls itself.

- **Define what is a base case and what is a recursive step**  
Base case is the simplest scenario where the problem is solved directly without further recursion. It is where the recursion eventually ends.
Recursive step is where the problem is broken into smaller subproblems by calling the same function

- **Define what is a recursive function**  
A recursive function is a function that calls itself in its algorithm.

- **Define what is a function call stack**  
- **Diagram the function and return sequence of a particular recursive solution**  
- **Convert between iterative and recursive solutions and vice versa**  
- **Apply and implement recursive functions to solve a problem**  

## Appendix C: Bit Manipulation

- **Define what is a bit**  
	- Recall a bit is a single binary digit – 0 or 1  
- **Define what is a nibble and byte**  
	- A nibble is a sequence of 4 bits and a byte is a sequence of 8 bits  
- **Convert between binary and decimal numbers and vice versa**  
- **How can we determine if a number is even or odd without using the mod (%)  
operator?**  
	- If the least significant bit (lsb) is 1 the number is odd, if its 0 the number  
is even  
- **How do we multiply and divide by powers of 2 without using the multiplication  (`*`) and division (`/`) operators?**  
	- Recall multiplication and division is expensive and resource intensive
	- Shift all bits in a number to the left by 1 to multiply by 2
	- Shift all bits in a number to the right by 1 to divide by 2 
- **Apply bitwise operations to decimal numbers**  
	- These include: one's complement or negation (~), left shift (<<), right  shift (>>), AND (&), OR ( | ), and XOR (^)**

## Chapter 12: Programming in the Large  

- **Define what is a command line argument**  
- **Modify main ( ) to accept command line arguments**  
	- The arguments are argc and argv 
- **Extract strings from the command line arguments**  
- **Convert strings to integers using atoi( )**  

## Chapter 13: Dynamic Data Structures  

- **Define what is dynamic memory**  
	- Memory allocated at runtime from a memory area called the heap or memory store
- **Apply malloc( ) to allocate memory**  
- **Apply free( ) to de-allocate memory**  
- **Apply sizeof( )**  
	- Recall this returns the number of bytes allocated for a type or variable
	- e.g. `sizeof(int)` returns 4 (usually).
