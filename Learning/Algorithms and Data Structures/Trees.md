---
date created: Tuesday, January 4th 2022, 10:53:47 am
date modified: Friday, April 8th 2022, 1:54:07 pm
---

# Trees

## Binary Search Tree

A Binary Search Tree (BST) is recursively defined as a binary tree which has the following properties:

The left subtree of a node contains only nodes with keys less than the node's key.

The right subtree of a node contains only nodes with keys greater than or equal to the node's key.

Both the left and right subtrees must also be binary search trees.

Insert:

- $O(n)$ - worst case
- $\Theta(logn)$ - balanced case

Search:

- $O(n)$ - worst case
- $O(logn)$ - balanced case

### Traversal

- pre-order
    - parent, left, right
    - good for copying trees
- in-order
    - left, parent, right
    - good for sorting
- post-order
    - left, right, parent
    - good for freeing

### Complete BST

A Complete Binary Tree (CBT) is a tree that is completely filled, with the possible exception of the bottom level, which is filled from left to right.

Now given a sequence of distinct non-negative integer keys, a unique BST can be constructed if it is required that the tree must also be a CBT. You are supposed to output the level order traversal sequence of this BST.

## AVL Tree

The AVL tree is a _self-balancing_ binary search tree.

A counter at each node is used to keep the tree balanced.

$counter_{node} = depth_{left} - depth_{right}$

Insert:

- ~~$O(n)$ - worst case~~
- $O(logn)$ - balanced case

Search:

- ~~$O(n)$ - worst case~~
- $O(logn)$ - balanced case

## 2-3-4 Tree

Binary trees have 2 pointers for each node.

2-3-4 trees have 2, 3, or 4 pointers for each node.

- insertion: always done on the bottom nodes
- nodes: broken up on the way down

time complexities:

- insertion: $\Theta(log_2n)$
- lookup: $O(log_2n)$

## B+ Trees

B+ trees are extensions of 2-3-4 trees.

- more keys per node: instead of 1…3 keys/node, have 1…512 keys/node
- same complexity class: different logarithm bases

They are commonly used within databases.
