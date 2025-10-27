## 🧭 Control Structures I: Selection Statements (C++)

Selection statements in C++ allow your program to **make decisions** based on conditions.

---

## 🔍 Logical Expressions

Logical expressions return either **true (1)** or **false (0)** and are used in decision-making.

**Examples:**
```cpp
a > b              // true if a is greater than b
x == 10            // true if x equals 10
(x >= 50) && (y >= 50)  // true if both x and y are ≥ 50
```

---

## 🔍 Logical Expressions – Syntax, Semantics, and Examples

| 🔣 Syntax                          | 📘 Semantic/Meaning                                      | 💡 Example                            |
|-----------------------------------|----------------------------------------------------------|---------------------------------------|
| `operand1 == operand2`            | Checks if both operands are equal                        | `5 == 5` → `true`                     |
| `operand1 != operand2`            | Checks if operands are not equal                         | `5 != 3` → `true`                     |
| `operand1 > operand2`             | Checks if left operand is greater than right             | `7 > 4` → `true`                      |
| `operand1 < operand2`             | Checks if left operand is less than right                | `3 < 9` → `true`                      |
| `operand1 >= operand2`            | Checks if left operand is greater than or equal to right | `6 >= 6` → `true`                     |
| `operand1 <= operand2`            | Checks if left operand is less than or equal to right    | `2 <= 5` → `true`                     |
| `(condition1) && (condition2)`    | True if **both** conditions are true                     | `(5 > 3) && (2 < 4)` → `true`         |
| `condition1 \|\| condition2`    | True if **at least one** condition is true               | `(5 > 3) \|\| (2 > 4)` → `true`         |
| `!(condition)`                    | True if the condition is **false**                       | `!(5 == 3)` → `true`                  |

---

## 🧠 `if` Statement

**Semantic:**  
Executes a block of code **only if** the condition is true.

```cpp
// Syntax:
if (condition) {
    // code to execute if condition is true
}
```

**Example:**
```cpp
int score = 75;
if (score >= 50) {
    cout << "Passed";
}
```

---

## 🔁 `if-else` Statement

**Semantic:**  
Executes one block if the condition is true, another if false.

```cpp
// Syntax:
if (condition) {
    // true block
} else {
    // false block
}
```

**Example:**
```cpp
int score = 45;
if (score >= 50) {
    cout << "Passed";
} else {
    cout << "Failed";
}
```

---

## 🧩 Nested `if` Statement

**Semantic:**  
An `if` inside another `if`. Used for **multi-level decisions**.

```cpp
// Syntax:
if (condition1) {
    if (condition2) {
        // code if both conditions are true
    }
}
```

**Example:**
```cpp
int score = 85;
if (score >= 50) {
    if (score >= 80) {
        cout << "Grade: A";
    } else {
        cout << "Grade: B";
    }
} else {
    cout << "Failed";
}
```

---

## 🔀 `switch` Statement

**Semantic:**  
Used for **multi-way branching** based on a single variable.

```cpp
// Syntax:
switch (expression) {
    case value1:
        // code for value1
        break;
    case value2:
        // code for value2
        break;
    default:
        // code if no case matches
}
```

**Example:**
```cpp
char grade = 'B';
switch (grade) {
    case 'A':
        cout << "Excellent";
        break;
    case 'B':
        cout << "Good";
        break;
    case 'C':
        cout << "Fair";
        break;
    case 'F':
        cout << "Fail";
        break;
    default:
        cout << "Invalid grade";
}
```
---

## 🧪 Example Problem: Grade Evaluation

### ✅ Problem:
Evaluate a student's grade and display a message using `if-else` and `switch`.

### 💻 Code:
```cpp
#include <iostream>
using namespace std;

int main() {
    int marks = 78;
    char grade;

    if (marks >= 80)
        grade = 'A';
    else if (marks >= 70)
        grade = 'B';
    else if (marks >= 60)
        grade = 'C';
    else
        grade = 'F';

    switch (grade) {
        case 'A': cout << "Excellent"; break;
        case 'B': cout << "Good"; break;
        case 'C': cout << "Fair"; break;
        case 'F': cout << "Fail"; break;
        default: cout << "Invalid grade";
    }

    return 0;
}
```
---
