# Terminology

Variable = Variables are containers that store data values. You declare a variable by specifying its type and giving it a name.

int = Integer - it is a data type that is a whole number. For example: 42

double = Decimal numbers - it is a data type that is a decimal number. Doubles don't avoid floating-point rounding errors. For example: 3.14

float = A float is a 32-bit floating-point number used for storing decimal values when you need to save memory and don't require high precision.

decimal = Precise decimal number - perfect for financial calculations where accuracy matters. Decimals avoid floating-point rounding errors.

bool = A bool (short for Boolean) represents a logical value that can only be true or false. Booleans are essential for making decisions in your code.

string = String - it is a data type that is Text/Characters. For example: "Hello"

Class = A container that groups related code together.

Method = A method is a reusable block of code that performs a specific task. Think of it like a recipe - you give it ingredients (inputs), it follows instructions, and gives you a result (output).

// = Comments are notes in your code that the computer ignores. They help you and other programmers understand what the code does.

/* = Start of a multi-line comment. This lets you write comments that span multiple lines. Use them to explain complex logic, or temporarily disable blocks of code.

*/ = End of a multi-line comment. This lets you write comments that span multiple lines. Use them to explain complex logic, or temporarily disable blocks of code.

Return = Exits the method immediately - no code after return runs. Sends a value back to the caller - the value becomes the result of the method call.

Const = Constant is a value that cannot change after it's defined. Use the const keyword to declare values that remain fixed throughout your program.

PascalCase = Naming convention - ItShouldLookLikeThis

Static members = When constants (or any static members) are defined in a separate class, you access them using the class name followed by a dot and the member name. This is called dot notation.

var = The var keyword lets the compiler figure out the type of a variable from the value you assign to it. The variable is still strongly typed, but you don't have to write the type name yourself.

Verbatim string = A verbatim string literal starts with @ before the opening quote. It tells C# to treat the string exactly as written, ignoring escape sequences like \n or \t. This is especially handy for Windows file paths, where every backslash would otherwise need to be doubled.

String Interpolation = String interpolation lets you embed variables and expressions directly inside strings using the $ prefix and curly braces {}.

char = Character - A char represents a single Unicode character. While strings hold multiple characters, a char holds exactly one. Use char when working with individual characters from strings or keyboard input.

+ = The + operator adds two values together. It's one of the most fundamental arithmetic operators in C#.

- = The subtraction operator (-) calculates the difference between two numbers. It subtracts the right operand from the left operand.

* = The multiplication operator * multiplies two numbers together. It's used whenever you need to calculate products, areas, or scale values.

/ = The division operator / divides one number by another. Unlike integer division, using double preserves decimal precision.

% = The modulo operator (%) returns the remainder after integer division. It's essential for tasks like checking even/odd numbers, cycling through values, and wrapping indices.

Order of Operation =
1. ( )      - Parentheses
2. * / %    - Multiplcation, Division, Modulo
3. + -      - Addition, Subtraction

