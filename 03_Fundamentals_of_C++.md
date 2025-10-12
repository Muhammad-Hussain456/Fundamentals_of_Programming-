````markdown
# 🌟 C++ Fundamentals 

## 📌 Program Structure  
Every C++ program must begin execution from the `main()` function.  
ہر پروگرام میں `main()` فنکشن ہونا ضروری ہے، جہاں سے عمل شروع ہوتا ہے۔

```cpp
#include <iostream>   // Input/Output header file included
using namespace std;  // Allows direct use of standard names

int main() {
    // Code goes here
    return 0;
}
````

### constructs:

**Programming constructs** are the fundamental building blocks used to create programs. That's why, we should understand the syntax, semantic and examples of each construct.

### 🔍 Syntax and Semantics

| Construct                | Syntax in C++                 | Semantic in C++                                                           | Example                                     |
| ------------------------ | ----------------------------- | ------------------------------------------------------------------------- | ------------------------------------------- |
| Preprocessor Directive | `#include <header>`           | Tells preprocessor to include a header file.                                | `#include <iostream>`                       |
| Namespace Usage          | `using namespace identifier;` | Enables direct use of standard objects without `std::` prefix             | `using namespace std;`                      |
| Main Function            | `int main()`                  | Defines the program’s entry point; returns an integer to the OS           | `int main() { cout << "Hello"; return 0; }` |

---

## 🧠 Variables

Variables are named memory locations used to store data.
ویری ایبل میموری میں نامزد جگہیں ہیں جہاں ڈیٹا محفوظ کیا جاتا ہے۔

```cpp
int age;
float height;
char grade;
bool isPassed;
```

### 🔍 Syntax and Semantics

| Construct      | Syntax in C++                | Semantic in C++                              | Example                          |
| -------------- | ---------------------------- | -------------------------------------------- | -------------------------------- |
| variable Declaration    | `datatype variable;`         | Declares a variable with a specific datatype | `int age; float height;`         |
| variable Initialization | `datatype variable = value;` | Declares and assigns an initial value        | `int age = 25; float pi = 3.14;` |
| variable Assignment     | `variable = value;`          | Updates the value of a variable              | `age = 30;`                      |


## ⚙️ Memory Concepts in Computing

Understanding how data is stored, addressed, and processed in memory is fundamental to computer architecture and programming.

---

### 🧩 1. Bit

**Definition:**  
A **bit (binary digit)** is the **smallest unit of data** in a computer.

**Value:**  
It can be either **0** or **1**.

**Example:**  
`10110010` → 8 bits (binary representation)

---

### 💾 2. Byte

**Definition:**  
A **byte** is a group of **8 bits**.

**Use:**  
It is the **basic addressable unit** of memory in most computer systems.

**Example:**  
1 Byte = 8 bits → can store values from **0 to 255** (unsigned).

---

### 🧠 3. Address in Memory

**Definition:**  
Every **byte in memory** has a **unique address**, like house numbers on a street.  
The **CPU uses these addresses** to read or write data.

**Example:**

| **Address** | 1000 | 1001 | 1002 | 1003 |
|--------------|------|------|------|------|
| **Contents** | 01101000 | 01100101 | 01101100 | 01101100 |

➡️ These 4 bytes together may store the word **"hell"**.

---

### 📏 4. Word in Memory

**Definition:**  
A **word** is the **standard unit of data** a CPU can process in one operation.  

The **word size** determines how much data the CPU can process at once.

It depends on the **CPU architecture**.


| **Architecture** | **Word Size** |
|-------------------|---------------|
| 8-bit CPU | 1 byte |
| 16-bit CPU | 2 bytes |
| 32-bit CPU | 4 bytes |
| 64-bit CPU | 8 bytes |

**Example:**  
In a **32-bit system**, one **word = 4 bytes**.  
The CPU fetches or stores **4 bytes at a time**.

## Figure - Address, Content in address, and Word in Memory 

![Alt Text](Figures/03_memory_address%26word.png)

---

## 🧮 5. How Each Data Type Gets an Address or Word in Memory

Each data type occupies a specific number of **bytes (memory cells)**, and each byte has its own **address**.  
Larger types occupy **consecutive addresses**.

