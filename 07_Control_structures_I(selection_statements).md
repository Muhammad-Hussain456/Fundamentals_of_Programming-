## 🧭 Control Structures I: Selection Statements

Selection statements allow your program to **choose different paths** based on conditions. These are essential for implementing logic and making decisions.

---

## 🔍 Logical Expressions

Logical expressions evaluate to either **true (1)** or **false (0)** and are used in selection statements.

**Examples:**
```cpp
a > b        // true if a is greater than b
x == 10      // true if x equals 10
(x >= 50) && (y >= 50)  // true if both x and y are ≥ 50
```

---

## 🧠 if Statement

Executes a block of code **only if** the condition is true.

```cpp
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

## 🔁 if-else Statement

Executes one block if the condition is true, another if false.

```cpp
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

## 🧩 Nested if Statement

An `if` inside another `if`. Used for **multi-level decisions**.

```cpp
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

## 🔀 switch Statement

Used for **multi-way branching** based on a single variable.

```cpp
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
