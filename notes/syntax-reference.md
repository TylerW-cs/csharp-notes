## Console Output

|     Code     |
|  Explanation |
| Example Code |
|    Output    |

// Console.WriteLine() //
Prints text and moves to a new line.

Console.WriteLine("Hello");
Console.WriteLine("World");

Hello
World

// Console.Write() //
Prints text but stays on the same line.

Console.Write("Hello ");
Console.Write("World");

Hello World

// Console.ReadLine() //
Reads a line of text that the user types and returns it as a string. It waits for the user to press Enter, then gives you everything they typed.

string input = Console.ReadLine();
Console.WriteLine(input);

// int //

int age = 25;

// bool //

bool isActive = true;

// double //

double price = 9.99;

// string //

string name = "Dave"

// dot notation //
When constants (or any static members) are defined in a separate class, you access them using the class name followed by a dot and the member name. This is called dot notation. 
ClassName.MemberName syntax.

// In MathConstants class:
public static class MathConstants
{
    public const double Pi = 3.14159;
    public const int DaysInWeek = 7;
}

// To use these constants from another class:
double circleConstant = MathConstants.Pi;     // Returns 3.14159
int days = MathConstants.DaysInWeek;          // Returns 7

// decimal //
The decimal type is a 128-bit precise decimal number, perfect for financial calculations where accuracy matters. Unlike double, decimals avoid floating-point rounding errors. The "m" suffix distinguishes it from a double.

decimal price = 19.99m;

// decimal.Add() //

decimal.Add(10.50m, 3.25m)

13.75

// decimal.Subtract() //

decimal.Subtract(10.50m, 3.25m)

7.25

// decimal.Multiply() //

decimal.Multiply(10.00m, 2m)

20.00

// decimal.Divide() //

decimal.Divide(10.00m, 4m)

2.50

// verbatim strings //
A verbatim string literal starts with @ before the opening quote. It tells C# to treat the string exactly as written, ignoring escape sequences like \n or \t. This is especially handy for Windows file paths, where every backslash would otherwise need to be doubled.

string verbatim = @"D:\Projects\Notes\todo.md";

D:\Projects\Notes\todo.md

// \n //
Escape sequences are special character combinations that represent characters which cannot be typed directly in a string, like newlines, tabs, or quote marks. This is for a new line.

Console.WriteLine("Line 1\nLine 2");

Line 1
Line 2

// \t //
Escape sequences are special character combinations that represent characters which cannot be typed directly in a string, like newlines, tabs, or quote marks. This is for a tab/indent.

Console.WriteLine("Name:\tJohn");

    John

// \\ //
Escape sequences are special character combinations that represent characters which cannot be typed directly in a string, like newlines, tabs, or quote marks. This is for a backslash.

Console.WriteLine("C:\\Program Files\\App");

C:\Program Files\App

// \" //
Escape sequences are special character combinations that represent characters which cannot be typed directly in a string, like newlines, tabs, or quote marks. This is for a double quote.

Console.WriteLine("She said \"Hello!\"");

She said "Hello!"

// String Interpolation //
String interpolation lets you embed variables and expressions directly inside strings using the $ prefix and curly braces {}.

string message2 = $"Hello, {name}! Your score is {score}.";

Hello, Tyler! Your score is 99.

// char //
A char represents a single Unicode character. While strings hold multiple characters, a char holds exactly one. Use char when working with individual characters from strings or keyboard input.

char letter = 'A';

A

// char.IsLetter() //

char.IsLetter('A');

True

// char.IsDigit() //

char.IsDigit('5');

True

// char.IsUpper() //

chat.IsUpper('a');

False

// char.IsLower() //

char.IsLower('a');

True

// char.ToUpper() //

char.ToUpper('a');

A

// char.ToLower() //

char.ToLower('A');

a

// && //
AND - Both must be true.

// || //
OR - At least one must be true.

// ! //
NOT - Inverts the value.

!true

false

// float //
A float is a 32-bit floating-point number used for storing decimal values when you need to save memory and don't require high precision.

float temperature = 98.6f;

Without 'f', the compiler treats it as a double (error!).

// + //
The + operator adds two values together. It's one of the most fundamental arithmetic operators in C#.

int sum = 5 + 3;

8

// - //
The subtraction operator (-) calculates the difference between two numbers. It subtracts the right operand from the left operand.

int sum = 5 - 3;

2

// * //
The multiplication operator * multiplies two numbers together. It's used whenever you need to calculate products, areas, or scale values.

int sum = 5 * 3;

15

// / //
The division operator / divides one number by another. Unlike integer division, using double preserves decimal precision.

int sum = 10 / 2;

5

// % //
The modulo operator (%) returns the remainder after integer division. It's essential for tasks like checking even/odd numbers, cycling through values, and wrapping indices.

int remainder = 17 % 5;

2

// Arithmetic Compound Operators //

int x = 20;

x += 5;
x -= 3;
x *= 2;
x /= 4;

25
22
44
11