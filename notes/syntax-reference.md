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

// Incremental and Decremental Operators //

| Prefix |

int x = 5;
int result = x++;  -> result = 5, x = 6 (returns original, then changes)

int y = 10;
int result2 = y--; -> result2 = 10, y = 9 (returns original, then changes)

| Postfix |

int x = 5;
int result = ++x;  -> result = 6, x = 6 (changes first, then returns)

int y = 10;
int result2 = --y; -> result2 = 9, y = 9 (changes first, then returns)

// Comparison Operators //

| == |
Equal to.

5 == 5 -> true

| != |
Not equal to.

5 != 3 -> true

| > |
Greater than.

7 > 5 -> true

| < |
Less than.

3 < 5 -> true

| >= |
Greater or equal.

5 >= 5 -> true

| <= |
Less or equal.

5 <= 5 -> true

// Logical AND operator //

bool result1 = true && true;   -> True - both are true
bool result2 = true && false;  -> False - second is false
bool result3 = false && true;  -> False - first is false
bool result4 = false && false; -> False - both are false

// Logical OR operator //

bool result1 = true || false;   -> true (first is true)
bool result2 = false || true;   -> true (second is true)
bool result3 = false || false;  -> false (neither is true)
bool result4 = true || true;    -> true (both are true)

// Logical NOT operator //

bool hasErrors = true;
bool succeeded = !hasErrors;   -> succeeded is false
-> hasErrors is still true - it was not modified

!booleanValue          // negates a single value
!(expression)          // negates the whole expression inside the parentheses

| Logical Operator Useful Reference |

!a -> Not a -> false
!a && !b -> neither a nor b -> false
!a || !b -> not both a and b -> true
!(a && b) -> not (a and b) -> true

// if Statement //

if (condition)
{
    -> Code runs only when condition is true
}

//

// if-else Statement //

if (condition)
{
    -> Runs when condition is true
}
else
{
    -> Runs when condition is false
}

// else-if Statement //

if (condition1)
{
    -> Runs if condition1 is true
}
else if (condition2)
{
    -> Runs if condition1 is false AND condition2 is true
}
else if (condition3)
{
    -> Runs if both above are false AND condition3 is true
}
else
{
    -> Runs if ALL conditions above are false
}

// Logical Patterns //
C# pattern matching allows you to combine conditions using pattern combinators. These make your code more readable when comparing against compile-time constants.

if (number is 1 or 0)
        {
            return "edge";
        }
        else if (number is >= 2 and <=9)
        {
            return "small positive";
        }
        else if (number is not > 0)
        {
            return "non-positive";
        }
        else if (number is >= 10 and <= 100)
        {
            return "medium";
        }
        else
        {
            return "large";
        }

// Switch Statement //
A switch statement compares a single value against a list of constant options and runs the matching branch. It is the idiomatic choice when one variable can take many known values (a menu choice, a status code, a month number), because it reads more clearly than a long chain of else if comparisons.

The value in the parentheses is evaluated once, then compared top-to-bottom against each case label. When a label matches, the statements under it run until the branch is ended by break (leave the switch) or return (leave the whole method). If nothing matches, the default branch runs — and if there is no default, the switch simply does nothing.

switch (dayNumber)
        {
            case 1:
                return "Monday";
                break;
            case 2:
                return "Tuesday";
                break;
            case 3:
                return "Wednesday";
                break;
            case 4:
                return "Thursday";
                break;
            case 5:
                return "Friday";
                break;
            case 6:
                return "Saturday";
                break;
            case 7:
                return "Sunday";
                break;
            default:
                return "Invalid day";
                break;

        }

// Switch Expressions //
Switch expressions are a concise, expression-based alternative to switch statements. They return a value directly and use the => arrow syntax.

var result = value switch
{
    pattern1 => result1,
    pattern2 => result2,
    _ => defaultResult  // discard pattern (default)
};

-> Traditional switch statement (verbose)
string GetGrade(int score)
{
    switch (score)
    {
        case 10:
            return "A+";
        case 9:
            return "A";
        default:
            return "B";
    }
}

-> Switch expression (concise)
return score switch
{
    10 => "A+",
    9 => "A",
    _ => "B"
};

// Ternary Operator //

-> Instead of this:
string result;
if (score >= 50)
    result = "Pass";
else
    result = "Fail";

-> Write this:
string result = score >= 50 ? "Pass" : "Fail";

-> More examples:
int max = a > b ? a : b;
bool isEven = number % 2 == 0 ? true : false;
string greeting = hour < 12 ? "Good morning" : "Good afternoon";

-> Ternary - concise for simple assignments
string status = isActive ? "Online" : "Offline";

-> If-Else - better for multiple operations
if (isActive)
{
    status = "Online";
    LogActivity();
}
else
{
    status = "Offline";
    SendNotification();
}

