# Trees
## Binary Search Tree
A Binary Search Tree (BST) is recursively defined as a binary tree which has the following properties:

The left subtree of a node contains only nodes with keys less than the node's key.  

The right subtree of a node contains only nodes with keys greater than or equal to the node's key.  

Both the left and right subtrees must also be binary search trees.

### Complete BST
A Complete Binary Tree (CBT) is a tree that is completely filled, with the possible exception of the bottom level, which is filled from left to right.  

Now given a sequence of distinct non-negative integer keys, a unique BST can be constructed if it is required that the tree must also be a CBT. You are supposed to output the level order traversal sequence of this BST.