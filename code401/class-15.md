# Trees

- Node - A node is the individual item/data that makes up the data structure
- Root - The root is the first/top Node in the tree
- Left Child - The node that is positioned to the left of a root or node
- Right Child - The node that is positioned to the right of a root or node
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not contain any children
- Height - The height of a tree is determined by the number of edges from the root to the bottommost node

Traversing a tree allows us to search for a node, print out the contents of a tree, and more.
There are two categories:

### **Depth First**

- prioritize going through the depth (height) of the tree first. three methods for depth first traversal:
  - Pre-order: `root >> left >> right`
  - In-order: `left >> root >> right`
  - Post-order: `left >> right >> root`


The most common way to traverse through a tree is to use recursion. With these traversals, we rely on the call stack to navigate back up the tree when we have reached the end of a sub-path.

```
ALGORITHM preOrder(root)

  OUTPUT <-- root.value

  if root.left is not NULL
      preOrder(root.left)

  if root.right is not NULL
      preOrder(root.right)
```

```
ALGORITHM inOrder(root)
// INPUT <-- root node
// OUTPUT <-- in-order output of tree node's values

    if root.left is not NULL
        inOrder(root.left)

    OUTPUT <-- root.value

    if root.right is not NULL
        inOrder(root.right)
```

```
ALGORITHM postOrder(root)
// INPUT <-- root node
// OUTPUT <-- post-order output of tree node's values

    if root.left is not NULL
        postOrder(root.left)

    if root.right is not NULL
        postOrder(root.right)

    OUTPUT <-- root.value
```

### **Breadth First**

Breadth first traversal iterates through the tree by going through each level of the tree node-by-node. So, given our starting tree one more time:

Traditionally, breadth first traversal uses a queue (instead of the call stack via recursion) to traverse the width/breadth of the tree.

```
ALGORITHM breadthFirst(root)
// INPUT  <-- root node
// OUTPUT <-- front node of queue to console

  Queue breadth <-- new Queue()
  breadth.enqueue(root)

  while breadth.peek()
    node front = breadth.dequeue()
    OUTPUT <-- front.value

    if front.left is not NULL
      breadth.enqueue(front.left)

    if front.right is not NULL
      breadth.enqueue(front.right)
```
## Binary Trees

- Trees can have any number of children per node. 
- Binary Trees restrict the number of children to two (left and right children).
- There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows
- One strategy for adding a new node to a binary tree is to fill all “child” spots from the top down.
- During the traversal, we find the first node that does not have 2 child nodes, and insert the new node as a child. We fill the child slots from left to right.

### Big O
#### Time complexity:
- inserting a new node is O(n)
- Searching for a specific node will also be O(n)

#### Space complexity:
- node insertion using breadth first insertion will be O(w), where w is the largest width of the tree.

## Binary Search Trees
- has some structure
- values that are smaller than the root are placed to the left
- values that are larger than the root are placed to the right

### Searching a BST
- Searching a BST can be done quickly
- compare the node you are searching for against the root of the tree or sub-tree
- If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.
- best way to approach a BST search is with a while loop
- cycle through the while loop until we hit a leaf, or until we reach a match with what we’re searching for

### Big O
#### Time complexity:
- O(height)
#### Space complexity:
- O(1). During a search, we are not allocating any additional space.