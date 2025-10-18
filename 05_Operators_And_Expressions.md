# ⚙️ Operators and Expressions in C++

---

## 📘 What Are Operators, Operands, Expressions, and Operations?

### 🔹 Operator  
  
Operators are special symbols that perform actions on variables and values.

| Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Operator             | `+`, `-`, `*`, `=` | Symbol that performs an action | `a - b`,`2 + 4`, `c / 5`, `b = 6`, `etc`. Here,  `-`, `+`, `/`, `=` are operators.  |

---

### 🔹 Operand  
 
Operands are the values or variables on which operators act.

| Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Operand              | `a`, `b`, `5`, `3` | Value or variable used in operation | `a + b`,`2 + 4`, `c / 5`, `b = 6`, `etc`. Here,  `a`, `b`, `2`, `4`,`c`, `5`, `6`, are operands |

---



### 🔹 Expression  

An expression is a combination of operands and operators that produces a result.

| Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Expression           | `a + b`, `x = 10` | Complete construct that evaluates to a value | `a + b`, sum = a + b`, `2 + 4`,  `mul = 4 * 2`, `answer = true`, `etc` are expressions. |

---

### 🧩 Statement

A **statement** is a complete instruction that tells the computer to **perform an action**.  
Each statement in C++ ends with a **semicolon (;)**.

**Examples:**
- `int a;` → Declaration statement (creates a variable)  
- `a = 5;` → Assignment statement (stores a value)  
- `cout << a;` → Output statement (displays a value)  
- `if (a > 0) cout << "Positive";` → Conditional statement (controls program flow)  
- `for (int i = 0; i < 5; i++) cout << i;` → Loop statement (repeats actions)  
- `return 0;` → Return statement (ends a function and returns a value)  
- etc.

---

### 🧩 Is `a = 5` an Expression?

✅ Yes — `a = 5` is an **expression**,  
because it **produces a value** (the value assigned to `a`, which is `5`).

But when you add a **semicolon** → `a = 5;`  
it becomes an **assignment statement**,  
because now it **performs an action** (assigns 5 to `a`)

🧠 **Summary:**
- `a = 5` → **Expression** (produces value 5)  
- `a = 5;` → **Statement** (executes the assignment)
---


### 🔹 Operation

An **operation** is the action performed by an **operator** on **operands**, or by an entire **expression** or **statement** to produce a result.

It can occur within an **expression** or a **statement**, and multiple operations may happen in a single line of code.

| Construct | Syntax | Semantic (Meaning) | Example |
|------------|---------|--------------------|----------|
| Operation | expression / statement | The action performed by an operator on operands, or by an entire expression or statement. | `int sum = a + b;` → <br>• `+` operator performs an addition operation between operands `a` and `b`. <br>• The expression `a + b` performs an addition operation. <br>• The expression `sum = a + b` performs addition and assignment operations. <br>• The statement `int sum = a + b;` performs three operations: declaration, addition, and initialization. |

---


## ➕ Arithmetic Operators  
  
Used for basic mathematical operations.

| Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Addition             | `+`    | Adds two values     | `a + b` |
| Subtraction          | `-`    | Subtracts second from first | `a - b` |
| Multiplication       | `*`    | Multiplies two values | `a * b` |
| Division             | `/`    | Divides first by second | `a / b` |
| Modulus              | `%`    | Returns remainder   | `a % b` |

---

## 📝 Assignment Operator  
 
Assigns a value to a variable.

| Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Assignment           | `=`    | Assigns value to variable | `x = 10;` |

---

## 🔁 Increment / Decrement Operators  
 
Used to increase or decrease a value by 1.

| Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Increment            | `++`   | Increases value by 1 | `x++`, `++x` |
| Decrement            | `--`   | Decreases value by 1 | `x--`, `--x` |

> `x++` → post-increment  
> `++x` → pre-increment

---

## 🔍 Relational Operators  

Used to compare two values.

| Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Equal to             | `==`   | Checks if values are equal | `a == b` |
| Not equal to         | `!=`   | Checks if values are not equal | `a != b` |
| Greater than         | `>`    | Checks if first is greater | `a > b` |
| Less than            | `<`    | Checks if first is less | `a < b` |
| Greater or equal     | `>=`   | Checks if first ≥ second | `a >= b` |
| Less or equal        | `<=`   | Checks if first ≤ second | `a <= b` |

---

## 🔐 Logical Operators  

Used to combine multiple conditions.

| Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Logical AND          | `&&`   | True if both conditions are true | `a && b` |
| Logical OR           | `||`   | True if at least one is true | `a || b` |
| Logical NOT          | `!`    | Reverses the condition | `!a` |

---

## 🧠 Operator Precedence  
  
Defines the order in which operators are evaluated.

| Precedence Level | Syntax | Semantic (Meaning) | Example |
|------------------|--------|---------------------|---------|
| 1 (Highest)      | `++`, `--`, `!` | Unary operations | `++x`, `!flag` |
| 2                | `*`, `/`, `%`   | Multiplication, division, modulus | `a * b`, `a / b` |
| 3                | `+`, `-`         | Addition, subtraction | `a + b`, `a - b` |
| 4                | `<`, `>`, `<=`, `>=` | Relational comparisons | `a < b`, `a >= b` |
| 5                | `==`, `!=`       | Equality checks | `a == b`, `a != b` |
| 6                | `&&`             | Logical AND | `a && b` |
| 7                | `||`             | Logical OR | `a || b` |
| 8 (Lowest)       | `=`              | Assignment | `x = 10` |

> Higher precedence operators are evaluated first.  
> Equal precedence is resolved **left to right**, except assignment (`=`), which is **right to left**.

---

## 🧩 Example Problem

Create variables for student marks, height, grade, and pass status. Assign values and display them.

---

## 🧠 Step-by-Step Solution

### 1. ✅ Problem Definition  
Calculate total and average marks using arithmetic operators, and check pass status using relational and logical operators.

---

### 2. 🔍 Problem Analysis  
- Declare three `int` variables for marks.  
- Use `+` and `/` for total and average.  
- Use `>=` and `&&` to check pass condition.  
- Display results using `cout`.

---

### 3. 🧮 Design Algorithm  
1. Start program  
2. Declare `mark1`, `mark2`, `mark3`  
3. Calculate `total = mark1 + mark2 + mark3`  
4. Calculate `average = total / 3.0`  
5. Check if average ≥ 50 and all marks ≥ 40  
6. Display results  
7. End program

---

### 4. 💻 Coding
```cpp
#include <iostream>
using namespace std;

