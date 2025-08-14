
## **AVL Trees**

* **Meaning**: AVL stands for *Adelson-Velsky and Landis* (inventors).
* **Purpose**: A height-balanced variant of a Binary Search Tree (BST) to ensure logarithmic height.
* **Height-Balancing Property**:
  For every internal node *v*, the heights of its left and right children differ by **at most 1**.
  Height bound: $h < 2 \log_2 n + 2 = O(\log n)$.
* **Node Structure**:
  Stores the same data as a BST plus the height of the node.
* **Balance Factor**:
  $\text{balance factor} = \text{height(right child)} - \text{height(left child)}$.
* **Rotations**:

  * **Left rotation**
  * **Right rotation**
  * **Double rotations**: Left-Right or Right-Left (a.k.a. Trinode Restructuring).
* **Trinode Restructuring**:
  Let (*a*, *b*, *c*) be the in-order order of nodes *x*, *y*, *z*.
  Perform rotations so *b* becomes the topmost of the three.
* **Insertion/Removal**:
  Done like in BST but may require rotations to restore balance.
* **Performance**:
  Search, insert, and remove are $O(\log n)$; a single restructure is $O(1)$.

---

## **Multi-Way Search Tree**

* **Definition**: An *ordered* tree where each internal node can have multiple children and multiple key-value entries.
* **d-node**: Node with *d* children.
* **Rules**:

  1. **Minimum Child Requirement**: Internal nodes have at least 2 children.
  2. **Key–Child Correlation**: A *d*-node has *d – 1* keys in sorted order.
  3. **Interleaved Ordering**: Keys in each subtree are constrained between the keys in the parent node.

---

## **(2,4) Trees**

* **Also Called**: 2–3–4 Trees (a type of Multi-Way Search Tree).
* **Node Size Property**: Every internal node has **at most 4 children**.
* **Depth Property**: All external (leaf) nodes have the **same depth**.
* **Node Types**:

  * **2-node**: 2 children, 1 key.
  * **3-node**: 3 children, 2 keys.
  * **4-node**: 4 children, 3 keys.
* **Advantages**: Perfectly balanced; no rotations needed.
* **Insertion**:

  * Insert key into the appropriate leaf.
  * If overflow (>3 keys), split into two nodes and push the middle key up.
  * May cause cascading splits up to root.
* **Removal**:

  * Remove key from a leaf or swap with predecessor if internal.
  * If underflow (<1 key), either **transfer** a key from a sibling or **fuse** with sibling, possibly cascading upward.
* **Performance**:
  Height is $O(\log n)$. Search, insert, remove visit $O(\log n)$ nodes. Split/transfer/fusion are $O(1)$.

