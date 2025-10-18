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

## 💡 Data Types and Range (حد)

**Data types** define what type of data a variable can store.
ڈیٹا ٹائپ بتاتا ہے کہ ویری ایبل کس قسم کا ڈیٹا رکھ سکتا ہے۔
**Range** tells the limits of that type. حد یہ بتاتی ہے کہ ویری ایبل میں کس حد تک کی ویلیو محفوظ کی جا سکتی ہے۔


## 🧮 5. How Each Data Type Gets an Address or Word in Memory

Each data type occupies a specific number of **bytes (memory cells)**, and each byte has its own **address**.  
Larger types occupy **consecutive addresses**.

| **Data Type** | **Storage(Addresses allocated in memory)(Bytes)(Typical Size)** | **Memory Allocation** | **Example (Starting Address = 1000)** |
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


### Storage and range of Data types (Signed and Unsigned)

**Note:** 
To learn how to find the range using the formula, see the section **Why Range is different for signed and Unsigned DataTypes**

**Note:** In the table below, **n** = number of bits.

| Data Type | Storage(Addresses allocated in memory)(Bytes)(Typical Size) | Example Values | Range Formula | Range | Purpose / Use Case |
| :--- | :---: | :--- | :--- | :--- | :--- |
| **signed char** | 1(8 bits) | -100, 0, 100 | −2ⁿ⁻¹ to (2ⁿ⁻¹ − 1) | −128 to 127 | Small signed numbers or characters |
| **unsigned char** | 1(8 bits) | 0, 50, 255 |  0 to (2ⁿ − 1) | 0 to 255 | Small positive numbers, binary data |
| **signed short int** | 2(16 bits) | -30000, 0, 30000 | −2ⁿ⁻¹ to (2ⁿ⁻¹ − 1) | −32,768 to 32,767 | Small signed integers |
| **unsigned short int** | 2(16 bits) | 0, 20000, 65000 |  0 to (2ⁿ − 1) | 0 to 65,535 | Small positive integers |
| **signed int** | 4(32 bits) | -100000, 0, 500000 | −2ⁿ⁻¹ to (2ⁿ⁻¹ − 1) | −2,147,483,648 to 2,147,483,647 | General-purpose signed integers |
| **unsigned int** | 4(32 bits) | 0, 1000000, 4000000000 |  0 to (2ⁿ − 1) | 0 to 4,294,967,295 | General-purpose positive integers |
| **signed long int** | 4(32 bits) or 8(64 bits) | -1000000000, 0, 2000000000 | −2ⁿ⁻¹ to (2ⁿ⁻¹ − 1) | Platform dependent | Large signed integers |
| **unsigned long int** | 4(32 bits) or 8(64 bits) | 0, 1000000000, 4000000000 |  0 to (2ⁿ − 1) | Platform dependent | Large positive integers |
| **signed long long int** | 8(64 bits) | -10¹⁸, 0, 10¹⁸ | −2ⁿ⁻¹ to (2ⁿ⁻¹ − 1) | −9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | Very large signed integers |
| **unsigned long long int** | 8(64 bits) | 0, 10¹⁸ |  0 to (2ⁿ − 1) | 0 to 18,446,744,073,709,551,615 | Very large positive integers |
| **float** | 4(32 bits) | 3.14, -2.5 | IEEE 754 | ±3.4 × 10⁻³⁸ to ±3.4 × 10³⁸ | Decimal numbers (single precision) |
| **double** | 8(64 bits) | 3.14159, -0.001 | IEEE 754 | ±1.7 × 10⁻³⁰⁸ to ±1.7 × 10³⁰⁸ | Decimal numbers (double precision) |
| **long double** | 12(96 bits) or 16(120 bits) | 3.1415926535 | IEEE 754 | ±3.4 × 10⁻⁴⁹³² to ±1.1 × 10⁴⁹³² | High precision decimals |
| **bool** | 1(8 bits) | true, false | — | 0 or 1 | Logical values (True/False) |



---
### Why Range is different for signed and Unsigned DataTypes 

🧩 **Explanation**

In **signed types**, one bit is reserved for the sign (0 = positive, 1 = negative), leaving the rest for the value.

**Formula** → −2ⁿ⁻¹ to (2ⁿ⁻¹ − 1)

here **n** => number of bits

In **unsigned types**, all bits are used for the value, allowing only positive numbers.

**Formula** → 0 to (2ⁿ − 1)

  here **n** => number of bits.
  
**Example:-**

**Question/Problem:**

 Find the **range** for **signed int** and **unsigned int** Data type.
 

