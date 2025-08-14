
# 📚 CMPT 225 – Week 8 Key Definitions

## **Priority Queue**

* Abstract data type that stores elements with associated priorities.
* Operations:

  * **Insert** – Add element with a priority.
  * **RemoveMin / RemoveMax** – Remove element with highest or lowest priority.
  * **Min / Max** – Access element with highest or lowest priority without removing it.

---

## **Heap**

* **Heap** – Key-based data structure storing keys as a complete binary tree.
* **Max Heap** – Each child’s key ≤ parent’s key.
* **Min Heap** – Each child’s key ≥ parent’s key.
* **Complete Tree** – All levels full except possibly the last, filled left-to-right.

**Heap Operations (Min Heap example)**:

* **Insert**: Add at next available spot, swap up until heap property is restored.
* **RemoveMin**: Replace root with last node, remove last node, swap down until heap property is restored.
* **Complexity**:

  * Insert – $O(\log n)$
  * RemoveMin – $O(\log n)$
  * Min – $O(1)$

---

## **Map ADT**

* **Map** – Stores unique key–value pairs (entries).
* **Operations**:

  * **get(k)** – Retrieve value by key.
  * **put(k, v)** – Insert or replace value for key.
  * **remove(k)** – Remove entry by key.
  * **keySet()** – Return collection of all keys.
  * **values()** – Return collection of all values.
  * **entrySet()** – Return collection of all entries.

---

## **Hash Table**

* **Hash Table** – Map implementation with expected $O(1)$ access using:

  * **Bucket array** – Array of slots ("buckets") to store entries.
  * **Hash function** – Maps keys to bucket indices.
* **Hash function steps**:

  1. Compute hash code (integer, possibly negative).
  2. Apply **compression function** to map hash code to \[0, N−1].

**Compression Functions**:

* **Division method**: $h(k) = k \bmod N$ (N prime recommended).
* **MAD method**: $h(k) = (a k + b) \bmod N$ (a, b chosen to avoid collisions).

---

## **Collisions**

* **Collision** – Different keys mapping to the same bucket.
* **Collision Handling**:

  * **Separate Chaining** – Store multiple entries in the same bucket (e.g., linked list or map).
  * **Open Addressing** – Find another bucket:

    * **Linear probing** – Check next slots sequentially.
    * **Quadratic probing** – Use squared increments.
    * **Double hashing** – Use second hash function to determine step size.

---

## **Load Factor & Rehashing**

* **Load factor (λ)** = $n / N$ (entries / buckets).
* High load factor → increased collisions → **rehashing** (increase N, rebuild table).

---

## **C++ Map Implementations**

* **`std::map`** – Ordered map using self-balancing BST (O(log n) operations).
* **`std::unordered_map`** – Hash table implementation (O(1) expected operations), uses separate chaining.

