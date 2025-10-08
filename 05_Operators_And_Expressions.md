# ⚙️ Operators and Expressions in C++  
**سی پلس پلس میں آپریٹرز اور ایکسپریشنز**

---

## 📘 What Are Operators, Operands, Expressions, and Operations?

### 🔹 Operator  
| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Operator             | `+`, `-`, `*`, `=` | Symbol that performs an action | `a + b` |

**Urdu**:  
آپریٹرز خاص علامات ہوتی ہیں جو ویری ایبلز اور ویلیوز پر عمل انجام دیتی ہیں۔

---

### 🔹 Operand  
| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Operand              | `a`, `b`, `5`, `3` | Value or variable used in operation | `a + b` → `a`, `b` are operands |

**Urdu**:  
آپریینڈز وہ ویلیوز یا ویری ایبلز ہیں جن پر آپریٹر عمل کرتا ہے۔

---

### 🔹 Expression  
| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Expression           | `a + b`, `x = 10` | Combination of operands and operators that produces a result | `int sum = a + b;` |

**Urdu**:  
ایکسپریشنز ویری ایبلز، ویلیوز اور آپریٹرز کا مجموعہ ہوتی ہیں جو کوئی نتیجہ دیتی ہیں۔

---

### 🔹 Operation  
| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Operation            | `a + b` | Action performed by operator on operands | `int sum = a + b;` → result is 8 |

**Urdu**:  
آپریشن وہ عمل ہے جو آپریٹر اپنے آپریینڈز پر انجام دیتا ہے۔

---

## ➕ Arithmetic Operators  
| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Addition             | `+`    | Adds two values     | `a + b` |
| Subtraction          | `-`    | Subtracts second from first | `a - b` |
| Multiplication       | `*`    | Multiplies two values | `a * b` |
| Division             | `/`    | Divides first by second | `a / b` |
| Modulus              | `%`    | Returns remainder   | `a % b` |

---

## 📝 Assignment Operator  
| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Assignment           | `=`    | Assigns value to variable | `x = 10;` |

---

## 🔁 Increment / Decrement Operators  
| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Increment            | `++`   | Increases value by 1 | `x++`, `++x` |
| Decrement            | `--`   | Decreases value by 1 | `x--`, `--x` |

> `x++` → post-increment  
> `++x` → pre-increment

---

## 🔍 Relational Operators  
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
| Programming Construct | Syntax | Semantic (Meaning) | Example |
|----------------------|--------|---------------------|---------|
| Logical AND          | `&&`   | True if both conditions are true | `a && b` |
| Logical OR           | `||`   | True if at least one is true | `a || b` |
| Logical NOT          | `!`    | Reverses the condition | `!a` |

---

## 🧠 Operator Precedence  
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
```cpp
// The preprocessor processes `#include <iostream>`
// It includes the iostream header file, which declares stream objects like cout, cin, cerr.
```

---

### 6. 🧩 Compiler  
- Translates source code to object code  
- Checks syntax and type rules

---

### 7. 🔗 Linker  
- Links object code with standard libraries  
- Resolves references like `cout`, `endl`

---

### 8. 🚚 Loader  
- Loads executable into memory  
- Prepares runtime environment

---

### 9. ▶️ Execution  
- Program starts at `main()`  
- Variables initialized  
- Operations performed  
- Output displayed:

```
Total Marks: 185
Average Marks: 61.6667
Passed: 1
```

> `Passed: 1` means `true`. If failed, it would show `0`.

---
