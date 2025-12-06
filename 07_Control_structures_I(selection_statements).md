
# 🧭 Control Structures I (C++)

---

## 🔍 Expressions in C++

An **expression** is any valid combination of operands and operators that evaluates to a value.

### ✅ Types of Expressions — Where & When to Use

| 🧩 Type        | ✅ Syntax                 | 📘 Semantic                                      | 💡 Example                              | 🎯 Where & When Used |
|----------------|---------------------------|--------------------------------------------------|-----------------------------------------|----------------------|
| **Arithmetic** | `operand1 operator operand2` | Performs mathematical operations                 | `a + b` → adds `a` and `b`              | Used in calculations (marks, salary, totals, averages) |
| **Relational** | `operand1 operator operand2` | Compares values and returns `true` or `false`    | `score > 50` → `true` if score above 50 | Used in conditions (grading, eligibility, comparisons) |
| **Logical**    | `condition1 operator condition2` | Combines Boolean results                         | `(x > 5) && (y < 10)` → `true` if both true | Used in complex decisions (multiple rules, validations) |
| **Assignment** | `variable = value`           | Assigns a value to a variable                    | `x = 10` → assigns `10` to `x`          | Used to store/update values (initialization, updates) |
| **Unary**      | `!condition`                 | Operates on a single operand                     | `!flag` → negates `flag`                | Used in toggling states (true ↔ false, on ↔ off) |
| **Compound**   | `variable operator= value`   | Combines arithmetic and assignment               | `x += 5` → adds `5` to `x`              | Used in counters, accumulations, iterative updates |

---

## 🧾 Statements in C++

A **statement** is a complete instruction that performs an action.  
It may contain expressions.

### ✅ Types of Statements — Where & When to Use

| 🧩 Type           | ✅ Syntax                  | 📘 Semantic                                 | 💡 Example                                | 🎯 Where & When Used |
|-------------------|---------------------------|---------------------------------------------|-------------------------------------------|----------------------|
| **Expression**    | `expression;`             | Evaluates an expression                      | `x = 5;` assigns 5 to x                   | Used for assignments, function calls |
| **Declaration**   | `type variable;`          | Declares a variable                          | `int score;` creates variable `score`     | Used at start of program or block to define variables |
| **Compound**      | `{ statement1; statement2; }` | Groups multiple statements                  | `{ int x=5; cout<<x; }` prints 5          | Used in functions, loops, conditional blocks |
| **Selection**     | `if`, `if-else`, `switch` | Chooses between paths based on conditions    | `if (x>0) cout<<x;` prints x if positive  | Used for decision-making |
| **Iteration**     | `for`, `while`, `do-while` | Repeats actions based on conditions          | `while (x<10) x++;` loops till x = 10     | Used for repetition (tables, lists, arrays) |
| **Jump**          | `break`, `continue`, `return` | Alters control flow directly                | `return 0;` exits function                | Used to exit loops/functions or skip steps |

---

## 🎯 Selection Statements

Selection statements allow programs to **make decisions** based on conditions.

---

### 🧠 `if` Statement
- 📘 Semantic → Executes block only if condition evaluates to **true**.  
- 🎯 Where & When → Used for **single-condition checks** (e.g., pass/fail, positive/negative).

💡 Example
```cpp
int score = 75;
if (score >= 50) {
    cout << "Passed";
}
// Output: Passed
```

---

### 🔁 `if-else` Statement
- 📘 Semantic → Executes one block if condition is **true**, another if condition is **false**.  
- 🎯 Where & When → Used when there are **two possible outcomes** (e.g., pass/fail, even/odd).

💡 Example
```cpp
int score = 45;
if (score >= 50) {
    cout << "Passed";
} else {
    cout << "Failed";
}
// Output: Failed
```

---

### 🧩 Nested `if` Statement
- 📘 Semantic → Allows **multi-level decision-making** with more than two possible outcomes.  
- 🎯 Where & When → Used when decisions depend on **three or more conditions** (e.g., grade levels, ranges, categories).

💡 Example
```cpp
int score = 85;
if (score >= 80) {
    cout << "Grade: A";
} else if (score >= 60) {
    cout << "Grade: B";
} else if (score >= 40) {
    cout << "Grade: C";
} else {
    cout << "Fail";
}
// Output: Grade: A
```

---

### 🔀 `switch` Statement
- 📘 Semantic → Executes one of many possible blocks based on the **value of an expression**.  
- 🎯 Where & When → Used when there are **multiple discrete options** (e.g., menu choices, grades, days of week) and executes one of many possible blocks based on the **selected option**.  
  > Note: Works with integral types (`int`, `char`, `enum`) — not ranges.

💡 Example
```cpp
char grade = 'B';
switch (grade) {
    case 'A': cout << "Excellent"; break;
    case 'B': cout << "Good"; break;
    case 'C': cout << "Fair"; break;
    case 'F': cout << "Fail"; break;
    default: cout << "Invalid grade";
}
// Output: Good
```

---

## 📊 Quick Comparison

| Statement   | Handles | Best Used For |
|-------------|---------|---------------|
| **if**      | One condition → executes if true | Single checks (pass/fail, positive/negative) |
| **if-else** | Two outcomes → true OR false | Binary decisions (yes/no, pass/fail) |
| **nested if** | Three or more outcomes | Ranges, categories, multi-level grading |
| **switch**  | Multiple fixed options | Menus, enums, discrete values (days, grades) |

---

## ✨ Key Takeaway
- **`if`** → one condition.  
- **`if-else`** → two outcomes.  
- **`nested if`** → three or more outcomes.  
- **`switch`** → multiple fixed options.  

Together, they form the foundation of **decision-making and control flow in C++**.
```

---
