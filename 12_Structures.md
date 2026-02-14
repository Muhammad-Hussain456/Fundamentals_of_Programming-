# 🏗️ Structures in C++

Structures (`struct`) are user-defined data types in C++ that allow grouping variables of different data types under one name. Unlike arrays (which store multiple values of the same type), structures can store heterogeneous data.

---

## 🔹 Structure Declaration & Initialization

### ✅ Syntax
```cpp
struct StructName {
    dataType member1;
    dataType member2;
    ...
};
```

### 💻 Example
```cpp
#include <iostream>
using namespace std;

struct Student {
    int rollNo;
    string name;
    float marks;
};

int main() {
    Student s1 = {101, "Ali", 85.5};   // Initialization
    cout << s1.rollNo << " " << s1.name << " " << s1.marks << endl;
    return 0;
}
```

---

## 🔹 Array of Structures

We can create multiple records using arrays of structs.

```cpp
#include <iostream>
using namespace std;

struct Student {
    int rollNo;
    string name;
    float marks;
};

int main() {
    Student students[3] = {
        {101, "Ali", 85.5},
        {102, "Sara", 90.0},
        {103, "Ahmed", 78.2}
    };

    for(int i = 0; i < 3; i++) {
        cout << students[i].rollNo << " " << students[i].name << " " << students[i].marks << endl;
    }
    return 0;
}
```

📌 **Use Case:** Storing records of multiple students, employees, or products.

---

## 🔹 Nested Structures

Structures can contain other structures as members.

```cpp
#include <iostream>
using namespace std;

struct Address {
    string city;
    int zip;
};

struct Student {
    int rollNo;
    string name;
    Address addr;   // Nested struct
};

int main() {
    Student s1 = {101, "Ali", {"Karachi", 74000}};
    cout << s1.name << " lives in " << s1.addr.city << " with ZIP " << s1.addr.zip << endl;
    return 0;
}
```

📌 **Use Case:** Student with address, employee with department details, etc.

---

## 🔹 Structs with Functions

Functions can be defined inside structs (similar to classes).

```cpp
#include <iostream>
using namespace std;

struct Student {
    int rollNo;
    string name;
    float marks;

    void display() {
        cout << rollNo << " " << name << " " << marks << endl;
    }
};

int main() {
    Student s1 = {101, "Ali", 85.5};
    s1.display();
    return 0;
}
```

📌 **Use Case:** Encapsulation of data + behavior (like classes, but simpler).

---

## 🔹 Pointers to Structures

We can use pointers to access struct members with `->`.

```cpp
#include <iostream>
using namespace std;

struct Student {
    int rollNo;
    string name;
    float marks;
};

int main() {
    Student s1 = {101, "Ali", 85.5};
    Student *ptr = &s1;

    cout << ptr->rollNo << " " << ptr->name << " " << ptr->marks << endl;

    return 0;
}
```

📌 **Use Case:** Dynamic memory allocation, linked lists, trees, graphs.

---

## 🧩 Summary Table

| Concept              | Example Keyword | Use Case |
|----------------------|-----------------|----------|
| Declaration          | `struct Student` | Define custom data type |
| Initialization       | `Student s1 = {...}` | Store values |
| Array of Structs     | `Student students[3]` | Multiple records |
| Nested Structs       | `struct Address inside Student` | Hierarchical data |
| Struct Functions     | `void display()` | Behavior with data |
| Pointers to Structs  | `Student *ptr` | Dynamic structures |

---
