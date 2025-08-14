Here’s the **definition summary** for the uploaded **Week 6** files, without including any previous weeks’ content:

---

## **Iterators**

* **Iterator** – Abstracts the process of scanning through a collection; behaves like a pointer to an element (`*p`, `++p`).
* **Container** – Data structure that supports element access via iterators.
* **Types of iterators**:

  * **iterator** – Read-write.
  * **const\_iterator** – Read-only.
  * **bidirectional iterator** – Supports `++p` and `--p`.
  * **random-access iterator** – Supports `p + i` and `p - i`.
* **Array-based iterator** – Uses an index to track position.
* **Linked list-based iterator** – Uses a pointer to the current node.

---

## **Trees**

* **Tree** – Non-linear data structure made of **vertices (nodes)** connected by **edges**, without cycles.
* **Empty tree** – No vertices.
* **Leaf** – Node with degree 1.
* **Internal node** – Node with degree > 1.
* **Distance** – Number of edges between two nodes.
* **Rooted tree** – A tree with a designated **root** node.
* **Parent / Child** – Immediate neighbors in a root-directed hierarchy.
* **Ancestor / Descendant** – Nodes on the path to/from the root.
* **Subtree** – Node plus all its descendants.
* **Depth** – Number of edges from a node to the root.
* **Height** – Maximum depth of any node.

---

## **Tree ADT**

* **Element(p)** – Returns element in node `p`.
* **Root()** – Returns root node.
* **Parent(p)** / **Children(p)** – Returns parent or children of `p`.
* **isInternal(p)** / **isExternal(p)** – Checks if `p` is internal or a leaf.
* **isRoot(p)** – Checks if `p` is the root.
* **Size()** – Number of nodes.
* **isEmpty()** – Checks if tree has nodes.
* **Iterator()** – Iterates over elements.
* **Positions()** – Returns all positions in the tree.
* **Replace(p, e)** – Replaces element in `p` with `e`.

---

## **Special Types of Trees**

* **Ordered tree** – Children have a defined order.
* **Balanced tree** – Height difference between subtrees ≤ 1.
* **Complete tree** – All levels filled except last, filled left to right.
* **Perfect tree** – All levels completely filled.
* **Binary tree** – Each node has ≤ 2 children.
* **Binary search tree** – Left subtree elements < node’s element < right subtree elements.

---

## **Traversals**

* **Preorder** – Visit node, then children.
* **Postorder** – Visit children, then node.
* **Inorder** (binary trees) – Visit left child, node, then right child.

---

## **Binary Tree Properties**

Given height `h`, nodes `n`, external nodes `e`, internal nodes `i`:

* **Max nodes**: `n ≤ 2^(h+1) - 1`
* **Max external nodes**: `e ≤ 2^h`
* **Max internal nodes**: `i ≤ 2^h - 1`
* **Height range**: `log₂(n+1) - 1 ≤ h ≤ n - 1`

---

Do you want me to also make **a compact table version** of this so it’s easy to revise? That would make it even quicker to study.