| **Data Type** | **Typical Size** | **Memory Allocation** | **Example (Starting Address = 1000)** |
|----------------|------------------|------------------------|---------------------------------------|
| `char` | 1 byte | Stored at one address | 1000 |
| `short` | 2 bytes | Occupies 2 consecutive bytes | 1000–1001 |
| `int` | 4 bytes | Occupies 4 consecutive bytes | 1000–1003 |
| `float` | 4 bytes | Occupies 4 consecutive bytes | 1000–1003 |
| `double` | 8 bytes | Occupies 8 consecutive bytes | 1000–1007 |
| `long long` | 8 bytes | Occupies 8 consecutive bytes | 1000–1007 |
| `bool` | 1 byte | Stored at one address | 1000 |

✅ **Note:**  
- Each variable’s starting **address** is assigned by the **compiler**.  
- Larger data types occupy **consecutive memory addresses**.  
- The **word size** determines how much data the CPU can process at once.

---


## 💡 Data Types and Range (حد)

**Data types** define what type of data a variable can store.
ڈیٹا ٹائپ بتاتا ہے کہ ویری ایبل کس قسم کا ڈیٹا رکھ سکتا ہے۔
**Range** tells the limits of that type. حد یہ بتاتی ہے کہ ویری ایبل میں کس حد تک کی ویلیو محفوظ کی جا سکتی ہے۔

### 🧮 Binary Representation of C++ Data Types

| **Data Type** | **Binary Representation (Bits)** | **Example Value** | **Example Binary Representation** |
|----------------|----------------------------------|-------------------|-----------------------------------|
| **int** | 32 bits | `10`, `-10` | `10 → 00000000 00000000 00000000 00001010` <br> `-10 → 11111111 11111111 11111111 11110110` *(two’s complement)* |
| **short int** | 16 bits | `5`, `-5` | `5 → 00000000 00000101` <br> `-5 → 11111111 11111011` *(two’s complement)* |
| **long int** | 32 or 64 bits (system-dependent) | `100000` | 32-bit: `00000000 00000000 00000001 10000100` |
| **float** | 32 bits (IEEE 754 format) | `5.5` | Sign = 0, Exponent = 10000001, Mantissa = 01100000000000000000000 → `01000000101100000000000000000000` |
| **double** | 64 bits (IEEE 754 format) | `3.14` | Sign = 0, Exponent = 10000000000, Mantissa = 10010010000111111011011 → `0100000000001001001000011111101101101110000101000111101011100000` |
| **long double** | 80–128 bits (extended precision) | `1.23e5` | Binary layout depends on compiler/architecture |
| **char** | 8 bits | `'A'` | `'A' → 01000001` |
| **bool** | 1 bit (stored as 1 byte) | `true`, `false` | `true → 00000001` <br> `false → 00000000` |

---


### Storage and range of Data types
| **Data Type** | **Storage** | **Example Values** | **Range Formula** | **Range (32-bit System)** | **Purpose** | **Example Code** |
|----------------|--------------|--------------------|-------------------|----------------------------|--------------|------------------|
| **int** | 4 bytes (32 bits) | 10, -5, 200 | Signed: −(2ⁿ⁻¹) → (2ⁿ⁻¹ − 1)<br>Unsigned: 0 → (2ⁿ − 1) | −2,147,483,648 → 2,147,483,647 | Whole numbers | `int a = 100;` |
| **short int** | 2 bytes (16 bits) | -300, 500 | Signed: −(2¹⁵) → (2¹⁵ − 1) | −32,768 → 32,767 | Small whole numbers | `short int s = 32000;` |
| **long int** | 4 or 8 bytes | 2000000000 | 32-bit: −(2³¹) → (2³¹ − 1)<br>64-bit: −(2⁶³) → (2⁶³ − 1) | System-dependent | Large whole numbers | `long int l = 5000000000;` |
| **float** | 4 bytes (32 bits) | 5.9, -3.14 | IEEE 754 format (1 sign bit, 8 exponent bits, 23 mantissa bits) | ≈ 3.4 × 10⁻³⁸ → 3.4 × 10³⁸ | Decimal numbers | `float f = 3.14;` |
| **double** | 8 bytes (64 bits) | 3.14159265 | IEEE 754 format (1 sign, 11 exponent, 52 mantissa bits) | ≈ 1.7 × 10⁻³⁰⁸ → 1.7 × 10³⁰⁸ | High precision decimals | `double d = 3.14159265;` |
| **long double** | 10–16 bytes | Very large decimals | Extended precision IEEE 754 | Very large range | Scientific calculations | `long double ld = 1.23e100;` |
| **char** | 1 byte (8 bits) | 'A', '%', 'b' | Signed: −(2⁷) → (2⁷ − 1)<br>Unsigned: 0 → (2⁸ − 1) | −128 → 127 / 0 → 255 | Single characters | `char grade = 'A';` |
| **bool** | 1 byte (8 bits) | true, false | — | 0 or 1 | Logical conditions | `bool isPassed = true;` |
```cpp

int FirstNumber = 2000000000;   // Correct
int SecondNumber = 3000000000;  // Incorrect, out of range
float pi = 3.14159;             // Fractional number
char letter = 'A';              // Single character
bool passed = true;             // True or False
```

