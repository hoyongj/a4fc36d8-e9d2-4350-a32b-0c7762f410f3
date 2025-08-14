
# 📚 CMPT 225 – Week 7 Key Definitions

## 1. **Binary Tree**

* **Binary Tree** – A tree where each node has at most two children (left and right).

---

## 2. **Linked Structure for Binary Trees**

* **Node Structure**:

  * `element`: Data stored in the node.
  * `parent`: Pointer to the parent node.
  * `left`: Pointer to the left child.
  * `right`: Pointer to the right child.
* **LinkedBinaryTree**: Class holding a `root` pointer and `size`.

---

## 3. **Array-Based Binary Tree**

* **Index Mapping Rules**:

  * Root node `v`: $f(v) = 1$
  * Left child of node `u`: $f(v) = 2f(u)$
  * Right child of node `u`: $f(v) = 2f(u) + 1$
  * Index 0 is unused for formula simplicity.
* **Advantages**:

  * O(1) access by index.
  * No pointers; simpler parent/child calculation.
  * Less chance of memory leaks.
  * Best for complete or nearly complete binary trees.
* **Disadvantages**:

  * Wasted space for sparse trees.
  * Resizing overhead.
  * Poor for unbalanced trees.
* **Sparse Tree Space**:

  * Array size for height $h$: $2^{h+1} - 1$ elements.
  * Minimum nodes for height $h$: $h + 1$.

---

## 4. **Tree Traversal – Inorder**

* **Inorder Traversal**:

  1. Visit left subtree.
  2. Visit current node.
  3. Visit right subtree.
* **Array Implementation**: Index-based recursive calls.
* **Linked Implementation**: Pointer-based recursive calls.

---

## 5. **Binary Search Tree (BST)**

* **BST Property**:

  * For every node:

    * Left subtree elements < node’s element.
    * Right subtree elements > node’s element.
* **Tree Search**:

  * Recursively compare key to current node’s element.
  * Traverse left or right accordingly.
  * External nodes (null children) left blank.
* **Search Complexity**:

  * $O(h)$ where $h$ is tree height.
  * Not guaranteed $O(\log n)$ unless balanced.

---

## 6. **BST Implementation Notes**

* **isExternal(v)**: Returns true if node `v` has no children.
* **treeSearch(key, v)**:

  * Base case: External node → return it.
  * Recursive case: Compare key and traverse left/right.
* **Insertion**:

  * Find external position via search.
  * Replace with internal node containing the key.
  * Add two external children.

