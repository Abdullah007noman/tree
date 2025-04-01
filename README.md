# Tree Implementation
In this repository I have implemented differtent types of tree ,such as:
 * The basic Binary Search Tree
 *  Red Black Tree
 *  AVL Tree
# The basic Binary Search Tree
This repository contains a simple, yet comprehensive implementation of a Binary Search Tree (BST) data structure in Python. This implementation focuses on clarity and correctness rather than advanced optimizations.
## Features
* Basic BST operations (insert, search, delete)
* Tree traversals (inorder, preorder, postorder)
* Utility functions (min, max, height, size, empty check)
* BST property validation
* Comprehensive test suite

## Implementation Details
The implementation consists of two main classes:
  * Node: Represents a single node in the tree with a value and references to left and right children
  * BinarySearchTree: The main BST class that contains all the operations
## Limitations
This is a basic BST implementation with the following limitations:

* Not self-balancing (can become unbalanced with certain insertion orders)
* No duplicate handling strategy (currently, duplicates go to the right subtree)
* Integer values only (can be easily modified for other comparable types)
## Usage Example
``` python
from bst import BinarySearchTree

# Create a new BST
bst = BinarySearchTree()

# Insert values
bst.insert(50)
bst.insert(30)
bst.insert(70)
bst.insert(20)
bst.insert(40)

# Check if values exist
print(bst.search(30))  # True
print(bst.search(100))  # False

# Get tree properties
print(bst.size())  # 5
print(bst.height())  # 2
print(bst.get_min())  # 20
print(bst.get_max())  # 70

# Traverse the tree
print(bst.inorder_traversal())  # [20, 30, 40, 50, 70]

# Delete a value
bst.delete(30)
print(bst.inorder_traversal())  # [20, 40, 50, 70]
```
# Red Black Tree
