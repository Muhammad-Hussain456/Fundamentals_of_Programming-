# 📘 Chapter 1 – Processing a C++ Program

## What is C++?
- C++ is a **general-purpose, high-level, object-oriented programming language**.  
- Developed by **Bjarne Stroustrup in 1979** as an extension of C.  
- Used in system programming, game development, embedded systems, and large-scale applications.  

### Why C++?
- Provides both **procedural** and **object-oriented** programming features.  
- Offers high performance, control, and flexibility.  
- Commonly used in industries where performance is critical.  

---

## Steps in Processing a C++ Program

1. **Editor**
   - You write code in a text editor or IDE (Integrated Development Environment).  
   Example: Visual Studio, Code::Blocks, Dev-C++, VS Code.

2. **Preprocessor**
   - Handles `#include` files, macros, and preprocessor directives.  
   - Expands the code before compilation.

3. **Compiler**
   - Converts high-level C++ code into **assembly or machine code**.  
   - Detects syntax errors.

4. **Linker**
   - Combines compiled code with libraries.  
   - Produces an **executable file (.exe)**.

5. **Loader**
   - Loads the executable file into memory for execution.  

6. **Execution**
   - The CPU runs the machine instructions and gives output.  

---

## Example Program

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!";
    return 0;
}
```

### Processing Flow:
- **Editor** → Code written.  
- **Preprocessor** → Expands `#include <iostream>`.  
- **Compiler** → Translates into machine code.  
- **Linker** → Links with standard C++ library.  
- **Loader** → Loads program into memory.  
- **Execution** → Displays: `Hello, World!`  

---

## Summary
- C++ is a high-level, object-oriented language.  
- A C++ program passes through stages: **Editor → Preprocessor → Compiler → Linker → Loader → Execution**.  
- Each stage plays a key role in transforming source code into machine-executable instructions.  
