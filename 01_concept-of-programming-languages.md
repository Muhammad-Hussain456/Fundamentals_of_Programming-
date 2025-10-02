# 📘 Concept of Programming Languages

## Language – Definition
A language is a system of communication that uses symbols, sounds, or signs to convey ideas, share information, and enable understanding between people or systems.

## Types of Languages
1. **Natural Languages** – Human languages that develop naturally over time.  
   Examples: English, Urdu, Arabic.  
   Used for communication among people.

2. **Formal Languages** – Artificially created languages with precise syntax and rules.  
   Examples: Mathematics, Logic notation, Programming languages.  
   Used in science, computing, and mathematics to avoid ambiguity.

3. **Sign Languages** – Visual-manual languages used primarily by deaf communities.  
   Example: American Sign Language (ASL).


---

## Programming:
Programming is a process/method of problem solving

## What is a Programming Language?
A programming language is a **formal language** used to instruct computers to solve a problem.  
It acts as a medium between humans and computers:

- Programmers write instructions in languages like C, C++, Java, Python.  
- A **translator** converts them into **machine language** (binary).  
- The **computer** executes the machine language.  

---

## Types of Programming Languages
1. **Low-Level Languages**
   - Machine Language – **Machine Language** – The most basic language understood directly by computers. Consists of binary code (0s and 1s)..  
   - Assembly Language – Symbolic mnemonics for machine instructions.

3. **High-Level Languages**
   - Procedural Languages (e.g., C, Pascal, FORTRAN, COBOL)  
   - Object-Oriented Languages (e.g., Java, C++, Python)  
   - Functional Languages (e.g., Lisp, Haskell)  
   - Scripting Languages (e.g., JavaScript, PHP, Python)  
   - Markup/Query Languages (e.g., HTML, SQL)

---

## Why Do We Use Programming Languages?
- Computers only understand binary code.  
- Programming languages make communication easier.  
- Translators (compilers, interpreters, assemblers) convert source code to machine code.

### Translators
- **Compiler** – Translates entire high-level code to machine code (C, C++, Java).  
- **Interpreter** – Translates line by line (Python).  
- **Assembler** – Converts assembly to machine code (binary).

---

To execute/run a program:
#### Linker: 
Combines object program with other programs provided by the SDK to create executable code
#### Loader: 
Loads executable program into main memory
The last step is to execute the program


### Software Development Kit (SDK)

SDK (Software Development Kit):
A set of headers, libraries, and tools provided by the platform (Windows, Linux, etc.) so programs can run. It does not depend on language (C++, Python, Java) or editor — only on the platform.

On Windows → the Windows SDK comes built-in with Visual Studio (so no need to install separately).

But if you use VS Code, Dev-C++, Eclipse, PyCharm, IntelliJ, etc., then you must install the SDK separately.


On Linux → standard libraries (glibc, libstdc++, etc.) are already part of the system, so normally no extra SDK installation.

On Android -> 


👉 In short: SDK = extra files and tools given by the platform your program is targeting.


### IDEs (Integrated Development Environments)

An IDE is a software application that helps programmers write, debug, and run programs easily.
While an SDK is a sep
arate set of tools, some IDEs automatically install and manage the correct SDKs for you, creating a single, integrated package.

IDES usually includes:

Code Editor – for writing code.

Compiler/Interpreter – for translating code.

Debugger – for finding and fixing errors.

Execution Environment – to run programs.

Examples: Code::Blocks, Dev-C++, Visual Studio, Eclipse, PyCharm, VS Code.

## Summary
- A language is a communication system.  
- Programming languages are formal languages designed to instruct computers.  
- They are classified into low-level and high-level languages.  
- Translators (compiler, interpreter, assembler) are needed for execution.  
