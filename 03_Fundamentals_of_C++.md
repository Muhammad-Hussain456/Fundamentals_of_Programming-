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

### 🔍 Syntax and Semantics

| Construct                | Syntax in C++                 | Semantic in C++                                                           | Example                                     |
| ------------------------ | ----------------------------- | ------------------------------------------------------------------------- | ------------------------------------------- |
| Preprocessor Directive | `#include <header>`           | Tells preprocessor to include a header file like iostream for I/O streams | `#include <iostream>`                       |
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
| Declaration    | `datatype variable;`         | Declares a variable with a specific datatype | `int age; float height;`         |
| Initialization | `datatype variable = value;` | Declares and assigns an initial value        | `int age = 25; float pi = 3.14;` |
| Assignment     | `variable = value;`          | Updates the value of a variable              | `age = 30;`                      |

---

## 💡 Data Types and Range (حد)

**Data types** define what type of data a variable can store.
ڈیٹا ٹائپ بتاتا ہے کہ ویری ایبل کس قسم کا ڈیٹا رکھ سکتا ہے۔
**Range** tells the limits of that type. حد یہ بتاتی ہے کہ ویری ایبل میں کس حد تک کی ویلیو محفوظ کی جا سکتی ہے۔

| Data Type   | Storage   | Example Values      | Range (32-bit)                  | Purpose                 | Example Code                 |
| ----------- | --------- | ------------------- | ------------------------------- | ----------------------- | ---------------------------- |
| int         | 4 bytes   | 10, -5, 200         | -2,147,483,648 to 2,147,483,647 | Whole numbers           | `int a = 100;`               |
| short int   | 2 bytes   | -300, 500           | -32,768 to 32,767               | Small whole numbers     | `short int s = 32000;`       |
| long int    | 4/8 bytes | 2000000000          | System-dependent                | Large whole numbers     | `long int l = 5000000000;`   |
| float       | 4 bytes   | 5.9, -3.14          | 3.4e-38 to 3.4e+38              | Decimal numbers         | `float f = 3.14;`            |
| double      | 8 bytes   | 3.14159265          | 1.7e-308 to 1.7e+308            | High precision decimals | `double d = 3.14159265;`     |
| long double | 10+ bytes | Very large decimals | Very large range                | Scientific calculations | `long double ld = 1.23e100;` |
| char        | 1 byte    | 'A', '%', 'b'       | -128 to 127 / 0 to 255          | Single characters       | `char grade = 'A';`          |
| bool        | 1 byte    | true, false         | 0 or 1                          | Logical conditions      | `bool isPassed = true;`      |

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
| Output          | `cout << expression;`   | Displays text or values on the screen | `cout << "Hello World";`  |
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
| Implicit | `datatype var1 = var2;`           | Automatically converts datatype of var2 to var1   | `int a = 5; float b = a;`        |
| Explicit | `datatype var1 = (datatype)var2;` | Manually casts datatype of var2 to specified type | `float x = 5.9; int y = (int)x;` |

---

## 🧪 Example Program

### Problem

Create variables for student marks, height, grade, and pass status. Assign values and display them.

### Coding

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

**Output**:

```
Marks: 85
Height: 5.9
Grade: A
Passed: 1
```

> Note: `true` is displayed as `1` because `cout` prints boolean values as integers by default.

---

## 🏗️ Program Execution Steps

1. **Preprocessor** – Processes directives like `#include`; makes `cin`, `cout`, `endl` available.
2. **Compiler** – Translates source code into object code; checks syntax and types.
3. **Linker** – Combines object code with standard libraries; resolves references.
4. **Loader** – Loads executable into RAM; allocates memory for variables.
5. **Execution** – CPU runs code from `main()`. Variables initialized, output displayed.

```

Do you want me to make that too?
```
