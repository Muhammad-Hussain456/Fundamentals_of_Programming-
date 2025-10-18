# 🧵 Strings in C++

---

## 📌 What Is a String?

A **string** is a sequence of characters used to represent text.  ۔

We use the preprocessor directive `#include <string>`, which includes the `<string>` header file that allows us to use `std::string` class to create string objects in a C++ program.

**Note:-* The concepts of **object** and **class** will be discussed in the **OOP course** which is taught in the **2nd semester**.

---

### 🔍 Syntax and Semantics

| Construct              | Syntax in C++                     | Semantic in C++                                                   | Example                                      |
|------------------------|-----------------------------------|-------------------------------------------------------------------|----------------------------------------------|
| Header File Inclusion  | `#include <string>`               | Adds the `<string>` header file.                                  | `#include <string>`                          |
| String Declaration     | `string variable;`                | Declares an empty string object                                   | `string msg;`                                |
| String Initialization  | `string variable = "text";`       | Declares and assigns a string value                               | `string name = "Ali";`                       |
| String Concatenation   | `str1 + str2`                     | Joins two strings together                                        | `"Hello " + name`                            |
| String Input (single word) | `cin >> variable;`            | Reads input until first space (single word only)                  | `cin >> name;`                               |
| String Input (full line)   | `getline(cin, variable);`     | Reads entire line including spaces                                | `getline(cin, name);`                        |
| String Output          | `cout << variable;`               | Displays string on screen                                         | `cout << name;`                              |


---

## 🧩 Example Problem

Write a program that takes user's name and city, then displays a welcome message.

---

## 🧠 Step-by-Step Solution

### ✅ Problem Definition  
Store and display personalized greeting using `std::string`.

### 🔍 Problem Analysis  
- Use `std::string` for name and city  
- Use `cin >>` or `getline()` for input  
- Concatenate strings  
- Display using `cout`

### 🧮 Design Algorithm  
1. Start program  
2. Declare `name`, `city`  
3. Take input using `getline()`  
4. Create message using `+` operator  
5. Display message  
6. End program

---

### 💻 Coding
```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string name;
    string city;

    cout << "Enter your name: ";
    getline(cin, name);

    cout << "Enter your city: ";
    getline(cin, city);

    string message = "Welcome " + name + " from " + city + "!";

    cout << message << endl;

    return 0;
}
```
---

### 🔍 `cin >>` vs `getline(cin, ...)`

| Feature / خصوصیت         | `cin >>`                                      | `getline(cin, variable)`                                  |
|--------------------------|-----------------------------------------------|------------------------------------------------------------|
| 📌 Purpose / مقصد         | Reads input until the first space             | Reads the entire line including spaces                     |
| 🧠 Behavior               | Stops at whitespace (space, tab, newline)     | Continues until newline is encountered                     |
| 🧪 Input Example          | `Ali Raza`                                    | `Ali Raza`                                                 |
| 📤 Stored Result          | `"Ali"`                                       | `"Ali Raza"`                                               |
| ✅ Use Case / استعمال کب کریں | For single-word input (e.g., roll number)     | For full names, addresses, or sentences                    |
| ⚠️ Limitation / حد         | Cannot read multi-word input                  | Requires flushing leftover newline if used after `cin >>`  |



````

