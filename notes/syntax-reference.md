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

