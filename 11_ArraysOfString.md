# 📦 Arrays of Strings in C++

## 🔹 What is a String Array?

A string array is an array where each element is a string (text).  
String array ek aisa array hai jisme har element **text** hota hai.

It allows storing multiple strings under one variable name.  
Yeh ek hi variable name ke zariye multiple strings store karne ki sahulat deta hai.

**Real-Life Use Cases:**  
- Student names  
- Product names  
- City names  
- Menu options

---

## 🧩 Declaring and Initializing String Arrays

### 1️⃣ Using `string` data type

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string fruits[3] = {"Apple", "Banana", "Mango"};
    cout << fruits[0] << endl; // Output: Apple
    return 0;
}
```

fruits[0] → first string

fruits[1] → second string

fruits[2] → third string


Analogy:
Think of it like boxes on a shelf 🗂️:

Each box (index) holds one fruit (string).

Access any box by its number (index).



---

🔁 Traversing String Arrays

Use a loop to visit all elements:

```cpp
for(int i = 0; i < 3; i++)
    cout << fruits[i] << " ";
```

Output: Apple Banana Mango

Analogy: Teacher calling all student names one by one.


---

🔍 Searching in String Arrays

```cpp
string searchName = "Mango";
for(int i = 0; i < 3; i++) {
    if(fruits[i] == searchName)
        cout << searchName << " found at index " << i << endl;
}
```

Finds the position of a string in the array.

Real-Life: Check if a city exists in a list of cities.



---

✏️ Updating a String in Array

```cpp
fruits[1] = "Orange";
cout << fruits[1]; // Output: Orange

```
Changes the value of an element.

Analogy: Replacing a book in a shelf with a new one.



---

➕ Summation / Concatenation (Optional)

You can concatenate strings:

```cpp
string allFruits = "";
for(int i = 0; i < 3; i++)
    allFruits += fruits[i] + " ";
cout << allFruits;
```

Output: Apple Mango Orange

Combines all strings into one sentence.

Real-Life: Listing all menu items in a single line.



---

🔧 Passing String Arrays to Functions

```cpp
void printStrings(string arr[], int size) {
    for(int i = 0; i < size; i++)
        cout << arr[i] << " ";
    cout << endl;
}

int main() {
    string fruits[3] = {"Apple", "Banana", "Mango"};
    printStrings(fruits, 3);
    return 0;
}

```

Arrays are passed by reference.

Changes inside the function affect the original array.



---

🔹 Multi-Dimensional String Arrays

A 2D string array stores rows and columns of strings.

```cpp
string seats[2][3] = {
    {"Alice", "Bob", "Charlie"},
    {"David", "Eva", "Frank"}
};

// Access
cout << seats[1][2]; // Output: Frank

seats[0][0] → Alice

seats[1][2] → Frank

```

Analogy:
Classroom seating chart 🏫:

Rows = rows of students

Columns = seats

Each cell = student name



---

🔁 Nested Loops for 2D String Arrays

```cpp
for(int i = 0; i < 2; i++) {         // rows
    for(int j = 0; j < 3; j++) {     // columns
        cout << seats[i][j] << " ";
    }
    cout << endl;
}

```

Outer loop → selects row

Inner loop → iterates columns in that row


Output:

Alice Bob Charlie
David Eva Frank


---

### Program demonstrating 1D String Array
```cpp
#include <iostream>
#include <string>
using namespace std;

// Function to print 1D array
void printArray(string arr[], int size) {
    for(int i = 0; i < size; i++)
        cout << arr[i] << " ";
    cout << endl;
}

int main() {
    string fruits[3] = {"Apple", "Banana", "Mango"};

    cout << "Original Array: ";
    printArray(fruits, 3);

    // Searching and updating
    for(int i = 0; i < 3; i++) {
        if(fruits[i] == "Banana") {
            fruits[i] = "Orange"; // Update
            cout << "Banana updated to Orange at index " << i << endl;
        }
    }

    cout << "Updated Array: ";
    printArray(fruits, 3);

    return 0;
}
```
---

### Program demonstrating 2D Or Multi-Dimensional String Array

```cpp
#include <iostream>
#include <string>
using namespace std;

// Function to print 2D array
void printMatrix(string matrix[][3], int rows) {
    for(int i = 0; i < rows; i++) {
        for(int j = 0; j < 3; j++)
            cout << matrix[i][j] << " ";
        cout << endl;
    }
}

int main() {
    string seats[2][3] = { {"Alice", "Bob", "Charlie"}, {"David", "Eva", "Frank"} };

    cout << "Original 2D Array:" << endl;
    printMatrix(seats, 2);

    // Searching
    for(int i = 0; i < 2; i++) {
        for(int j = 0; j < 3; j++) {
            if(seats[i][j] == "Eva") {
                cout << "Found Eva at row " << i << ", column " << j << endl;
            }
        }
    }

    // Updating
    seats[0][2] = "Grace";
    cout << "Updated 2D Array:" << endl;
    printMatrix(seats, 2);

    return 0;
}
```
---
