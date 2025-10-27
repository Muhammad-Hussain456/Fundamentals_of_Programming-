## 🧭 Control Structures I(C++):

---

## 🔍 Expressions in C++

An **expression** is any valid combination of operands and operators that evaluates to a value.

### ✅ Types of Expressions

| 🧩 Type            | ✅ Syntax                          | 📘 Semantic Meaning                                      | 💡 Example                      |
|--------------------|------------------------------------|----------------------------------------------------------|---------------------------------|
| Arithmetic         | `operand1 + operand2`              | Performs math operations                                 | `a + b` → adds `a` and `b`      |
| Relational         | `operand1 > operand2`              | Compares values, returns `true` or `false`               | `score > 50` → `true` if score is above 50 |
| Logical            | `condition1 && condition2`         | Combines Compares values, or Boolean results and returns `true` or `false`                 | `(x > 5) && (y < 10)` → `true` if both are true |
| Assignment         | `variable = value`                 | Assigns a value to a variable                            | `x = 10` → assigns 10 to `x`    |
| Unary              | `!condition`                       | Operates on a single operand                             | `!flag` → negates `flag`        |
| Compound           | `variable += value`                | Combines arithmetic and assignment                       | `x += 5` → adds 5 to `x`         |

---

## 🧾 Statements in C++

A **statement** is a complete instruction that performs an action. It may contain expressions.

### ✅ Types of Statements

| 🧩 Type                  | ✅ Syntax Example                  | 📘 Semantic Meaning                                      | 💡 Example                      |
|--------------------------|------------------------------------|----------------------------------------------------------|---------------------------------|
| Expression Statement     | `expression;`                      | Evaluates an expression and ends with `;`                | `x = 5;`                        |
| Declaration Statement    | `type variable;`                   | Declares a variable                                      | `int score;`                   |
| Compound Statement       | `{ statement1; statement2; }`      | Groups multiple statements                               | `{ int x = 5; cout << x; }`    |
| Selection Statement      | `if`, `if-else`, `switch`          | Chooses between paths based on conditions                | `if (x > 0) cout << x;`        |
| Iteration Statement      | `for`, `while`, `do-while`         | Repeats actions based on conditions                      | `while (x < 10) x++;`          |
| Jump Statement           | `break`, `continue`, `return`      | Alters control flow directly                             | `return 0;`                    |

---

### Selection Statement
Selection statements in C++ allow your program to **make decisions** based on conditions.

### 🧠 `if` Statement

#### ✅ Syntax
```cpp
if (condition) {
    // code to execute if condition is true
}
```

#### 📘 Semantic
Executes the block only if the condition evaluates to `true`.

#### 💡 Example
```cpp
int score = 75;
if (score >= 50) {
    cout << "Passed";
}
```

---

### 🔁 `if-else` Statement

#### ✅ Syntax
```cpp
if (condition) {
    // true block
} else {
    // false block
}
```

#### 📘 Semantic
Executes one block if the condition is true, another if false.

#### 💡 Example
```cpp
int score = 45;
if (score >= 50) {
    cout << "Passed";
} else {
    cout << "Failed";
}
```

---

### 🧩 Nested `if` Statement

#### ✅ Syntax
```cpp
if (condition1) {
    if (condition2) {
        // code if both conditions are true
    }
}
```

#### 📘 Semantic
Allows multi-level decision-making by nesting conditions.

#### 💡 Example
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

### 🔀 `switch` Statement

#### ✅ Syntax
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

#### 📘 Semantic
Selects one of many possible blocks to execute based on a single expression.

### 💡 Example
```cpp
char grade = 'B';
switch (grade) {
    case 'A': cout << "Excellent"; break;
    case 'B': cout << "Good"; break;
    case 'C': cout << "Fair"; break;
    case 'F': cout << "Fail"; break;
    default: cout << "Invalid grade";
}
```

---
