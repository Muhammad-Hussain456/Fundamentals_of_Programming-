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

for(int i = 0; i < 3; i++)
    cout << fruits[i] << " ";

Output: Apple Banana Mango

Analogy: Teacher calling all student names one by one.


---

🔍 Searching in String Arrays

string searchName = "Mango";
for(int i = 0; i < 3; i++) {
    if(fruits[i] == searchName)
        cout << searchName << " found at index " << i << endl;
}

Finds the position of a string in the array.

Real-Life: Check if a city exists in a list of cities.



---

✏️ Updating a String in Array

fruits[1] = "Orange";
cout << fruits[1]; // Output: Orange

Changes the value of an element.

Analogy: Replacing a book in a shelf with a new one.



---

➕ Summation / Concatenation (Optional)

You can concatenate strings:

string allFruits = "";
for(int i = 0; i < 3; i++)
    allFruits += fruits[i] + " ";
cout << allFruits;

Output: Apple Mango Orange

Combines all strings into one sentence.

Real-Life: Listing all menu items in a single line.



---

🔧 Passing String Arrays to Functions

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

Arrays are passed by reference.

Changes inside the function affect the original array.



---

🔹 Multi-Dimensional String Arrays

A 2D string array stores rows and columns of strings.

string seats[2][3] = {
    {"Alice", "Bob", "Charlie"},
    {"David", "Eva", "Frank"}
};

// Access
cout << seats[1][2]; // Output: Frank

seats[0][0] → Alice

seats[1][2] → Frank


Analogy:
Classroom seating chart 🏫:

Rows = rows of students

Columns = seats

Each cell = student name



---

🔁 Nested Loops for 2D String Arrays

for(int i = 0; i < 2; i++) {         // rows
    for(int j = 0; j < 3; j++) {     // columns
        cout << seats[i][j] << " ";
    }
    cout << endl;
}

Outer loop → selects row

Inner loop → iterates columns in that row


Output:

Alice Bob Charlie
David Eva Frank


---

🧠 Summary

Operation	Example

Declare & Initialize	string fruits[3] = {"Apple","Banana","Mango"};
Access	fruits[0] → Apple
Traverse	for(int i=0;i<3;i++) cout<<fruits[i];
Search	if(fruits[i]=="Mango")
Update	fruits[1]="Orange";
Concatenate	Combine all strings into one sentence
Pass to Function	printStrings(fruits, 3);
2D Array	string seats[2][3]; seats[1][2] = "Frank";


Loops:

Single loop → 1D string array

Nested loops → 2D string array


Real-Life Analogies:

Shelf of books, classroom seating chart, menu list, student names.



---
