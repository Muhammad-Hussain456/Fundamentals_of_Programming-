# 🌟 C++ Fundamentals 
**سی پلس پلس کی بنیادی باتیں**

---

## 📌 Program Structure  
Every C++ program must begin execution from the `main()` function.  
ہر پروگرام میں `main()` فنکشن ہونا ضروری ہے، جہاں سے عمل شروع ہوتا ہے۔

```cpp
#include <iostream>   // Input/Output library included
using namespace std;  // Allows direct use of standard names

int main() {
    // Code goes here
    return 0;
}
```

### 🔍 Syntax and Semantics

| Construct               | Syntax in C++             | Semantic in C++                                                                 |
|------------------------|---------------------------|----------------------------------------------------------------------------------|
| Include I/O Library    | `#include <iostream>`     | Adds the standard input/output stream library to use `cin`, `cout`, etc.        |
| Namespace Usage        | `using namespace std;`    | Enables direct use of standard library names without prefixing `std::`          |
| Main Function          | `int main() { ... }`      | Defines the program’s entry point and returns an integer to the operating system|

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

| Construct             | Syntax in C++           | Semantic in C++                                                       |
|----------------------|-------------------------|------------------------------------------------------------------------|
| Declaration          | `int age;`              | Declares a variable of type `int`                                     |
| Initialization       | `int age = 25;`         | Declares and assigns an initial value                                 |
| Assignment           | `age = 30;`             | Updates the value of a variable using the assignment operator `=`     |

---

## 📊 Data Types and Ranges  
Data types define the kind of data a variable can store.  
ڈیٹا ٹائپ بتاتا ہے کہ ویری ایبل کس قسم کا ڈیٹا رکھ سکتا ہے۔

| Data Type     | Storage     | Example Values         | Range (32-bit)                     | Purpose                        |
|---------------|-------------|------------------------|------------------------------------|--------------------------------|
| `int`         | 4 bytes     | 10, -5, 200            | -2,147,483,648 to 2,147,483,647    | Whole numbers                  |
| `short int`   | 2 bytes     | -300, 500              | -32,768 to 32,767                  | Small whole numbers            |
| `long int`    | 4/8 bytes   | 2000000000             | System-dependent                   | Large whole numbers            |
| `float`       | 4 bytes     | 5.9, -3.14             | 3.4e-38 to 3.4e+38                 | Decimal numbers                |
| `double`      | 8 bytes     | 3.14159265             | 1.7e-308 to 1.7e+308               | High precision decimals        |
| `long double` | 10+ bytes   | Very large decimals    | Very large range                   | Scientific calculations        |
| `char`        | 1 byte      | 'A', '%', 'b'          | -128 to 127 / 0 to 255             | Single characters              |
| `bool`        | 1 byte      | true, false            | 0 or 1                             | Logical conditions             |

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

| Construct        | Syntax in C++                      | Semantic in C++                                      |
|------------------|------------------------------------|------------------------------------------------------|
| Output           | `cout << "Text";`                  | Displays text or values on the screen                |
| Input            | `cin >> variable;`                 | Receives input from the user and stores it in a variable |
| Combined Output  | `cout << var1 << var2;`            | Displays multiple values in sequence                 |

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

| Type            | Syntax in C++               | Semantic in C++                                         |
|-----------------|-----------------------------|----------------------------------------------------------|
| Implicit        | `float b = a;`              | Automatically converts `int` to `float`                 |
| Explicit        | `int y = (int)x;`           | Manually casts `float` to `int`                         |

---

## 🧪 Example Program

### 🎯 Problem 
Create variables for student marks, height, grade, and pass status. Assign values and display them.

### 1. ✅ Problem Definition

Create a program that stores and displays a student's marks, height, grade, and pass status.
---

### 2. 🧠 Problem Analysis 

**Requirements**:  
- Declare variables for each data item.  
- Assign appropriate values.  
- Display the values using output statements.

---

### 3. 🧮 Design Algorithm  
**Steps**:
1. Start the program.
2. Declare variables:
   - `marks` → `int`
   - `height` → `float`
   - `grade` → `char`
   - `passed` → `bool`
3. Assign values:
   - `marks = 85`
   - `height = 5.9`
   - `grade = 'A'`
   - `passed = true`
4. Display each value using `cout`.
5. End the program.

---

### 4. 💻 Coding  
```cpp
#include <iostream>       // Preprocessor includes I/O library
using namespace std;      // Allows direct use of cout, endl, etc.

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

### 5. ⚙️ Preprocessor  
- Handles `#include <iostream>`  
- Inserts the contents of the I/O library before compilation begins.  
- Makes `cin`, `cout`, `endl` available to the program.

---

### 6. 🧩 Compiler  
- Translates the C++ source code into **object code** (machine-readable instructions).  
- Checks for syntax errors and type mismatches.

---

### 7. 🔗 Linker  
- Combines object code with **standard libraries** (like I/O functions).  
- Resolves external references (e.g., `cout` is linked to its definition in the standard library).

---

### 8. 🚚 Loader  
- Loads the final executable into memory.  
- Prepares the program for execution by allocating memory and setting up runtime environment.

---

### 9. ▶️ Execution  
- The program starts from `main()`.  
- Variables are initialized.  
- Output is displayed on the screen:
  ```
  Marks: 85
  Height: 5.9
  Grade: A
  Passed: 1
  ```


> Note: `true` is displayed as `1` because `cout` prints boolean values as integers by default.

---

Would you like me to add a section on control structures (if, loops, switch) or functions next?
