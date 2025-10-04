C++ Fundamentals

A C++ program consists of a set of instructions executed sequentially.
سی پلس پلس پروگرام ایک سلسلہ وار ہدایات پر مشتمل ہوتا ہے جو ایک کے بعد ایک عمل میں آتی ہیں۔

Every program must have a main() function where execution begins.
ہر پروگرام میں main() فنکشن ہونا ضروری ہے، جہاں سے عمل شروع ہوتا ہے۔

#include <iostream>   // Input/Output library included
using namespace std;  // Allows direct use of standard names

int main() {
    // Code goes here
    return 0;
}

The first line includes the Input/Output library so cin and cout can be used.
پہلی لائن انپٹ/آؤٹ پٹ لائبریری شامل کرتی ہے تاکہ سن اور کاوٹ استعمال ہو سکیں۔

Input refers to receiving data from the user.
انپٹ کا مطلب ہے صارف سے ڈیٹا لینا۔

Output refers to displaying data on the screen.
آؤٹ پٹ کا مطلب ہے اسکرین پر ڈیٹا دکھانا۔

Without including iostream, you cannot use cin or cout in your program.
iostrem شامل کیے بغیر آپ اپنے پروگرام میں سن یا کاوٹ استعمال نہیں کر سکتے۔

The second line allows using standard C++ names without std:: prefix.
دوسری لائن سٹینڈرڈ نام براہ راست استعمال کرنے کی اجازت دیتی ہے، بغیر std:: کے۔


---

Variables

Variables are named memory locations used to store data.
ویری ایبل میموری میں نامزد جگہیں ہیں جہاں ڈیٹا محفوظ کیا جاتا ہے۔

Each variable has a data type defining what kind of data it can store.
ہر ویری ایبل کا ڈیٹا ٹائپ ہوتا ہے جو بتاتا ہے کہ وہ کس قسم کا ڈیٹا رکھ سکتا ہے۔

int age;
float height;
char grade;
bool isPassed;


---

Declaration and Initialization

Declaration tells the compiler about a variable's name and type.
اعلان کمپائلر کو ویری ایبل کا نام اور قسم بتانے کا عمل ہے۔

Initialization assigns an initial value to the variable.
ابتدائی قیمت دینا وہ عمل ہے جس میں ویری ایبل کو declare کرتے وقت ابتدائی value دی جاتی ہے۔

int age;        // declaration
int age = 25;   // declaration with initialization


---

Assignments

Assignment gives a value to a variable using the = operator.
ویلیو دینا وہ عمل ہے جس میں ویری ایبل کو = آپریٹر کے ذریعے ویلیو دی جاتی ہے۔

age = 30;
height = 6.1;
grade = 'B';
isPassed = true;


---

Data Types, What They Store, and Range

Data types define what type of data a variable can store.
ڈیٹا ٹائپ بتاتا ہے کہ ویری ایبل کس قسم کا ڈیٹا رکھ سکتا ہے۔

Range tells the limits of that type.
حد یہ بتاتی ہے کہ ویری ایبل میں کس حد تک کی ویلیو محفوظ کی جا سکتی ہے۔

Data Type	Storage	What It Stores (Examples)	Range (32-bit)	Purpose

int	4 bytes	Whole numbers (10, -5, 200)	-2,147,483,648 to 2,147,483,647	Counting, whole numbers
short int	2 bytes	Small whole numbers (-300, 500)	-32,768 to 32,767	Small numbers
long int	4/8 bytes	Large whole numbers (2000000000)	Larger numbers (depends on system)	Large whole numbers
float	4 bytes	Fractional numbers (5.9, -3.14)	3.4e-38 to 3.4e+38	Numbers with decimals
double	8 bytes	High precision fractional numbers (3.14159265)	1.7e-308 to 1.7e+308	More precise decimals
long double	10/12/16 bytes	Very large or very small fractional numbers	Very large fractional numbers	High precision calculations
char	1 byte	Single characters ('A', 'b', '%')	-128 to 127 / 0 to 255	Characters, symbols
bool	1 byte	True/False values (true, false)	0 or 1	Conditional checks, flags


Range ensures that the value stored fits within the data type limits to avoid overflow or incorrect results.
حد اس بات کو یقینی بناتی ہے کہ محفوظ شدہ ویلیو ڈیٹا ٹائپ کی حد میں فٹ ہو تاکہ overflow یا غلط نتائج نہ ہوں۔

Example

int smallNumber = 2000000000;   // Correct
int tooBig = 3000000000;        // Incorrect, out of range
float pi = 3.14159;             // Fractional number
char letter = 'A';              // Single character
bool passed = true;             // True or False

چھوٹا نمبر صحیح ہے۔
بہت بڑا نمبر غلط ہے، حد سے زیادہ۔
پی اعشاریہ نمبر ہے۔
حرف ایک ہے۔
پاس ہوا صحیح یا غلط ہے۔


---

Input/Output Operations

Input operations let the program receive data from the user.
انپٹ آپریشن پروگرام کو صارف سے ڈیٹا حاصل کرنے دیتی ہے۔

Output operations display data on the screen.
آؤٹ پٹ آپریشن اسکرین پر ڈیٹا دکھاتی ہے۔

int age;
cout << "Enter your age: ";
cin >> age;
cout << "You are " << age << " years old.";


---

Type Conversions

Type conversion converts a value from one data type to another.
ڈیٹا کی قسم تبدیل کرنا وہ عمل ہے جس میں ایک قسم کی ویلیو کو دوسری قسم میں بدلا جاتا ہے۔

Implicit conversion happens automatically.
خودکار تبدیلی خود بخود ہوتی ہے۔

Explicit conversion / type casting is done manually.
واضح تبدیلی پروگرامر خود کرتا ہے۔

int a = 5;
float b = a;      // implicit
float x = 5.9;
int y = (int)x;   // explicit


---

Example Problem

Create variables for student marks, height, grade, and pass status.
ایک ویری ایبل نمبرز، قد، گریڈ اور پاس کی حالت کے لیے بنائیں۔

Assign values and display them.
ویلیو مقرر کریں اور اسکرین پر دکھائیں۔

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
