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
| String Declaration     | `string variable;`                | Declares an empty string variable(object).                                 | `string msg;`                                |
| String Initialization  | `string variable = "text";`       | Declares and assigns a string value                               | `string name = "Ali";`                       |
| String Concatenation   | `str1 + str2`                     | Joins two strings together                                        | `"Hello " + name`                            |
| String Input (single word) | `cin >> variable;`            | Reads input until first space (single word only)                  | `cin >> name;`                               |
| String Input (full line)   | `getline(cin, variable);`     | Reads entire line including spaces                                | `getline(cin, name);`                        |
| String Output          | `cout << variable;`               | Displays string on screen                                         | `cout << name;`                              |


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

---

## 🧩 Example Problem 1  

Store a name and city in string variables and display them.  

---

## ✅ Problem Definition  

Create a simple program that use two different variables to stores two string values and prints them using `cout`.  

---

## 🔍 Problem Analysis  
- Use `std::string` to store name and city  
- Assign values directly to variables  
- Use `cout` to display output

---

## 🧮 Algorithm  
1. Start the program  
2. Declare two string variables.  
3. Assign values to both variables  
4. Display the values using `cout`  
5. End the program

---

## 💻 Program

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {

    string fullName = "Muslim Ali";
    string city = "Skradu";

    cout << "Full Name: " << fullName << endl;
    cout << "City: " << city << endl;

    return 0;
}
```

---

### 🧪 Output
```
Full Name: Muslim Ali
City: Skardu
```


### ✅ Example Problem 2

Ask the user for their name and city, then display a welcome message.  

## 🧩 Problem Definition  

we need user's name and city to display a welcome message to them.  

---

## 🔍 Problem Analysis  
- Use `std::string` to store name and city
- Use `getline()` for multi-word input (name)  
- Use `cin >>` for single-word input (city)  
- Use `cout` to display the final message  

---

## 🧮 Algorithm  
1. Start the program  
2. Declare string variables: `name`, `city`  
3. Input full name using `getline()`    
5. Input city using `cin >>`  
6. Concatenate and display message  
7. End the program

## 💻 Program

```cpp

#include <iostream>
#include <string>
using namespace std;

int main() {
    string fullName;  
    string city; 

    cout << "Enter your full name: ";
    getline(cin, fullName);  // reads full line including spaces

    cout << "Enter your city: ";
    cin >> city;  // reads one word only

    cout << "Welcome " << fullName << " from " << city << "!" << endl;

    return 0;
}

```
---

### 🧪 Sample Input
```
Enter your full name: Sartaj ALi
Enter your city: Skardu
```

### 📤 Output
```
Welcome Sartaj from Skardu!
```

---




````

