- Define what is a dynamic data structure in C++
- Apply new and delete to dynamic data structures
- Compare and contrast linked lists, stacks, queues, and BSTs
- Compare and contrast container and value classes
- Design and implement an ordered or non-ordered dynamic linked list using C++ classes including the following methods:
- `isEmpty ( )` - returns an integer or bool type; true for an empty list, false for non-empty list
```cpp
bool List::isEmpty() {
	return (pHead == nullptr);
}
```
- `insertAtFront ( )` – allocates a node dynamically; initializes it to the data passed in; inserts the node at the front of the list only; returns true or false for successful or unsuccessful insertion, respectively
```cpp
template<typename T>
bool List::insertAtFront(T newData) {
	Node<T>* pMem = new Node<T>(newData);
	if (pMem != nullptr) {
		pMem->setNext(pHead);
		pHead = pMem;
		return true;
	}
	return false;
}
``` 
- insertAtEnd ( ) - allocates a node dynamically; initializes it to the data passed in; inserts the node at the tail or end of the list only; returns true or false for successful or unsuccessful insertion, respectively
- insertInOrder ( ) - allocates a node dynamically; initializes it to the data passed in; inserts the node in the list in ascending or descending order
only; returns true or false for successful or unsuccessful insertion,
respectively

o deleteNode ( ) – de-allocates a node dynamically; returns true if node
was de-allocated, false otherwise
o printList ( ) – prints out the data in each node of the list; may be printed
iteratively or recursively
o others?
Design and implement a dynamic linked stack (LIFO – last-in, first-out) using
C++ classes including the following methods:
o isEmpty ( ) - returns an integer or enumerated bool type; true for an
empty stack, false for non-empty stack
o push ( ) - allocates a node dynamically; initializes it to the data passed
in; inserts the node at the top of the stack only; returns true or false for
successful or unsuccessful insertion, respectively
o pop ( ) - de-allocates a node at the top of the stack dynamically; returns
true if node was de-allocated, false otherwise; NOTE: some variations of
pop ( ) will return the data in the node found at the top of the stack,
instead of true or false
o top ( ) or peek ( ) – returns the data found in the top node of the stack;
nodes are not affected (removed)
o printStack ( ) - prints out the data in each node of the stack; may be
printed iteratively or recursively
Design and implement a dynamic linked queue (FIFO – first-in, first-out) using
C++ classes including the following methods:
o isEmpty ( ) - returns an integer or enumerated bool type; true for an
empty queue, false for non-empty queue
o enqueue ( ) - allocates a node dynamically; initializes it to the data
passed in; inserts the node at the tail/e of the queue only; returns true
or false for successful or unsuccessful insertion, respectively
o dequeue ( ) - de-allocates a node at the head/front of the queue
dynamically; returns the data in the node found at the head/front of the
queue; NOTE: some implementations may also return true or false for
successful or unsuccessful removal of a node from the head/front
o printQueue ( ) - prints out the data in each node of the queue; may be
printed iteratively or recursively
Design and implement a dynamic linked binary search tree (BST) using C++
classes including the following methods:
o isEmpty ( ) - returns an integer or enumerated bool type; true for an
empty BST, false for non-empty BST
o insert ( ) – allocates a node dynamically; initializes it to the data passed
in; inserts the node into the left or right subtree; returns true or false
for successful or unsuccessful insertion, respectively
o inOrder ( ) – performs an inorder traversal of a BST and prints out the
data in the nodes accordingly
Inorder left, process, right
o preOrder ( ) – performs a preorder traversal of a BST and prints out the
data in the nodes accordingly
Process, left, right
o postOrder ( ) - performs a postorder traversal of a BST and prints out the
data in the nodes accordingly
Left, Right, Process
o destroyTree () – removes all nodes in the tree
Design and implement makeNode ( ) as a separate helper function for each of
the above data structures
o makeNode ( ) – allocates a node dynamically; initializes the node;
returns a pointer to the dynamic node
How would you make use of private and public member functions for each of
the container classes? Could you design a public preorder () function, which
calls upon a private preorder () helper function? Etc.
Draw block/memory diagrams to illustrate how links are modified for any of the
particular operations described above
Design and implement a list, stack, and queue with arrays instead of dynamic
“links”
### Chapters 1 - 3: Introduction to Classes and Objects
Design and implement classes in C++
o What are some advantages to using classes?
Design and apply data members and member functions for classes
Define and apply accessor (getter) functions and mutator (setter) functions
Define access specifier
o These include private, protected, and public
Apply UML Class Diagrams
Apply and implement default constructors, copy constructors, and destructors
How is the size (amount of memory) of an object determined?
o We generally assume an object contains data and
operations…However, each instance of an object uses the same copy
of the member functions, which is separate from the object size
o Sizeof reports only the number of bytes required for a class’s data
members
What is the rule of three/Law of the Big Three/the Big Three?
o Rule of thumb in C++: should define destructor, copy constructor, and
overloaded copy assignment operator
### Chapter 6 & 9: Classes: A Deeper Look
Compare and contrast procedural programming (C) versus objected-oriented
programming (C++)
Define the term encapsulation
o Wrapping of attributes and operations into objects
Define the term information hiding
o Implementation details are hidden within objects
Define and apply function overloading
o Allows for functions with the same name to be defined. The key is the
functions must have different parameters (number, type, order)
Define and apply procedural abstraction
Define and apply data abstraction
What is a data member (attribute)? What is a member function (operation)?
Define and apply function templates
Apply the reference (&) operator in C++, including returning references from
functions
Define pass-by-reference and pass-by-value
What is a dangling reference?
Define, implement, and apply friend functions and classes
o Recall: a friend class has access to private members
What is the this pointer? When do we need to use it?
Apply dynamic memory management with new and delete operators
What is a const object and const member function?
What is class composition?
o Recall: represents a “has-a” relationship
### Chapter 10: Operator Overloading
List the operators that may not be overloaded (there are four of them…)
o Recall: precedence, associativity, and number of operands (arity) for an
operator may not be changed
Implement and apply overloaded stream insertion and extraction operators
Implement and apply overloaded unary operators
Implement and apply overloaded binary operators (+, -, \*, /, etc.)
Compare and contrast overloaded member operators versus non-member
operators
Define what is a forward class declaration
Chapters 18 & 19: Templates
What is a function template?
What is a class template?
Design, implement, and apply templates
What are advantages and disadvantages of templates?
Other Chapters/Topics (More in chapters 6, 7, & 14)
What is a function call stack?
Apply recursion to a given set of problems, including BSTs
What is a stream? What is a file stream?
Open, read from/write to, and close files in C++
Analyze an algorithm and provide the Big-O time and space complexities