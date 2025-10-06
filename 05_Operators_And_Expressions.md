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



Would you like a quiz or practice problems to reinforce these operator concepts next?
