EX 1 
TASK 1
### Summary of the Code:

The code defines a basic implementation of a singly linked list with a **dummy header node**. The linked list is implemented using two classes: `Node` and `LinkedList`.

1. **`Node` Class**: 
   - Represents a node in the linked list.
   - Each `Node` object has two attributes: `data` (which holds the value of the node) and `next` (which holds the reference to the next node in the list).
   - The constructor initializes the `data` to the provided value and sets the `next` pointer to `None`.

2. **`LinkedList` Class**:
   - Represents the linked list that contains a dummy header node to simplify insertion and deletion operations.
   - The constructor initializes the linked list by creating a dummy node. 
     - This dummy node doesn't hold any meaningful data (`data` is set to `None`), but it serves as a placeholder, ensuring that every node (even the head) has a predecessor.
   - The `head` pointer of the list is set to the dummy node, making the list ready for other operations.

The dummy node allows the list to handle operations uniformly, even when it's "empty," simplifying edge cases like inserting or deleting the first node.
Data Structure (Node): Each node in the linked list is represented by the structure Node with a data field (in this case, assumed to hold a char value) and a next pointer pointing to the next node in the list.

Initial Pointers:

last1 points to the last node of the first circular linked list (which contains POWER).
last2 points to the last node of the second circular linked list (which contains POINT).
Merging Logic:

The mergeCircularLists function connects the last node of the first list (last1) to the first node of the second list (last2->next).
It then connects the last node of the second list (last2) to the first node of the first list (last1->next), forming a merged circular linked list.
Finally, last1 is updated to point to last2, which now becomes the last node of the merged list.
Result: After the merge, the contents of the two circular linked lists (POWER and POINT) are combined into a single circular linked list with the contents POWERPOINT.

This code ensures that the two circular linked lists are properly merged without breaking their circular nature.


TASK 2
o implement a Linked List with a Dummy Head Node for a list of integers in C++, we first need to define the structure of the linked list (HList) and the Node. We'll also implement the required member functions, including the constructor and the function to check if the list is empty.

Class Node: Each node in the list will store an integer value and a pointer to the next node.
Class HList: This will manage the linked list with a dummy head node.
The head pointer will always point to the dummy head node, even if the list contains no real data.
The constructor (HList()) initializes the list by creating the dummy node.
A method to check if the list is empty (isEmpty()) will compare if the next node after the dummy head is nullptr, which indicates that the list contains no real elements.

EXERCISE 1 
In the following, we are implementing a singly linked list with a dummy head node, and here’s what each function in the class does:

1. bool emptyList();
Purpose: Checks if the list is empty or not.
How: It returns true if the list contains no real data nodes (i.e., if the next node after the dummy head node is nullptr), and false otherwise.
Purpose: Inserts a new node with the value newV after the node that contains oldV.
How: The list is traversed to find the node with the value oldV. Once the node is found, a new node containing newV is created and inserted after it.
EXERCISE 2
To implement a Circular Linked List class CList for integers, we need to define a Node structure and the member functions of the class as described. A circular linked list is a type of linked list where the last node points back to the first node, forming a continuous loop.
Class CList Overview:
Private Member:
Node* head: Points to the head (first node) of the circular linked list.
Public Member Functions:
Constructor (CList()): Initializes an empty circular linked list.
emptyList(): Checks if the list is empty.
insert_at(pos, value): Inserts a node with a specific value at a given position (except position 1).
insert_begin(value): Inserts a node at the beginning of the list.
insert_end(value): Inserts a node at the end of the list.
deleteNode(pos): Deletes a node at a given position (except the first node).
delete_begin(): Deletes the first node from the list.
delete_end(): Deletes the last node from the list.
traverse(): Displays the values in the list.
