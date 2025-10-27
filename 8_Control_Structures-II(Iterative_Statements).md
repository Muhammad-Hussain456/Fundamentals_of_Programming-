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

### 📘 Semantic Meaning  
Executes the loop block a fixed number of times. Initialization runs once, then the condition is checked before each iteration. The update runs after each iteration.

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

### 📘 Semantic Meaning  
Executes the loop block **as long as** the condition is true. The condition is checked **before** each iteration.

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

### 📘 Semantic Meaning  
Executes the loop block **at least once**, then repeats **as long as** the condition is true. The condition is checked **after** each iteration.

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

### 📘 Semantic Meaning  
A loop inside another loop. The inner loop completes all its iterations for each iteration of the outer loop.

### 💡 Example
```cpp
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 2; j++) {
        cout << "i = " << i << ", j = " << j << endl;
    }
}
```

---
