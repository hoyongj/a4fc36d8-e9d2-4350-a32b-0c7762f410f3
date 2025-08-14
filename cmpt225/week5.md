
# 📚 CMPT 225 – Week 5 Key Definitions

## 1. **Queue**

* **Queue (ADT)** – Collection of elements with **First-In, First-Out (FIFO)** order.
* **Core Operations**:

  * **enqueue(x)** – Add element to rear.
  * **dequeue()** – Remove element from front.
  * **front()** – Return front element without removing.
  * **isEmpty()** – Check if queue has no elements.
  * **size()** – Number of elements.
* **Linked List Queue**:

  * Front = head, Rear = tail.
  * Both enqueue and dequeue in $O(1)$ with tail pointer.

---

## 2. **Deque (Double-Ended Queue)**

* Pronounced “deck”.
* Allows insertion/removal at both ends.
* **Core Operations**:

  * `addFirst(x)` – Insert at head.
  * `addLast(x)` – Insert at tail.
  * `removeFirst()` – Remove from head.
  * `removeLast()` – Remove from tail.
  * `getFirst()` – Peek at head.
  * `getLast()` – Peek at tail.
  * `size()` – Number of elements.
  * `isEmpty()` – True if empty.
* **Implementation**: Typically a **doubly linked list**; O(1) for both ends.

---

## 3. **Adapter Pattern**

* **Definition**: Structural design pattern that converts one interface into another expected by clients.
* **How It Works**:

  * Wrap an existing class inside another.
  * Provide the expected interface while internally using the original.
* **Example**: Implementing `Stack` using a `Deque` (DequeStack).

---

## 4. **Vector (Array List)**

* **Vector (ADT)** – Extends array with dynamic resizing.
* **Core Operations**:

  * `get(i)` – Access element at index i.
  * `set(i, x)` – Replace element at index i.
  * `insert(i, x)` – Insert at index i (O(n) worst-case).
  * `erase(i)` – Remove at index i (O(n) worst-case).
* **Array-Based Implementation**:

  * Store elements in contiguous array.
  * Track number of stored elements.
* **Performance**:

  * End insertion/removal: O(1) amortized with doubling strategy.
  * Front insertion/removal: O(n).

---

## 5. **Dynamic Array Resizing Strategies**

* **Incremental**: Increase capacity by a constant $c$ – inefficient for large n.
* **Doubling**: Double capacity when full – amortized O(1) per push\_back.
* **Amortized Analysis**:

  * Look at average time over many operations.
  * Doubling strategy leads to $O(1)$ amortized insertion at end.

---

## 6. **Containers and Iterators**

* **Container**: Data structure supporting element access via iterators.
* **Iterator**: Object that abstracts traversal through a container.
* **Iterator Operations**:

  * `*p` – Access current element.
  * `++p` – Move to next.
  * `--p` – Move to previous (bidirectional).
* **Types**:

  * **iterator** – Read/write access.
  * **const\_iterator** – Read-only.
  * **bidirectional iterator** – Can move both ways.
  * **random-access iterator** – Supports jumps (p + i).
* **STL Examples**: `vector`, `deque`, `list`.

