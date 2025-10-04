# Basic Terms

## 1. Syntax vs Semantics

### Syntax
- The set of rules that defines the structure of statements in a language.  
  قواعد ہیں جو جملے یا کوڈ کی صحیح شکل بتاتے ہیں۔  
- Rules for writing code correctly so that it can be compiled or interpreted.  
  کوڈ کو صحیح لکھنے کے قواعد تاکہ یہ چل سکے۔  
- Rules for forming grammatically correct sentences in a language.  
  زبان میں جملے درست بنانے کے قواعد۔  
**Example (Programming):** 
  ```cpp
  int x = 10;  // Correct syntax in C++
  int = x 10;  // Incorrect syntax

صحیح: int x = 10;
غلط: int = x 10;

**Example (Natural Language):**
"I am learning English."
میں انگریزی سیکھ رہا ہوں۔
"Am I learning English?"
یہ جملہ صحیح گرامر کے باوجود غیر مناسب ہے۔


### Semantics

The meaning or behavior of a statement when executed or interpreted.
کسی جملے یا کوڈ کا مطلب یا عمل۔

What the code actually does when it runs.
جب کوڈ چلتا ہے تو یہ اصل میں کیا کرتا ہے۔

The meaning conveyed by a sentence in a language.
جملے کا مطلب۔

**Example (Programming):**

int x = 10;
int y = x / 0; // Syntax correct, but semantic error

کوڈ درست ہے مگر تقسیم بر صفر کی غلطی ہے۔

**Example (Natural Language):**
"I drank the book."
یہ جملہ گرامر کے لحاظ سے درست مگر مطلب میں بے معنی ہے۔



---

## 2. Instruction, Code, Program, File, Folder

### Instruction

A single command given to a computer to perform a specific task.
کمپیوٹر کو ایک کام کرنے کا ایک حکم۔

**Example:**

cout << "Hello World"; // One instruction to print text

یہ ایک حکم ہے جو پیغام دکھاتا ہے۔


**Code**

A collection of instructions written in a programming language.
ہدایات کا مجموعہ جو ایک ساتھ کام کرتا ہے۔

**Example:**

int a = 5;
int b = 10;
int sum = a + b;
cout << sum;

یہ ہدایات کا مجموعہ ہے جو جمع دکھاتا ہے۔


### Program

A complete set of code that performs a specific task when executed.
مکمل کوڈ جو چلانے پر ایک کام کرتا ہے۔

**Example:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int a, b;
    cout << "Enter two numbers: ";
    cin >> a >> b;
    cout << "Sum = " << a + b;
    return 0;
}
```
یہ پروگرام دو نمبروں کا مجموعہ دکھاتا ہے۔


### File

A storage unit on a computer that contains data or code. It can contain any type of data. The extension shows the type of data it contains.
کمپیوٹر پر ایک جگہ جہاں ڈیٹا یا کوڈ رکھا جاتا ہے۔ یہ کسی بھی قسم کا ڈیٹا رکھ سکتا ہے اور ایکسٹینشن ڈیٹا کی قسم بتاتا ہے۔

**Extensions for different types of files:**

**Text:** .txt, .md → متن

**Documents:** .doc, .docx, .pdf → دستاویزات

**Images:** .jpg, .png, .gif → تصاویر

**Audio:** .mp3, .wav → آواز

**Video:** .mp4, .avi → ویڈیو

**Programming Code:** .cpp(extension for C++ files), .py(for python files), .java(for java files), .c(for c files)→ پروگرامنگ کوڈ



### Folder (Directory)

A container used to organize multiple files and subfolders.
ایک جگہ جہاں کئی فائلیں اور سب فولڈرز رکھے جاتے ہیں۔

**Example:**

Project/
  ├── main.cpp
  ├── utils.cpp
  └── README.md
پروجیکٹ فولڈر جس میں مختلف فائلیں موجود ہیں۔

here, **Project** is a folder and it contains three files, **main.cpp,utild.cpp,and README.md.**


---


