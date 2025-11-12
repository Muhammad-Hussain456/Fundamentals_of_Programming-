
# 🧭 Control Structures I (C++)

---

## 🔍 Expressions in C++

An **expression** is any valid combination of operands and operators that evaluates to a value.

### ✅ Types of Expressions

| 🧩 Type        | ✅ Syntax           | 📘 Semantic Meaning                                      | 💡 Example          |
|----------------|----------------------------------|----------------------------------------------------------|----------------------------------------|
| **Arithmetic** | `operand1 operator operand2`     | Performs mathematical operations                         | `a + b` → adds `a` and `b`             |
| **Relational** | `operand1 operator operand2`     | Compares values and returns `true` or `false`            | `score > 50` → `true` if score above 50 |
| **Logical**    | `condition1 operator condition2` | Combines Boolean results                                 | `(x > 5) && (y < 10)` → `true` if both true |
| **Assignment** | `variable = value`               | Assigns a value to a variable                            | `x = 10` → assigns `10` to `x`         |
| **Unary**      | `!condition`                     | Operates on a single operand                             | `!flag` → negates `flag`               |
| **Compound**   | `variable operator= value`       | Combines arithmetic and assignment                       | `x += 5` → adds `5` to `x`             |

---

## 🧾 Statements in C++

A **statement** is a complete instruction that performs an action.  
It may contain expressions.

### ✅ Types of Statements

| 🧩 Type           | ✅ Syntax              | 📘 Semantic Meaning                                 | 💡 Example         |
|-------------------|----------------------------------|----------------------------------------------------|---------------------------------------|
| **Expression**    | `expression;`                    | Evaluates an expression                            | `x = 5;` assigns 5 to x               |
| **Declaration**   | `type variable;`                 | Declares a variable                                | `int score;` creates variable score    |
| **Compound**      | `{ statement1; statement2; }`    | Groups multiple statements                         | `{ int x=5; cout<<x; }` prints 5      |
| **Selection**     | `if`, `if-else`, `switch`        | Chooses between paths based on conditions          | `if (x>0) cout<<x;` prints x if positive |
| **Iteration**     | `for`, `while`, `do-while`       | Repeats actions based on conditions                | `while (x<10) x++;` loops till x = 10 |
| **Jump**          | `break`, `continue`, `return`    | Alters control flow directly                       | `return 0;` exits function             |

---

## 🎯 Selection Statements

Selection statements allow programs to **make decisions** based on conditions.

---

### 🧠 `if` Statement

#### ✅ Syntax
```cpp
if (condition) {
    // code if condition is true
}

📘 Semantic

Executes block only if condition is true.

💡 Example

int score = 75;
if (score >= 50) {
    cout << "Passed";
}
// Output: Passed


---

🔁 if-else Statement

✅ Syntax

if (condition) {
    // true block
} else {
    // false block
}

📘 Semantic

Executes one block if true, another if false.

💡 Example

int score = 45;
if (score >= 50) {
    cout << "Passed";
} else {
    cout << "Failed";
}
// Output: Failed


---

🧩 Nested if Statement

✅ Syntax

if (condition1) {
    if (condition2) {
        // code if both are true
    }
}

📘 Semantic

Used for multi-level decision-making.

💡 Example

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
// Output: Grade: A


---

🔀 switch Statement

✅ Syntax

switch (expression) {
    case value1:
        // code
        break;
    case value2:
        // code
        break;
    default:
        // code if no match
}

📘 Semantic

Executes one of many possible blocks based on the value of the expression.

💡 Example

char grade = 'B';
switch (grade) {
    case 'A': cout << "Excellent"; break;
    case 'B': cout << "Good"; break;
    case 'C': cout << "Fair"; break;
    case 'F': cout << "Fail"; break;
    default: cout << "Invalid grade";
}
// Output: Good


---
