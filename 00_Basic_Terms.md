# Basic Terms

## 1. Syntax vs Semantics

### Syntax
- The set of rules that defines the structure of statements in a language.  
  قواعد ہیں جو جملے یا کوڈ کی صحیح شکل بتاتے ہیں۔  
- Rules for writing code correctly so that it can be compiled or interpreted and executed.  
 کوڈ کو صحیح طریقے سے لکھنے کے اصول تاکہ اسے کمپائل یا انٹرپریٹ کر کے چلایا جا سکے۔ 
- Rules for forming grammatically correct sentences in a language.  
  زبان میں جملے درست بنانے کے قواعد۔  
**Example (Programming):**
  
  ```cpp
  int x = 10;  // Correct syntax in C++
  int = x 10;  // Incorrect syntax
  ```
صحیح: int x = 10;
غلط: int = x 10;

**Example (Natural Language):**
"I am learning English."
میں انگریزی سیکھ رہا ہوں۔
"Am I learning English?"
یہ جملہ صحیح گرامر کے باوجود غیر مناسب ہے۔


### Semantics

The meaning or behavior of a statement when executed.
کسی جملے یا کوڈ کا مطلب یا عمل۔

What the code actually does when it runs.
جب کوڈ چلتا ہے تو یہ اصل میں کیا کرتا ہے۔

The meaning conveyed by a sentence in a language.
جملے کا مطلب۔

**Example (Programming):**
```cpp
int x = 10;
int y = x / 0; // Syntax correct, but semantic error
```

کوڈ درست ہے مگر تقسیم بر صفر کی غلطی ہے۔
**Example (Natural Language):**
"I drank the book."
یہ جملہ گرامر کے لحاظ سے درست مگر مطلب میں بے معنی ہے۔



---

## 2. Instruction, Code, Program, File, Folder

### Instruction

A single command given to a computer to perform a specific task.
کمپیوٹر کو ایک کام کرنے کا ایک حکم/ہدایت ۔

**Example:**
```cpp
cout << "Hello World";        // One instruction to print text
```
یہ ایک حکم ہے جو پیغام دکھاتا ہے۔


**Code**

A single instruction or a collection of instructions written in a programming language.
ہدایات کا مجموعہ جو ایک ساتھ کام کرتا ہے۔

**Example:**
```cpp
int a = 5;
int b = 10;
int sum = a + b;
cout << sum;
```
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
یہ پروگرام دو نمبروں کا مجموعہ دکھاتا ہے
## **File**  
A **file** is the basic unit of storage on a computer. It can contain anything: text, program, media, etc.  
فائل کمپیوٹر پر اسٹوریج کی بنیادی اکائی ہے۔ یہ کچھ بھی رکھ سکتی ہے: ٹیکسٹ، کوڈ، میڈیا وغیرہ۔  

It can contain any type of data. The extension shows the type of data it contains.
کمپیوٹر پر ایک جگہ جہاں ڈیٹا یا کوڈ رکھا جاتا ہے۔ یہ کسی بھی قسم کا ڈیٹا رکھ سکتا ہے اور ایکسٹینشن ڈیٹا کی قسم بتاتا ہے۔

**Extensions for different types of files:**

**Extensions of files that store Text:** .txt, .md → متن

**Extensions of files that store Documents:** .doc, .docx, .pdf → دستاویزات

**Extensions of files that store Images:** .jpg, .png, .gif → تصاویر

**Extensions of files that store Audio:** .mp3, .wav → آواز

**Extensions of files that store Video:** .mp4, .avi → ویڈیو

**Extensions of files that store Programs:**   .cpp(extension for C++ files), .py(for python files), .java(for java files), .c(for c files)→ پروگرامنگ کوڈ

---

## **Module (Category of File)**  
A **module** is a **special category of file** that contains **code meant to be reused by other programs**.  
ماڈیول فائل کی ایک خاص قسم ہے جو دوسرے پروگرامز کے استعمال کے لیے کوڈ رکھتی ہے۔  

- **Contains:** Functions, classes, variables (Will be discussed in the next chapters)
  فنکشنز، کلاسز، ویری ایبلز  
- **Purpose:** Reusable piece of code that can be imported into other programs  
  دوبارہ استعمال ہونے والا کوڈ جسے دوسرے پروگرامز میں امپورٹ کیا جا سکتا ہے  
- **Examples:**  
  - `math.py` (Python standard module)  
  - `os` module in Python  

**Key Point:**  
- All modules are files, but not all files are modules.  
- تمام ماڈیولز فائلیں ہیں، لیکن ہر فائل ماڈیول نہیں ہوتی۔  

---

## **Folder / Directory**  
A **folder** or **directory** is a container used to organize files and other folders on a computer.  
فولڈر یا ڈائریکٹری ایک کنٹینر ہے جو فائلوں اور دیگر فولڈرز کو منظم کرنے کے لیے استعمال ہوتا ہے۔  

- **Contains:** Files and/or subfolders  
  فائلیں اور/یا ذیلی فولڈرز شامل ہوتے ہیں  
