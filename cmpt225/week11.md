
# CMPT 225 – Week 11: Definition Summary

## **General Concepts**

* **Sorting Algorithm** – A method for arranging elements of a list or array in a specific order (e.g., ascending or descending).
* **In-place Algorithm** – Performs sorting without requiring additional significant memory beyond the input array.
* **Stable Sort** – Preserves the relative order of elements with equal keys.
* **Time Complexity** – Describes how the runtime of an algorithm grows with input size.
* **Worst Case** – Maximum time an algorithm could take.
* **Average Case** – Expected time over random input.

---

## **Divide-and-Conquer**

* **Divide-and-Conquer Algorithm** – A design pattern involving:

  1. **Divide**: Break the problem into smaller subproblems.
  2. **Recur**: Solve subproblems recursively.
  3. **Conquer**: Combine solutions to form the final result.

---

## **Sorting Algorithms**

### **Insertion Sort**

* **Definition** – Sorts by building the final sorted array one element at a time, inserting each new element into its correct position.
* **Properties** – In-place, stable, O(n²) average & worst-case.

### **Merge Sort**

* **Definition** – A divide-and-conquer algorithm that splits the array into halves, sorts each half, and merges them.
* **Steps** – Divide, recursively sort, merge.
* **Complexity** – O(n log n) average & worst-case, stable, not in-place.

### **Quicksort**

* **Definition** – A divide-and-conquer algorithm that partitions the array around a pivot, recursively sorting each side.
* **Randomized Quicksort** – Picks pivot randomly to reduce worst-case probability.
* **Complexity** – O(n log n) average, O(n²) worst-case, in-place, unstable.

### **Heapsort**

* **Definition** – Builds a max-heap and repeatedly extracts the maximum element to build a sorted array.
* **Steps** – Heapify array, remove root n times.
* **Complexity** – O(n log n) average & worst-case, in-place, unstable.

---

## **Lower Bound for Comparison Sorting**

* **Comparison Sorting** – Sorting using only element comparisons (e.g., `<` operator).
* **Lower Bound** – Any comparison-based sorting requires Ω(n log n) comparisons in the worst case (decision tree argument).

---

## **Non-Comparison-Based Sorting**

### **Bucket Sort**

* **Definition** – Distributes elements into buckets based on their keys, then concatenates buckets in order.
* **Complexity** – O(n + N) time, O(n + N) space, stable if buckets use queues.

### **Radix Sort**

* **Definition** – Sorts keys with multiple digits by applying a stable sort (e.g., bucket sort) on each digit, from least significant to most significant (LSD) or vice versa.
* **Complexity** – O(dn), where d is number of digits.

