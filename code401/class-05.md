# Linked Lists

> Sequence of Nodes linked together. Each Node references the next node in the link.

- Singly linked list has only one reference to the next Node.Only go in one direction.
- Doubly linked list has two references, one to the next Node and one to th previous Node. This can be helpful if we wanted to be able to traverse our data structure not just in a single track or direction, but also backwards, too. Gives the ability to hop between one node and the node previous without having to go back to the very beginning of the list
- Nodes are individual items, Each node contains the data for each link.
- Each node contains a property called Next. This property contains the reference to the next node.
- Head - The Head is a reference type of type Node to the first node in a linked list.
- Current - The Current reference is a reference type of type Node that is currently being looked at.


- When traversing a linked list,use Next property. (can't use forEach or for loop) Use While loop. programm will stop when reaching a Node that is null.

### What’s a Linked List, Anyway?
- linked lists are linear data structures: we have to go through all of the items in the list in order, or sequentially.
- Linked lists don't need to be contiguous in memory, they can grow dynamically.
- linked lists are dynamic data structures: can shrink and grow in memory. It doesn’t need a set amount of memory to be allocated in order to exist, and its size and shape can change, and the amount of memory it needs can change as well.

> A node only knows about what data it contains, and who its neighbor is.

### Big O
- about efficiency and tradeoffs
- a way of evaluating the performance of an algorithm.
- Think about how much time it requires at runtime given how much time and memory it needs.
- "O" refers to order
- n is the size of the input
- O(1) function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm.
- O(n) function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and time that we need to run that algorithm grows linearly.
-  O(n²) function takes exponentially more time and memory the more elements that you have.

### Growing a linked list
- to add something to our linked list: figure out which pointer needs to point to where.

#### insert an element into a linked list at the very beginning
- find the head node of the linked list.
- make new node, and set its pointer to the current first node of the list.
- rearrange our head node’s pointer to point at our new node.
- Inserting an element at the beginning of a linked list is efficient:takes the same amount of time, no matter how long our list is, has a space time complexity that is constant, or O(1).

#### insert an element at the end of a linked list
- Find the node we want to change the pointer of (in this case, the last node)
- Create the new node we want to insert and set its pointer (in this case, to null)
- Direct the preceding node’s pointer to our new node
- Takes more time, have to traverse the entired linked list to find it. Space time complexity is O(n)

> a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element.