---

## 🎯 Input/Output Operations

Input allows the program to receive data from the user.
Output displays data on the screen.
انپٹ آپریشن صارف سے ڈیٹا لیتا ہے، آؤٹ پٹ اسکرین پر دکھاتا ہے۔

```cpp
int age;
cout << "Enter your age: ";
cin >> age;
cout << "You are " << age << " years old.";
```

### 🔍 Syntax and Semantics

| Construct       | Syntax in C++           | Semantic in C++                       | Example                   |
| --------------- | ----------------------- | ------------------------------------- | ------------------------- |
| Output          | `cout << expression/statement;`   | Displays text or values on the screen | `cout << "Hello World";`  |
| Input           | `cin >> variable;`      | Receives input from the user          | `int age; cin >> age;`    |
| Combined Output | `cout << var1 << var2;` | Displays multiple values in sequence  | `cout << "Age: " << age;` |

---

## 🔄 Type Conversion

Type conversion changes a value from one data type to another.
ڈیٹا کی قسم تبدیل کرنا ایک قسم کی ویلیو کو دوسری قسم میں بدلنے کا عمل ہے۔

```cpp
int a = 5;
float b = a;      // implicit
float x = 5.9;
int y = (int)x;   // explicit
```

### 🔍 Syntax and Semantics

| Type     | Syntax in C++                     | Semantic in C++                                   | Example                          |
| -------- | --------------------------------- | ------------------------------------------------- | -------------------------------- |
| Implicit Type Conversion | `datatype var1 = var2;`           | Automatically converts datatype of var2 to var1   | `int a = 5; float b = a;`        |
| Explicit Type Conversion| `datatype var1 = (datatype)var2;` | Manually casts datatype of var2 to specified type | `float x = 5.9; int y = (int)x;` |

---

### 🔍 Syntax and Semantics for Next line and Spacing 

| Construct       | Syntax Example                      | Semantics / Meaning                            | Example Code                          | Output        |
|-----------------|-------------------------------------|------------------------------------------------|----------------------------------------|---------------|
| **Next Line**   | `cout << "\n";` or `cout << endl;` | Moves cursor to the next line (`endl` also flushes buffer) | `cout << "Hello\nWorld";`             | Hello<br>World |
| **Spacing**     | `cout << " " ;` or inside quotes `" "` | Adds space between outputs                     | `cout << "Hello" << " " << "World";`  | Hello World   |




## 🧪 Example Program

### Problem

Create variables for student marks, height, grade, and pass status. Assign values and display them.

---

🔍 Analysis

marks → int

height → float

grade → char

passed → bool

Use cout to display all values.



---

🪜 Algorithm

1. Start


2. Declare variables


3. Assign values


4. Display using cout


5. End




---

💻 Code
```cpp
#include <iostream>

using namespace std;

int main() {
    int marks = 85;
    float height = 5.9;
    char grade = 'A';
    bool passed = true;

    cout << "Marks: " << marks << endl;
    cout << "Height: " << height << endl;
    cout << "Grade: " << grade << endl;
    cout << "Passed: " << passed << endl;
    return 0;
}

```
---

🧾 Output

Marks: 85
Height: 5.9
Grade: A
Passed: 1
> Note: `true` is displayed as `1` because `cout` prints boolean values as integers by default.

---

## 🏗️ Program Execution Steps

1. **Preprocessor** – Processes directives like `#include`; makes `cin`, `cout`, `endl` available.
2. **Compiler** – Translates source code into object code; checks syntax and types.
3. **Linker** – Combines object code with standard libraries; resolves references.
4. **Loader** – Loads executable into RAM; allocates memory for variables.
5. **Execution** – CPU runs code from `main()`. Variables initialized, output displayed.

```
