### C Data Structures  
>[!book] **Compare and contrast the terms Abstract Data Types (ADTs) and data structures**  
> - For ADT think: “specification”; for data structure think: “implementation”  

>[!book] **Declare, define, and apply a self-referential structure**  
> - Nodes for linked lists and stacks require self-referential structures  
> - Self-referential structure is a data structure where elements contain references to other parts of the structure of the same type.
```c
typedef struct _node {
	int value;
	struct _node *pNext;
} Node;
```


>[!book] **Define what is dynamic memory**  
>Memory allocation and deallocation during execution of program at runtime.

>[!book] **Define what is a dynamic data structure**  
> Type of data structure that can change size during execution of a program. This includes linked lists, stacks, and trees.

**Apply malloc ( ) and free ( ) to dynamic data structures**

**Compare and contrast linked lists and stacks implemented with linked lists**  

**Design and implement an ordered or non-ordered dynamic (singly and doubly) linked list including and variations of the following:**  
- `isEmpty ( )` - returns an integer or enumerated Boolean type; true for an  
empty list, false for non-empty list  
```c
bool isEmpty(Node *pList) {
	if (*pList == NULL) {
		return FALSE;
	}
	return TRUE;
}
```
- `insertAtFront ( )` – allocates a node dynamically; initializes it to the data  
passed in; inserts the node at the front of the list only; returns true or  
false for successful or unsuccessful insertion, respectively  
```c
Node* createNode(Data newData) {
	Node* node = malloc(sizeof(Node));
	if (node != NULL) {
		node->data = newData;
		node->pNext = NULL;
	}
	return node;
}
bool insertAtFront(Node **pList, Data newData) {
	Node* pMem = createNode(newData);
	if (pMem != NULL) { //memory successfully allocated
		pMem->pNext = *pList;
		*pList = pMem;
		return TRUE;
	}
	return FALSE;
}
```
- `insertAtBack ( )` - allocates a node dynamically; initializes it to the data  
passed in; inserts the node at the back or end of the list only; returns  
true or false for successful or unsuccessful insertion, respectively  
```c
bool insertAtBack(Node **pList, Data newData) {
	Node* pMem = createNode(newData);
	Node* pCur = *pList;
	pMem->pNext = NULL;
	if (pMem != NULL) { //memory successfully allocated
		if (*pList == NULL) {
			*pList = pMem;
		}
		else {
			while(pCur->pNext != NULL) {
				pCur = pCur->pNext;
			}
			pCur->pNext = pMem;
		}
		return TRUE;
	}
	return FALSE;
}
```
- `insertInOrder ( )` - allocates a node dynamically; initializes it to the data  
passed in; inserts the node in the list in ascending or descending order  
only; returns true or false for successful or unsuccessful insertion, respectively  
```c
bool insertInOrder(Node **pList, Data newData) {
	Node *pMem = createNode(newData);
	Node* pCur = *pList;
	Node* pPrev = NULL;
	if (pMem != NULL) {
		while (strcmp(newData, pCur->data) < 0 && pCur != NULL) {
			pPrev = pCur;
			pCur = pCur->pNext;
		}
		if (pPrev == NULL) { //empty list or insert at front
			if (pCur != NULL) {
				pMem->pNext = *pList;
			}
			*pList = pMem;
		}
		else { //insert at middle
			pPrev-pNext = pMem;
			pMem->pNext = pCur;
		}
		return TRUE;
	}
	else {
		return FALSE;
	}
}
```
- `deleteAtFront ( )` – de-allocates the node at the front of the list; returns  
the data in the node  
- `deleteNode ( )` – de-allocates a node; returns true if node was de-  
allocated, false otherwise  
- `printList ( )` – prints out the data in each node of the list; may be printed  
iteratively or recursively  

**Design and implement `makeNode ( )` as a separate helper function for each of**  
**the above data structures**  
- `makeNode ( )` – allocates a node dynamically; initializes the node; returns a pointer to the dynamic node  
```c
Node* makeNode(data newData) {
	Node* node = malloc(sizeof(Node));
	if (node != NULL) {
		node->data = newData;
		node->next = NULL;
	}
	return node;
}
```
Design and implement functions that expand on the basic list operations.  
Example functions include, but are not limited to:  
- `mergeLists ( )` – join two linked lists  
- `insertAtPosN ( )` – insert data at position N in the list  
- `compareLists ( )` – check to see if two lists have the same data  
```c
bool compare_lists(SinglyLinkedListNode* head1, SinglyLinkedListNode* head2) {
	while (head1 != NULL && head2 != NULL && head1->data == head2->data) {
		head1 = head1->next;
		head2 = head2->next;
	}
	if (head1 == NULL && head2 == NULL) {
		return true;
	}
	else {
		return false;
	}
}
```

- `reverseList ( )` – reverse the links in a singly linked list  
```c
Boolean reverseList(Node** pList) {
    Node* pCur = *pList;
    Node* pPrev = NULL;
    Node* temp = NULL;
    if (*pList != NULL) {
        while (pCur != NULL) {
            temp = pCur->pNext;
            pCur->pNext = pPrev;
            pPrev = pCur;
            pCur = temp;
        }
        *pList = pPrev;
    }
    return true;
}
```
- others...  

**Given a problem, describe which data structure is most appropriate**  
- For example:  
	- Converting infix expression to postfix expressions (stack)  
	- Storing personal contact information (list)  
- Draw block/memory diagrams to illustrate how links are modified for any of the particular operations described above  

**Design and implement a list with arrays instead of dynamic “links”**  

**Define what is a memory leak**  
- Think: lost pointer to dynamically allocated memory; can’t access the  
memory anymore, but memory is still allocated by system on the heap  

**Define what is a dangling pointer**  
- Think: have a pointer to memory that is no longer accessible  

**What is defensive programming?**  
- We check to see if lists are empty inside our corresponding removal  
functions
- Some implementations add preconditions to `deleteNode ( )` not empty  

### Other Topics  
Compare and contrast char `*str` vs. `str[]`, and char `*str[]` vs. `char str[][]`  
1. A `char *` needs to point to some allocated memory; this memory may be  
allocated dynamically or via another automatic local variable  
2. A `str[]` has memory associated with it; str refers to the address of the 0th  
element in the array  
3. A char `*str[]` is an array of pointers; where each pointer could refer to  
dynamically allocated memory or automatic local variable memory  
4. A `str[][]` may be considered an array of strings or a 2-D array of  
characters; all required memory is allocated upfront; str[] (one index  
specified) refers to the start of the corresponding row  

**Compare and contrast strings vs. character arrays**  

**What is the three-file format?**  

**What is a model? How do they apply to software development?**