**Answer/Solution:**

For **int** or **signed int**:

**Formula:**

−2ⁿ⁻¹ to (2ⁿ⁻¹ − 1) 

(As we know, storage unit for *int* is 4 bytes = 32 bits)
 
−2ⁿ⁻¹ = -2³²⁻¹

      = -2³¹
      
      = −2,147,483,648
      

2ⁿ⁻¹ − 1 = 2³²⁻¹ - 1

         = 2³¹ - 1
         
         = 2,147,483,648 - 1 
         
         = 2,147,483,647
         

So the **range** for **int*" or **signed int** is −2,147,483,648  to 2,147,483,647.

For **unsigned int**:

**Formula:**

0 to (2ⁿ − 1) 

(As we know, storage unit for *int* is 4 bytes = 32 bits)

2ⁿ − 1 = 2³² - 1

       = 4,294,967,296 - 1
       
       = 4,294,967,295
       

So the **range** for **unsigned int** is 0  to 4,294,967,295.




**Note:** Same formulas are used to find range for all other datatypes.


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
| Output          | `cout << value;`   | Displays text or values on the screen | `int num1 = 5; cout << num1;` , `cout << "Hello World";` , `cout << "5 + 6 = " << 5 + 6;` |
| Input           | `cin >> variable;`      | Receives input from the user          | `int age; cin >> age;`    |
| Combined Output | `cout << value1 << value2;` | Displays multiple values in sequence  | `cout << "Age: " << age;` |

### 🧩 `cout << value;`

- **`cout`** → stands for **console output** (from `<iostream>` header)  
- **`<<`** → is the **insertion operator**, which sends data to the output stream  
- **`value`** → can be anything that produces data, such as:  
  - a **string** → `"Hello"`  
  - a **number** → `42`  
  - a **variable** → `age`  
  - an **operation** → `a + b` => addition operation 
  - an **expression** → `(x * y) / 2`  
  - a **statement** → cout << "The sum is: " << (a + b);

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
| Explicit Type Conversion| `datatype var1 = (datatype)var2; / datatype var = (datatype)(value); / datatype var1 = static_cast<datatype> (var2);` | Manually casts datatype of var2 to specified type | `float x = 5.9; int y = (int)x;` |


### Different ways of Explicit Type conversion:-

**1. datatype var1 = (datatype)var2;**	
        
**Example:-**
```cpp
  float a = 5.7;
  int b  = (int)a;	

 ```
**2. datatype var = (datatype)(value);**

**Example:-**
```cpp
int b =(int)(7.8);	
        
```



**3. datatype var1 = static_cast<datatype> (var2);**
     
**Example:-**

```cpp
  float a = 5.7;
  int b = static_cast<int>(b);	

```

**4. datatype var = static_cast<datatype> (value);**

 **Example:-**
 
 ```cpp
  int b = static_cast<int>(6.3);	
        
 ```

Ap Jo Kam krna Chahtay h us hisab sy in m sy ksi ka b use kr sktay h.
Ya phir agr ap variable m store nahi krna Chahtay aur srf output p type convert kr k show krna Chahtay h to simple **cout** k zrye b kr sktay Hain.
Jesay ki:-

```cpp
cout <<< "datatype converted: " << static_cast<int>(10.2);
```
Or
```cpp
cout << " datatype converted: " << (int)(12.4);
```
Or
```cpp
int a = 5.9;
cout << "datatype converted: " << (int)a;
```
---

## Escape sequences 
Escape sequences in C++ are special character combinations that begin with a backslash`(\)` and represent characters have special meaning in formatting. They're commonly used in strings and character literals.

### 🔍 Syntax and Semantics for Escape sequences 

| Escape Sequence | Syntax Example         | Semantics / Meaning                        |
|------------------|------------------------|--------------------------------------------|
| `\n`             | `cout << "Line1\nLine2";` | Inserts a newline; moves cursor to next line |
| `\t`             | `cout << "A\tB";`        | Inserts a horizontal tab space              |
| `\"`             | `cout << "\"Quoted\"";`  | Inserts double quotation marks              |
| `\\`             | `cout << "C:\\Path";`    | Inserts a backslash character               |


### std::endl vs \n in C++

std::endl and \n both seem to do the same thing but there is a precise difference between them. 

- **endl** is a manipulator that inserts a new line and ensures that data is sent to the intended output, such as a file or console, without delay, while  **\n** is an Escape Sequence Character that only inserts a new line.

- **endl** doesn't occupy any memory but **\n** occupies 1 byte memory as it is a character.


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