int main() {
    int mark1 = 60;
    int mark2 = 70;
    int mark3 = 55;

    int total = mark1 + mark2 + mark3;
    float average = total / 3.0;

bool passed = (average >= 50) && (mark1 >= 40) && (mark2 >= 40) && (mark3 >= 40);

    cout << "Total Marks: " << total << endl;
    cout << "Average Marks: " << average << endl;
    cout << "Passed: " << passed << endl;

    return 0;
}
```

---

### 5. ⚙️ Preprocessor  
**Definition**:  
The preprocessor runs before compilation and handles directives like `#include`.

```cpp
// The preprocessor processes `#include <iostream>`
// It includes the iostream header file, which declares stream objects like cout, cin, cerr.
```

---

### 6. 🧩 Compiler  
**Definition**:  
Translates source code into object code and checks for syntax errors.

---

### 7. 🔗 Linker  
**Definition**:  
Links object code with standard libraries and resolves external references.

---

### 8. 🚚 Loader  
**Definition**:  
Loads the executable into memory and prepares it for execution.

---

### 9. ▶️ Execution  
**Definition**:  
Runs the program starting from `main()`, performs operations, and displays output.

```
Total Marks: 185
Average Marks: 61.6667
Passed: 1
```

> `Passed: 1` means `true`. If failed, it would show `0`.

---
