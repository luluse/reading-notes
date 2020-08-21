# [Stacks & Queues](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-10/resources/stacks_and_queues.html)

## What is a Stack

- data structure that consists of Nodes
- Each Node references hte next Node

- Push - Nodes or items that are put into the stack are pushed. When you push something to the stack, it becomes the new top
- Pop - Nodes or items that are removed from the stack are popped. When you pop something from the stack, you pop the current top and set the next top as top.next.
- Top - This is the top of the stack.
- Peek - When you peek you will view the value of the top Node in the stack. 
- IsEmpty - returns true when stack is empty otherwise returns false.

### FILO
First In Last Out

- This means that the first item added in the stack will be the last item popped out of the stack.

### LIFO
Last In First Out

- This means that the last item added to the stack will be the first item popped out of the stack.

### Push O(1)

Will always be an O(1) operation
```
ALOGORITHM push(value)
// INPUT <-- value to add, wrapped in Node internally
// OUTPUT <-- none
   node = new Node(value)
   node.next <-- Top
   top <-- Node
```

### Pop O(1)
When conducting a pop, the top Node will be re-assigned to the Node that lives below and the top Node is returned to the user.

```
ALGORITHM pop()
// INPUT <-- No input
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   Node temp <-- top
   top <-- top.next
   temp.next <-- null
   return temp.valu
```

### Peek O(1)

Only inspect the top Node of the stack.

```
ALGORITHM peek()
// INPUT <-- none
// OUTPUT <-- value of top Node in stack
// EXCEPTION if stack is empty

   return top.value
```

## What is a Queue

- Enqueue - Nodes or items that are added to the queue.
- Dequeue - Nodes or items that are removed from the queue. 
- Front - This is the front/first Node of the queue.
- Rear - This is the rear/last Node of the queue.
- Peek - When you peek you will view the value of the front Node in the queue. 

### FIFO
First In First Out

- first item in the queue will be the first item out of the queue.

### LILO
Last In Last Out

- last item in the queue will be the last item out of the queue.

### Enqueue O(1)

```
ALGORITHM enqueue(value)
// INPUT <-- value to add to queue (will be wrapped in Node internally)
// OUTPUT <-- none
   node = new Node(value)
   rear.next <-- node
   rear <-- node
```

### Dequeue O(1)

```
ALGORITHM dequeue()
// INPUT <-- none
// OUTPUT <-- value of the removed Node
// EXCEPTION if queue is empty

   Node temp <-- front
   front <-- front.next
   temp.next <-- null

   return temp.value
```
