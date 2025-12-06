# 🔁 Control Structures II (C++): Iterative Statements / Loops

Loops in C++ allow a program to **repeat a block of code** multiple times based on a condition or range.

---

## 🔄 `for` Loop

### ✅ Syntax
```cpp
for (initialization; condition; update) {
    // code block to execute
}
```

### 📘 Semantic  
Executes the loop block a fixed number of times.  
- Initialization runs once.  
- Condition is checked before each iteration.  
- Update runs after each iteration.  

### 💡 Example
```cpp
for (int i = 0; i < 5; i++) {
    cout << "Iteration " << i << endl;
}
```

---

## 🔁 `while` Loop

### ✅ Syntax
```cpp
while (condition) {
    // code block to execute
}
```

### 📘 Semantic  
Executes the loop block **as long as** the condition is true.  
Condition is checked **before** each iteration.

### 💡 Example
```cpp
int count = 0;
while (count < 5) {
    cout << "Count: " << count << endl;
    count++;
}
```

---

## 🔁 `do-while` Loop

### ✅ Syntax
```cpp
do {
    // code block to execute
} while (condition);
```

### 📘 Semantic  
Executes the loop block **at least once**, then repeats **as long as** the condition is true.  
Condition is checked **after** each iteration.

### 💡 Example
```cpp
int count = 0;
do {
    cout << "Count: " << count << endl;
    count++;
} while (count < 5);
```

---

## 🔁 Nested Loops

### ✅ Syntax
```cpp
for (int i = 0; i < outerLimit; i++) {
    for (int j = 0; j < innerLimit; j++) {
        // nested loop block
    }
}
```

### 📘 Semantic  
A loop inside another loop.  
- The **outer loop** controls rows (or higher dimension).  
- The **inner loop** usually controls columns and completes all its iterations for each iteration of the outer loop.  

### 💡 Example
```cpp
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 2; j++) {
        cout << "i = " << i << ", j = " << j << endl;
    }
}
```

---

## 🟢 Single Loop vs 🔁 Nested Loops

| Loop Type       | Rows | Columns | Example Use Case |
|-----------------|------|---------|------------------|
| Single Loop     | ✅   | ❌ (only 1) | Printing roll numbers in a single column |
| Nested Loops    | ✅   | ✅ (2+)   | Printing seating arrangement in rows × columns |

---

## 🔁 Nested Loop Examples

### 1️⃣ Nested `for` Loop → Classroom Seats (3 rows × 4 columns)
```cpp
for(int row = 1; row <= 3; row++) {
    for(int col = 1; col <= 4; col++) {
        cout << "Row " << row << ", Seat " << col << endl;
    }
}
```

### 2️⃣ Nested `while` Loop → Hotel Floors & Rooms (2 floors × 3 rooms)
```cpp
int floor = 1;
while(floor <= 2) {
    int room = 1;
    while(room <= 3) {
        cout << "Floor " << floor << ", Room " << room << endl;
        room++;
    }
    floor++;
}
```

### 3️⃣ Nested `do-while` Loop → Students & Subjects
```cpp
string students[] = {"Ali", "Hussain"};
string subjects[] = {"Math", "English"};

int i = 0;
do {
    int j = 0;
    do {
        cout << students[i] << " → " << subjects[j] << endl;
        j++;
    } while(j < 2);
    i++;
} while(i < 2);
```

---

## ✨ Key Takeaway
- **Single loop → one dimension (rows OR columns).**  
- **Nested loops → two dimensions (rows AND columns).**  
This distinction helps in modeling real-world structures like seating charts, hotel floors, or student-subject mappings.
```

