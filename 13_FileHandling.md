# 📂 File Handling in C++

File handling in C++ allows programs to store and retrieve data permanently using files. It is done using **file streams** provided by the `<fstream>` library.

---

## 🔹 File Streams in C++

C++ provides three main classes for file handling:

| Class      | Purpose |
|------------|---------|
| `ifstream` | Input file stream → used for reading from files |
| `ofstream` | Output file stream → used for writing to files |
| `fstream`  | General file stream → supports both reading and writing |

---

## 🔹 Opening and Closing Files

### ✅ Syntax
```cpp
#include <fstream>
using namespace std;

ifstream inFile;   // for reading
ofstream outFile;  // for writing
fstream file;      // for both

inFile.open("input.txt");   // open file for reading
outFile.open("output.txt"); // open file for writing
file.open("data.txt", ios::in | ios::out); // both read & write

inFile.close();   // close file
outFile.close();
file.close();
```

📌 Always close files after use to free resources.

---

## 🔹 Reading and Writing Text Files

### Writing to a text file
```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    ofstream outFile("example.txt");   // open file for writing
    if(outFile.is_open()) {
        outFile << "Hello, File Handling!" << endl;
        outFile << "This is a text file." << endl;
    }
    outFile.close();
    return 0;
}
```

### Reading from a text file
```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    ifstream inFile("example.txt");   // open file for reading
    string line;
    if(inFile.is_open()) {
        while(getline(inFile, line)) {
            cout << line << endl;
        }
    }
    inFile.close();
    return 0;
}
```

---

## 🔹 Reading and Writing Binary Files

Binary files store data in raw memory format (not human-readable). Useful for images, audio, or serialized objects.

### Writing binary data
```cpp
#include <iostream>
#include <fstream>
using namespace std;

struct Student {
    int rollNo;
    char name[20];
    float marks;
};

int main() {
    Student s1 = {101, "Ali", 85.5};

    ofstream outFile("student.dat", ios::binary);
    outFile.write((char*)&s1, sizeof(s1));
    outFile.close();

    return 0;
}
```

### Reading binary data
```cpp
#include <iostream>
#include <fstream>
using namespace std;

struct Student {
    int rollNo;
    char name[20];
    float marks;
};

int main() {
    Student s2;

    ifstream inFile("student.dat", ios::binary);
    inFile.read((char*)&s2, sizeof(s2));
    inFile.close();

    cout << s2.rollNo << " " << s2.name << " " << s2.marks << endl;
    return 0;
}
```

---

## 🔹 File Modes

When opening files, we can specify modes:

| Mode         | Meaning |
|--------------|---------|
| `ios::in`    | Open for reading |
| `ios::out`   | Open for writing |
| `ios::app`   | Append to end of file |
| `ios::trunc` | Delete contents if file exists |
| `ios::binary`| Open in binary mode |

Example:
```cpp
fstream file("data.txt", ios::in | ios::out | ios::app);
```

---

## 🧩 Summary

- **`ifstream`** → read files  
- **`ofstream`** → write files  
- **`fstream`** → read/write files  
- Text files → human-readable  
- Binary files → raw memory format  
- Always **open** before use and **close** after use  

---

Would you like me to create a **single program** that demonstrates **all file operations together** (open, read, write, text, binary) just like we did for arrays and structs? That way you’ll have one consolidated reference.
