Here’s the **Week 9 – CMPT 225 Definition Summary** from your uploaded files:

---

# 📚 CMPT 225 – Week 9 Key Definitions

## **Skip List**

* **Skip List** – A probabilistic data structure for ordered elements allowing fast search, insertion, and deletion.
* **Height (h)** – Number of levels in the skip list.
* **Coin Flip Mechanic** – Determines how many levels a new entry occupies.
* **QuadNode Structure** – Each node stores `data`, and pointers to `above`, `below`, `next`, and `prev`.
* **TowerNode Structure** – Each tower represented as a single node with an array of forward pointers.

**Complexity**:

* **Worst-case**: $O(n + h)$ for search, insert, remove.
* **Average**: $O(\log n)$ for search, insert, remove.
* **Space**: Average $O(n)$, worst $O(hn)$.

---

## **Dictionary ADT**

* **Dictionary** – Searchable collection of key–element pairs allowing duplicate keys.
* **Operations**:

  * `get(k)` – Return an entry with key $k$.
  * `getAll(k)` – Return all entries with key $k$.
  * `put(k, v)` – Insert new entry.
  * `remove(e)` – Remove a given entry.
  * `entrySet()` – Return all entries.
  * `isEmpty()` – Check if empty.
  * `size()` – Number of entries.
* **Implementations**:

  * Unordered linked list.
  * Hash table with separate chaining.
  * Ordered array (search table).
  * Skip list.

---

## **AVL Tree**

* **AVL Tree** – Self-balancing binary search tree.
* **Height-Balancing Property** – Heights of children differ by at most 1.
* **Height Bound** – $h < 2 \log_2 n + 2$, $O(\log n)$ complexity.
* **Balance Factor** – $\text{height(right)} - \text{height(left)}$.
* **Rotations**:

  * **Single Rotation** – Left or right.
  * **Double Rotation** – Left–Right or Right–Left.
* **Trinode Restructuring** – Rebalancing using three nodes $x, y, z$ ordered as $a, b, c$ in in-order traversal.

**Complexity**:

* Search, Insert, Remove: $O(\log n)$.
* Restructuring: $O(1)$ with linked structure.

---

## **(2, 4) Tree**

* **Multi-Way Search Tree** – Internal node can have multiple keys and children.
* **d-node** – Node with $d$ children.
* **Properties**:

  1. **Minimum Child Requirement** – Internal node has at least 2 children.
  2. **Key–Child Correlation** – d-node has $d - 1$ keys in sorted order.
  3. **Interleaved Ordering** – Keys in subtrees follow in-between ordering.
* **(2, 4) Tree** – Special multi-way search tree:

  * Node Size Property – At most 4 children.
  * Depth Property – All external nodes at same depth.
* **Balanced** – No rotations needed.

---

Do you want me to also add **small visual mnemonics** in the markdown so you can quickly recall the structure of Skip Lists, AVL Trees, and (2,4) Trees during the exam? That could speed up your memorization.
