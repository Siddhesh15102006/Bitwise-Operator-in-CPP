# 🧪 Experiment 4 :- Bitwise Operators in C++

---

## ✅ Q1: Set and Reset a Bit

---

### 🎯 Aim:

To write a C++ program to **set** and **reset** (clear) a specific bit in a given integer using **bitwise operators**.

---

### 📚 Theory:

Bitwise operators allow direct manipulation of individual bits within an integer.

* **Setting a bit** means changing a specific bit to 1.
* **Resetting a bit** means changing a specific bit to 0.

### Bitwise Concepts Used:

* `|` (OR) → Used to **set** a bit.
* `&` (AND) with bitwise **NOT** `~` → Used to **reset** a bit.

### Formulae:

* **Set bit at position `n`:**

  ```cpp
  result = num | (1 << n);
  ```
* **Reset bit at position `n`:**

  ```cpp
  result = num & ~(1 << n);
  ```

---

### 🧠 Logic:

1. Accept an integer `num` and a bit position `n` (0-indexed).
2. To **set** the bit at position `n`, use: `num | (1 << n)`
3. To **reset** the bit at position `n`, use: `num & ~(1 << n)`
4. Display both results.

---

### 💡 Syntax:

```cpp
num | (1 << n);      // Set bit
num & ~(1 << n);     // Reset bit
```

---

### 🧾 Code:

```cpp
// Q1: Set and Reset Bit in C++
#include <iostream>
using namespace std;

int main() {
    int num, pos;

    cout << "Enter an integer: ";
    cin >> num;

    cout << "Enter bit position to modify (0-indexed): ";
    cin >> pos;

    int setBit = num | (1 << pos);         // Set bit
    int resetBit = num & ~(1 << pos);      // Reset bit

    cout << "Original number: " << num << endl;
    cout << "After setting bit " << pos << ": " << setBit << endl;
    cout << "After resetting bit " << pos << ": " << resetBit << endl;

    return 0;
}
```

---

### ✅ Sample Output:

```
Enter an integer: 10
Enter bit position to modify (0-indexed): 1
Original number: 10
After setting bit 1: 10
After resetting bit 1: 8
```

---

### 📌 Conclusion:

This program demonstrates how to manipulate individual bits using **bitwise shift** and **logical operators** in C++. Setting and resetting bits is essential in embedded systems, low-level programming, and optimization techniques.

---

## ✅ Q2: Demonstration of Bitwise Operators

---

### 🎯 Aim:

To write a C++ program demonstrating the use of **bitwise operators**:
`AND (&)`, `OR (|)`, `XOR (^)`, `NOT (~)`, `Left Shift (<<)`, and `Right Shift (>>)`.

---

### 📚 Theory:

Bitwise operators perform operations on the binary representations of integers.

| Operator | Description          | Example (a = 5, b = 3) |   |       |
| -------- | -------------------- | ---------------------- | - | ----- |
| `&`      | AND                  | 5 & 3 = 1              |   |       |
| \`       | \`                   | OR                     | 5 | 3 = 7 |
| `^`      | XOR                  | 5 ^ 3 = 6              |   |       |
| `~`      | NOT (1's complement) | \~5 = -6               |   |       |
| `<<`     | Left Shift           | 5 << 1 = 10            |   |       |
| `>>`     | Right Shift          | 5 >> 1 = 2             |   |       |

---

### 🧠 Logic:

1. Accept two integers from the user.
2. Apply and display results of all bitwise operations.
3. Demonstrate left and right shift with one of the numbers.

---

### 💡 Syntax:

```cpp
a & b;      // AND
a | b;      // OR
a ^ b;      // XOR
~a;         // NOT
a << n;     // Left shift
a >> n;     // Right shift
```

---

### 🧾 Code:

```cpp
// Q2: Demonstrating Bitwise Operators in C++
#include <iostream>
using namespace std;

int main() {
    int a, b;

    cout << "Enter two integers: ";
    cin >> a >> b;

    cout << "Bitwise AND (a & b): " << (a & b) << endl;
    cout << "Bitwise OR (a | b): " << (a | b) << endl;
    cout << "Bitwise XOR (a ^ b): " << (a ^ b) << endl;
    cout << "Bitwise NOT (~a): " << (~a) << endl;
    cout << "Left Shift (a << 1): " << (a << 1) << endl;
    cout << "Right Shift (a >> 1): " << (a >> 1) << endl;

    return 0;
}
```

---

### ✅ Sample Output:

```
Enter two integers: 5 3
Bitwise AND (a & b): 1
Bitwise OR (a | b): 7
Bitwise XOR (a ^ b): 6
Bitwise NOT (~a): -6
Left Shift (a << 1): 10
Right Shift (a >> 1): 2
```

---

### 📌 Conclusion:

This program demonstrates all fundamental **bitwise operations** in C++. Bitwise manipulation is powerful in tasks involving flags, masks, and low-level device control. Understanding these operators is crucial for performance optimization in system-level programming.

---
