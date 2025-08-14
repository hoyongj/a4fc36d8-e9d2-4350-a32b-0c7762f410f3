
# 📚 CMPT 225 – Week 1 Key Definitions

## 1. Data Structures

* **Data Structure**: A way in which data is stored for efficient search and retrieval (Encyclopaedia Britannica).

* Examples: **Stacks**, **Trees**, **Hash Maps**, **Arrays**.

* **Array**:
  A collection of elements of the same type, stored contiguously in memory, accessed by index.

  * Size is fixed at creation.
  * Random access: O(1) element access.

## 2. Algorithms

* **Algorithm**: A specific procedure for solving a well-defined computational problem (Encyclopaedia Britannica).
* Example: **Merge Sort** – A divide-and-conquer sorting method that splits, sorts, and recombines data.

## 3. C++ Basics

### 3.1 Fundamental Types

| Type     | Description                     |
| -------- | ------------------------------- |
| `bool`   | Boolean value (true/false)      |
| `char`   | Character                       |
| `short`  | Short integer                   |
| `int`    | Integer                         |
| `long`   | Long integer                    |
| `float`  | Single-precision floating-point |
| `double` | Double-precision floating-point |

### 3.2 Pointers

* A variable that holds the **address** of a piece of memory.
* Dereferencing (`*p`) accesses the value stored at that address.

### 3.3 Memory Management

* **malloc()** (C): Allocates raw memory; must use `free()` to release.
* **new** (C++): Allocates memory for an object/array; use `delete`/`delete[]` to free.
* **Memory Leak**: Allocated memory without deallocation.
* **Dangling Pointer**: Pointer referencing deallocated memory.

### 3.4 Arrays

* **Static Array**: Size fixed at creation.
* **Dynamic Array**: Allocated with `new`, can be released with `delete[]`.

### 3.5 C-Strings & `std::string`

* **C-String**: Null-terminated array of characters.
* **`std::string`**: Class providing string manipulation in C++ STL.

### 3.6 Scope

* **Local Scope**: Variables accessible only within their block.
* **Global Scope**: Variables accessible throughout the program.

### 3.7 Namespaces

* Logical grouping of names to prevent naming conflicts.
* Example: `std::cout` from namespace `std`.

## 4. Operators

### Arithmetic

`+`, `-`, `*`, `/`, `%`

### Increment/Decrement

`++i`, `i++`, `--i`, `i--`

### Relational

`<`, `>`, `<=`, `>=`, `==`, `!=`

### Logical

`!`, `&&`, `||`

### Bitwise

`~`, `&`, `|`, `^`, `<<`, `>>`

### Assignment

`=`, `+=`, `-=`, `*=`, `/=`, `%=` and bitwise equivalents.

## 5. Control Flow

* **If / Else If / Else**
* **Switch**
* **While Loop**
* **Do-While Loop**
* **For Loop**
* **Break** & **Continue**

## 6. Functions

* **Declaration**: States function name, parameters, and return type.
* **Definition**: Provides the body/implementation.
* **Pass by Reference**: Function arguments passed as references (`&`), allowing modification.
* **Function Overloading**: Multiple functions with the same name but different parameter lists.

## 7. Structures & Classes

* **C-Style Struct**: Aggregates related variables into one type.
* **Class**: Encapsulation of data (member variables) and methods (member functions).

  * **Public**: Accessible from outside the class.
  * **Private**: Accessible only from within the class.