- **Purpose:** Helps organize and structure files for easier management  
  فائلوں کو آسانی سے منظم کرنے اور ترتیب دینے میں مدد کرتا ہے  
- **Examples:**  
  - Project/
       ├── main.cpp
       ├── utils.cpp
       └── README.md
پروجیکٹ فولڈر جس میں مختلف فائلیں موجود ہیں۔

here, **Project** is a folder/directory and it contains three files, **main.cpp,utild.cpp,and README.md.**

**Usage difference:**  
- **Directory:** Term more common in **command-line or programming contexts** (Linux, Windows CMD, Terminal).  
  ڈائریکٹری عام طور پر کمانڈ لائن یا پروگرامنگ ماحول میں استعمال ہوتی ہے۔  
- **Folder:** Term more common in **graphical user interfaces (GUIs)** like Windows Explorer or macOS Finder.  
  فولڈر زیادہ تر GUI میں استعمال ہوتا ہے۔  

---

## **Library**  
A **library** is a collection of **modules** (files containing reusable code) that a program can use to perform specific tasks.  
لائبریری ماڈیولز (کوڈ فائلوں) کا مجموعہ ہے جسے پروگرام مخصوص کام انجام دینے کے لیے استعمال کرتا ہے۔  

- **Contains:** Modules  
  ماڈیولز شامل ہوتے ہیں  
- **Purpose:** Provides ready-made functionality so programmers don’t have to write everything from scratch  
  تیار شدہ فنکشنلٹی فراہم کرتی ہے تاکہ پروگرامرز سب کچھ شروع سے نہ لکھیں  
- **Examples:**  
  - `NumPy` (Python) → contains multiple modules for math functions  
  - `React` (JavaScript) → contains modules for UI components  

**Key Point:**  
- Modules are the building blocks of a library.  
- ماڈیولز لائبریری کے بنیادی اجزاء ہیں۔  

---

## **Package**  
A **package** is a collection of related modules or libraries bundled together to provide additional functionality.  
پیکیج متعلقہ ماڈیولز یا لائبریریوں کا مجموعہ ہے جو اضافی فنکشنلٹی فراہم کرنے کے لیے ایک ساتھ پیک کیا جاتا ہے۔  

- **Contains:** Libraries or modules  
  لائبریریاں یا ماڈیولز شامل ہوتے ہیں  
- **Purpose:** Makes it easier to distribute and use related functionality  
  متعلقہ فنکشنلٹی کو آسانی سے استعمال اور تقسیم کرنے کے لیے  
- **Examples:**  
  - `NumPy` package in Python  
  - `Lodash` package in JavaScript  

**Relation:**  
- A package can contain multiple libraries.  
- پیکیج میں کئی لائبریریاں شامل ہو سکتی ہیں۔  

---

## **Software**  
**Software** is a collection of files, folders, libraries, packages, and modules that work together to perform tasks on a computer.  
سافٹ ویئر فائلوں، فولڈرز، لائبریریوں، پیکیجز اور ماڈیولز کا مجموعہ ہے جو کمپیوٹر پر کام انجام دینے کے لیے ایک ساتھ کام کرتے ہیں۔  

### **Two common Types of Software**  

1. **System Software**  (Will be discussed in depth in the Operating System Course)
   - Manages hardware and provides a platform for running application software.  
     ہارڈویئر کو منظم کرتا ہے اور ایپلیکیشن سافٹ ویئر چلانے کے لیے پلیٹ فارم فراہم کرتا ہے۔  
   - **Examples:** Windows, Linux, macOS, Antivirus tools  

2. **Application Software**  (Will be discussed in the Operating System Course)
   - Designed for end-users to perform specific tasks.  
     صارفین کے مخصوص کام انجام دینے کے لیے تیار کیا گیا سافٹ ویئر  
   - **Examples:** Google Chrome, Microsoft Office, WhatsApp  

#
---

## **Framework**  
A framework provides a blueprint or skeleton for building software applications. It gives developers a structured foundation, standard rules, and reusable components to follow.
فریم ورک سافٹ ویئر ایپلیکیشن بنانے کے لیے ایک خاکہ یا اسکلیٹن فراہم کرتا ہے۔ یہ ڈویلپرز کو ایک منظم بنیاد، معیاری قوانین، اور دوبارہ استعمال ہونے والے اجزاء دیتا ہے۔

Contains: Libraries, packages, tools, templates, predefined rules
لائبریریاں، پیکیجز، ٹولز، ٹیمپلیٹس، اور پہلے سے طے شدہ قوانین

Purpose: Provides a ready-made structure and standard practices for building applications
ایپلیکیشن بنانے کے لیے تیار شدہ ڈھانچہ اور معیاری طریقے فراہم کرتا ہے

- **Examples:**  
  - `Django` (Python)  
  - `React` (JavaScript)  

**Relation:**  
- A framework uses libraries and packages internally and dictates how software is built.  
- فریم ورک اندرونی طور پر لائبریریاں اور پیکیجز استعمال کرتا ہے اور سافٹ ویئر کی ساخت متعین کرتا ہے۔ 

---


