1. Program Structure

A C++ program consists of a set of instructions executed sequentially. Every program must have a main() function where execution begins.

C++ پروگرام ایک سلسلہ وار ہدایات پر مشتمل ہوتا ہے جو ایک کے بعد ایک execute ہوتی ہیں۔ ہر پروگرام میں main() فنکشن ہونا ضروری ہے، جہاں سے execution شروع ہوتی ہے۔

#include <iostream>   // Input/Output library شامل کرو
using namespace std;  // Standard names براہ راست استعمال کرو

int main() {
    // Code goes here
    return 0;
}

First Two Lines Explained

1. #include <iostream>

Includes Input/Output library so cin and cout can be used.

Input/Output کے لیے library شامل کرو تاکہ cin اور cout استعمال ہو سکیں۔



2. using namespace std;

Allows using standard C++ names without std:: prefix.

Standard names براہ راست استعمال کرو، std:: لکھنے کی ضرورت نہیں۔





---

2. Streams

Streams are paths through which data flows into (input) or out of (output) a program.

Streams ایسے راستے ہیں جن کے ذریعے ڈیٹا پروگرام میں آتا (input) یا پروگرام سے باہر جاتا (output) ہے۔

cin → input stream

cout → output stream



---

3. Variables

Variables are named memory locations used to store data. Each variable has a data type defining what kind of data it can store.

Variables memory میں نامزد جگہیں ہیں جہاں ڈیٹا محفوظ کیا جاتا ہے۔ ہر variable کا data type ہوتا ہے جو بتاتا ہے کہ یہ کس قسم کا ڈیٹا رکھ سکتا ہے۔

int age;
float height;
char grade;
bool isPassed;


---

4. Declaration and Initialization

Declaration tells the compiler about variable name and type.

Initialization assigns an initial value to the variable.


Declaration کمپائلر کو variable کا نام اور type بتانے کا عمل ہے۔
Initialization وہ عمل ہے جس میں variable کو declare کرتے وقت initial value دی جاتی ہے۔

int age;        // declaration
int age = 25;   // declaration with initialization


---

5. Assignments

Assignment gives a value to a variable using = operator.

Assignment وہ عمل ہے جس میں variable کو = operator کے ذریعے value دی جاتی ہے۔

age = 30;
height = 6.1;
grade = 'B';
isPassed = true;


---

6. Data Types, What They Store, and Range

Data types define what type of data a variable can store. Range tells the limits of that type.

Data Type	Storage	What It Stores (Examples)	Range (32-bit)	Purpose

int	4 bytes	Whole numbers (e.g., 10, -5, 200)	-2,147,483,648 to 2,147,483,647	Counting, whole numbers
short int	2 bytes	Small whole numbers (e.g., -300, 500)	-32,768 to 32,767	Small numbers
long int	4/8 bytes	Large whole numbers (e.g., 2000000000)	Larger numbers	Large whole numbers
float	4 bytes	Fractional numbers (e.g., 5.9, -3.14)	3.4e-38 to 3.4e+38	Numbers with decimals
double	8 bytes	High precision fractional numbers (e.g., 3.14159265)	1.7e-308 to 1.7e+308	More precise decimals
long double	10/12/16 bytes	Very large or very small fractional numbers	Very large fractional numbers	High precision calculations
char	1 byte	Single characters (e.g., 'A', 'b', '%')	-128 to 127 (signed) / 0 to 255 (unsigned)	Characters, symbols
bool	1 byte	True/False values (true, false)	0 or 1	Conditional checks, flags


Purpose of Range:
Range ensures that the value stored fits within the data type limits to avoid overflow or incorrect results.

Example:

int smallNumber = 2000000000;   // Correct
int tooBig = 3000000000;        // Incorrect, out of range
float pi = 3.14159;             // Fractional number
char letter = 'A';              // Single character
bool passed = true;             // True or False


---

7. Input/Output Operations

Input operations let the program receive data from the user, output displays it on the screen.

Input operations پروگرام کو صارف سے ڈیٹا حاصل کرنے دیتی ہیں، output operations اسکرین پر دکھاتی ہیں۔

int age;
cout << "Enter your age: ";
cin >> age;
cout << "You are " << age << " years old.";


---

8. Type Conversions

Type conversion converts a value from one data type to another.

Implicit conversion happens automatically.

Explicit conversion / type casting is done manually.


int a = 5;
float b = a;      // implicit
float x = 5.9;
int y = (int)x;   // explicit


---

9. Example Problem

Create variables for student marks, height, grade, and pass status. Assign values and display them.

ایک variable marks, height, grade، اور pass status کے لیے بنائیں، values assign کریں، اور screen پر دکھائیں۔

#include <iostream>
using namespace std;

int main() {
    int marks = 85;
    float height = 5.9;
    char grade = 'A';
    bool passed = true;

    cout << "Marks: " << marks << endl;
    cout << "Height: " << height << endl;
    cout << "Grade: " << grade << endl;
    cout << "Passed: " << passed << endl;

    return 0;
}


---
