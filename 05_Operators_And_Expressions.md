# ⚙️ Operators and Expressions in C++

---

## 📘 What Are Operators, Operands, Expressions, and Operations?

### 🔹 Operator  
  
Operators are special symbols that perform actions on variables and values.

| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Operator             | `+`, `-`, `*`, `=` | Symbol that performs an action | `a - b`,`2 + 4`, `c / 5`, `b = 6`, `etc`. Here,  `-`, `+`, `/`, `=` are operators.  |

---

### 🔹 Operand  
 
Operands are the values or variables on which operators act.

| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Operand              | `a`, `b`, `5`, `3` | Value or variable used in operation | `a + b`,`2 + 4`, `c / 5`, `b = 6`, `etc`. Here,  `a`, `b`, `2`, `4`,`c`, `5`, `6`, are operands |

---

### 🔹 Operation  

An operation is the action performed by an operator on operands.

| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Operation            | `a + b` | Action performed by operator on operands | `int sum = a + b;`. Here, `a + b` , `sum = a + b` are operations.|

---


### 🔹 Expression  

An expression is a combination of operands and operators that produces a result.

| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Expression           | `a + b`, `x = 10` | Complete construct that evaluates to a value | `int sum = a + b;`, `float mul = 4 * 2`, `bool answer = true`, `etc` are expressions. |

---


## ➕ Arithmetic Operators  
  
Used for basic mathematical operations.

| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Addition             | `+`    | Adds two values     | `a + b` |
| Subtraction          | `-`    | Subtracts second from first | `a - b` |
| Multiplication       | `*`    | Multiplies two values | `a * b` |
| Division             | `/`    | Divides first by second | `a / b` |
| Modulus              | `%`    | Returns remainder   | `a % b` |

---

## 📝 Assignment Operator  
 
Assigns a value to a variable.

| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Assignment           | `=`    | Assigns value to variable | `x = 10;` |

---

## 🔁 Increment / Decrement Operators  
 
Used to increase or decrease a value by 1.

| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Increment            | `++`   | Increases value by 1 | `x++`, `++x` |
| Decrement            | `--`   | Decreases value by 1 | `x--`, `--x` |

> `x++` → post-increment  
> `++x` → pre-increment

---

## 🔍 Relational Operators  

Used to compare two values.

| Programming Construct | Syntax | Semantic (Meaning) | Example |
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

| Programming Construct | Syntax | Semantic (Meaning) | Example |
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
