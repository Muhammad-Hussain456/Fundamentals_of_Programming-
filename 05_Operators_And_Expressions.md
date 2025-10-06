# ⚙️ Operators and Expressions in C++  
**سی پلس پلس میں آپریٹرز اور ایکسپریشن

## 🧮 What Are Operators?  
Operators are special symbols used to perform operations on variables and values.  
آپریٹرز خاص علامات ہوتی ہیں جو ویری ایبلز اور ویلیوز پر عمل انجام دیتی ہیں۔

Expressions are combinations of variables, values, and operators that produce a result.  
ایکسپریشنز ویری ایبلز، ویلیوز اور آپریٹرز کا مجموعہ ہوتی ہیں جو کوئی نتیجہ دیتی ہیں۔

---

## ➕ Arithmetic Operators  
Used for basic mathematical operations.  
بنیادی ریاضی کے عمل کے لیے استعمال ہوتے ہیں۔

| Operator | Syntax Example     | Semantic in C++                          |
|----------|--------------------|------------------------------------------|
| `+`      | `a + b`            | Adds two values                          |
| `-`      | `a - b`            | Subtracts second value from first        |
| `*`      | `a * b`            | Multiplies two values                    |
| `/`      | `a / b`            | Divides first value by second            |
| `%`      | `a % b`            | Returns remainder of division            |

---

## 📝 Assignment Operator  
Assigns a value to a variable.  
ویری ایبل کو ویلیو دینے کے لیے استعمال ہوتا ہے۔

| Operator | Syntax Example     | Semantic in C++                          |
|----------|--------------------|------------------------------------------|
| `=`      | `x = 10;`          | Assigns 10 to variable `x`               |

---

## 🔁 Increment / Decrement Operators  
Used to increase or decrease a value by 1.  
ویلیو کو 1 بڑھانے یا گھٹانے کے لیے استعمال ہوتے ہیں۔

| Operator | Syntax Example     | Semantic in C++                          |
|----------|--------------------|------------------------------------------|
| `++`     | `x++` or `++x`     | Increments value by 1                    |
| `--`     | `x--` or `--x`     | Decrements value by 1                    |

> `x++` is **post-increment** (value used first, then increased)  
> `++x` is **pre-increment** (value increased first, then used)

---

## 🔍 Relational Operators  
Used to compare two values.  
دو ویلیوز کا موازنہ کرنے کے لیے استعمال ہوتے ہیں۔

| Operator | Syntax Example     | Semantic in C++                          |
|----------|--------------------|------------------------------------------|
| `==`     | `a == b`           | Checks if values are equal               |
| `!=`     | `a != b`           | Checks if values are not equal           |
| `>`      | `a > b`            | Checks if first is greater than second   |
| `<`      | `a < b`            | Checks if first is less than second      |
| `>=`     | `a >= b`           | Checks if first is greater or equal      |
| `<=`     | `a <= b`           | Checks if first is less or equal         |

---

## 🔐 Logical Operators  
Used to combine multiple conditions.  
متعدد شرائط کو جوڑنے کے لیے استعمال ہوتے ہیں۔

| Operator | Syntax Example     | Semantic in C++                          |
|----------|--------------------|------------------------------------------|
| `&&`     | `a && b`           | Logical AND — true if both are true      |
| `||`     | `a || b`           | Logical OR — true if at least one is true|
| `!`      | `!a`               | Logical NOT — reverses the condition     |

---

## 🧠 Operator Precedence  
Defines the order in which operators are evaluated.  
یہ ترتیب بتاتی ہے کہ آپریٹرز کس ترتیب سے عمل میں آئیں گے۔

### 🔢 Precedence Table (High to Low)

| Precedence Level | Operators                      | Description                          |
|------------------|--------------------------------|--------------------------------------|
| 1 (Highest)      | `++`, `--`, `!`                | Unary operators                      |
| 2                | `*`, `/`, `%`                  | Multiplication, division, modulus    |
| 3                | `+`, `-`                       | Addition, subtraction                |
| 4                | `<`, `>`, `<=`, `>=`           | Relational comparisons               |
| 5                | `==`, `!=`                     | Equality checks                      |
| 6                | `&&`                           | Logical AND                          |
| 7                | `||`                           | Logical OR                           |
| 8 (Lowest)       | `=`                            | Assignment                           |

> Operators with higher precedence are evaluated first.  
> Equal precedence is resolved **left to right**, except assignment (`=`), which is **right to left**.

---





## Example Problem:

Create variables for student marks, height, grade, and pass status. Assign values and display them.

## 🧩 Step-by-Step Solution 

### 1. ✅ Problem Definition  

Create a program that calculates the total and average marks of a student using arithmetic operators, and checks if the student passed using relational and logical operators.

---

### 2. 🧠 Problem Analysis  

- Declare three integer variables for marks in three subjects.  
- Use arithmetic operators to calculate total and average.  
- Use relational and logical operators to check if the student passed (average ≥ 50).  
- Display all results.


---

### 3. 🧮 Design Algorithm  
**Steps**:
1. Start the program.
2. Declare three `int` variables: `mark1`, `mark2`, `mark3`.
3. Calculate `total = mark1 + mark2 + mark3`.
4. Calculate `average = total / 3`.
5. Check if `average >= 50` and all marks ≥ 40.
6. Display total, average, and pass/fail result.
7. End the program.

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
- Handles `#include <iostream>`  
- Includes the I/O stream library so `cout` and `endl` can be used.

---

### 6. 🧩 Compiler  
- Converts the source code into object code.  
- Checks for syntax errors and type compatibility.

---

### 7. 🔗 Linker  
- Links object code with standard libraries.  
- Resolves references like `cout`, `endl`.

---

### 8. 🚚 Loader  
- Loads the executable into memory.  
- Prepares runtime environment and allocates memory.

---

### 9. ▶️ Execution  
- Program starts at `main()`.  
- Variables are initialized.  
- Arithmetic and logical operations are performed.  
- Output is displayed:

```
Total Marks: 185
Average Marks: 61.6667
Passed: 1
```

> Note: `Passed: 1` means `true`. If the condition fails, it would show `0`.

---


