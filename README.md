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
This repository also contains a complete implementation of a Red-Black Tree (RBT) data structure in Python. A Red-Black Tree is a self-balancing binary search tree where each node has an extra bit for denoting color (red or black), ensuring that the tree remains approximately balanced during insertions and deletions. This implementation supports integer keys and provides a variety of operations with rigorous testing.
## Features
 * Every node is either red or black.
 * The root is black.
 * All leaves (NIL nodes) are black.
 * If a node is red, both its children are black.
 * Every path from a node to its descendant leaves contains the same number of black nodes.
## Usage Example
``` python

# Create a new Red-Black Tree
tree = RedBlackTree()

# Insert some values
values = [10, 20, 30, 15, 25, 5, 35]
for value in values:
    tree.insert(value)

# Print the tree structure
print("Tree structure:")
tree.print_tree()

# Perform searches
print("\nSearch results:")
print(f"15 in tree: {15 in tree}")  # True
print(f"40 in tree: {40 in tree}")  # False

# Get traversals
print("\nTraversals:")
print(f"Inorder: {tree.inorder_traversal()}")  # Sorted order
print(f"Preorder: {tree.preorder_traversal()}")

# Delete values
tree.delete(20)
tree.delete(5)

# Print updated tree
print("\nTree structure after deleting 20 and 5:")
tree.print_tree()

# Verify properties
print("\nRed-Black properties valid:", tree.check_properties())

# Get tree height
print(f"Tree height: {tree.height()}")
```
# AVL Tree
A complete implementation of an AVL (Adelson-Velsky and Landis) tree data structure, which is a self-balancing binary search tree where the heights of the two child subtrees of any node differ by at most one.
## Features
 * Self-Balancing: Automatically maintains balance via rotations after insertions and deletions
 * Complete Operations: Includes insert, delete, search, and traversal methods
 * Visualization: Built-in display method to visualize the tree structure with heights
 * Comprehensive Testing: Includes test cases to verify all operations.



## Usage Example
``` python
from avl_tree import AVLTree

# Create a new AVL Tree
avl = AVLTree()

# Insert elements
avl.insert(10)
avl.insert(20)
avl.insert(30)

# Display the tree structure
avl.display()

# Search for an element
node = avl.search(20)
if node:
    print(f"Found node with key {node.key}")

# Get an in-order traversal (sorted)
sorted_elements = avl.inorder()
print(sorted_elements)  # [10, 20, 30]

# Delete an element
avl.delete(20)

``` 
