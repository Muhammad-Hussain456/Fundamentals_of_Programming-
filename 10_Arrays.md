# 📦 Arrays in C++

## 🔹 What is an Array?

An array is a collection of elements of the same data type stored in contiguous memory locations (in rows or in both rows and columns).
Array ek data structure hai jo ek hi data type ki multiple values ko memory mein lagatar (continuous) store karta hai (rows mein ya rows aur columns dono mein).

It allows storing multiple values (in rows or in both rows and columns) under one variable name.
Yeh ek hi variable name ke zariye multiple values (rows mein ya rows aur columns dono mein) store karne ki sahulat deta hai.


---

### 🧠 Core Concepts

All elements must be of the same data type.
Sab elements ek hi data type ke hote hain.

Memory is contiguous (side by side).
Memory lagatar hoti hai, beech mein gap nahi hota.

Index starts from 0.
Index hamesha 0 se start hota hai.

### Loops in arrays:

Single loop → 1D arrays ke liye

Nested loops → 2D ya multi-dimensional arrays ke liye



Reason: Loops allow us to automatically access, traverse, update, or process all elements efficiently instead of manually handling each element.


---

## 🧩 Types of Arrays

### 1️⃣ One-Dimensional Array (1D)

A one-dimensional array stores elements in a single row (linear form).
1D array values ko ek seedhi line ya row mein store karta hai.

#### ✅ Syntax

dataType arrayName[size];

#### 💻 Example

int marks[5] = {80, 75, 90, 60, 85};

Index:   0   1   2   3   4
Value:  80  75  90  60  85

marks[2] gives 90.
marks[2] teesri value return karta hai.

#### 📌 Real-Life Use Cases

Student marks

Monthly salaries

Daily temperatures

Product prices


#### 🧠 Analogy

Think of a train with seats in a single row 🚆:

Train = array

Seats = index

Passenger = value


Har seat ko directly access kar sakte ho, jaise marks[2] = seat number 3 ka passenger.

#### Traversal: Single loop automatically checks each seat (element).


---

### 2️⃣ Two-Dimensional Array (2D)

A two-dimensional array stores elements in rows and columns (tabular form).
2D array data ko rows aur columns mein table ki tarah store karta hai.

#### ✅ Syntax

dataType arrayName[rows][columns];

#### 💻 Example
``cpp
int matrix[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
``
``cpp
Column
          0  1  2
Row 0     1  2  3
Row 1     4  5  6
``
First index → row

Second index → column


matrix[1][2] returns 6.
Pehla index row ko aur doosra column ko represent karta hai.

#### 📌 Real-Life Use Cases

Attendance sheet of students (rows = students, columns = days)

Marks sheet (rows = students, columns = subjects)

Chess board (rows and columns = board squares)

Seating layout of a theater


#### 🧠 Analogy

Excel sheet 📋:

Row = student

Column = subject

Cell = marks


Access = matrix[1][2] = second student’s third subject marks.

#### Traversal: Nested loops needed because we first select a row (outer loop), then iterate columns (inner loop).


---

### 3️⃣ Multi-Dimensional Array

Array with more than 2 dimensions.
2 se zyada brackets wale arrays ko multi-dimensional kehte hain.

#### ✅ Example

int arr[2][3][4];

#### 📌 Real-Life Use Cases

3D games → coordinates (x, y, z)

3D matrices in physics simulations

Image pixels (height × width × RGB color channels)


#### 🧠 Analogy

Think of a building with floors, rooms, and cabinets 🏢:

Floor = first index

Room = second index

Cabinet/item = third index



---

#### 🔁 Nested Loops in Multi-Dimensional Arrays

Outer loop → rows (or first dimension)

Inner loop → columns (or second dimension)


for(int i = 0; i < 2; i++) {        // rows
    for(int j = 0; j < 3; j++) {    // columns
        cout << matrix[i][j] << " ";
    }
    cout << endl;
}

Rule:

1D array → single loop

2D array → nested loop

Multi-dimensional array → multiple nested loops


Reason: Har element ko systematically access karne ke liye.


---

### 🔧 Common Array Operations

#### 1️⃣ Traversing

for(int i = 0; i < 5; i++)
    cout << marks[i] << " ";

Visiting each element one by one.
Har element ko ek ek karke visit karna.


---

#### 2️⃣ Searching

if(marks[i] == 90)
    cout << "Found";

Finding a specific value.
Kisi khas value ko dhoondhna.


---

#### 3️⃣ Updating

marks[2] = 100;

Changing an element value.
Kisi element ki value change karna.


---

#### 4️⃣ Summation

sum += marks[i];

Adding all elements.
Sab values ko add karna.


---

#### 5️⃣ Finding Maximum

Finding the largest element.
Sab se bari value identify karna.


---

### 📤 Passing Arrays to Functions

void printArray(int arr[], int size) {
    for(int i = 0; i < size; i++)
        cout << arr[i] << " ";
}

Arrays are passed by reference → original array changes if modified in function.

Efficient way to handle large data.



---
