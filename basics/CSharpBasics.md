# **Basics of C#**

## **1. Basic Structure of a C# Program**

A C# program follows a specific structure, consisting of: 
1. Namespaces – Used to organize code and avoid name conflicts. 
2. Classes – A blueprint for objects, defining properties and methods. 
3. Methods – Blocks of code that perform specific tasks. 
4. Statements – Instructions executed by the program. 

```javascript

using System;  // Importing built-in namespace 
namespace MyFirstApp  // Namespace declaration 
{ 
} 
class Program  // Class declaration 
{ 
} 
static void Main()  // Main method (Entry point of the program) 
{ 
} 
Console.WriteLine("Hello, World!");  // Print statement

```  

## **2. Comments in C#**
Comments help to document the code and make it more understandable. 
**C# supports three types of comments:**

1. **Single-Line Comment:** Used for short explanations. 

```javascript

// This is a single-line comment 
Console.WriteLine("Hello, World!");  // This prints text to the console 

```  

2. **Multi-Line Comment:** Used for longer explanations. 

```javascript

/* 
This is a multi-line comment. 
It can span multiple lines. 
*/ 
Console.WriteLine("Multi-line comment example"); 

```  

3. **XML Documentation Comments:** Used for generating documentation. 

```javascript

/// <summary> 
/// This method prints a greeting message. 
/// </summary> 
static void Greet() 
{ 
Console.WriteLine("Hello!"); 
} 

```  

## **3. Data Types & Variables** 
A variable is a container that holds a value, each variable has a data type that defines what kind of data it can store. 

1. **Value Types**

These store actual values in memory. 

|Data Type |Size    |Example               |
|----------|--------|----------------------|
|int       |4 bytes |int age = 25;         |
|double    |8 bytes |double pi = 3.14159;  |
|float     |4 bytes |float price = 99.99f; |
|char      |2 bytes |char letter = 'A';    |
|bool      |1 byte  |bool isPassed = true; |
 


2. **Reference Types** 

These store memory addresses instead of actual values. 

|Data Type |Description             |Example               |
|----------|------------------------|----------------------|
|string    |Sequence of characters  |string name = "John"; |
|object    |Base type for all types |object obj = 42;      |


## **4. Constants & Read-Only Variables**

1. **Constants (const)**

Constants **cannot be changed** after assignment. 

```javascript

const double Pi = 3.14159; 
Console.WriteLine("Value of Pi: " + Pi); 

```  

2. **Read-Only Variables (readonly)** 

Can be assigned **only inside a constructor**. 

```javascript

class Example 
{ 

} 

readonly int year; 

public Example(int y) 
{ 
year = y;  // Assigned in constructor 
} 

public void Display() 
{ 
Console.WriteLine("Year: " + year); 
}

```

## **5. Input & Output** 

1. **Printing Output (Console.WriteLine)**

```javascript

Console.WriteLine("Hello, World!"); 
Console.Write("Enter your name: "); 

```

2. **Taking User Input (Console.ReadLine)**

```javascript 

Console.Write("Enter your name: "); 
string name = Console.ReadLine(); 
Console.WriteLine("Hello, " + name); 

```

3. **Converting Input (Convert.ToInt32)**

```javascript

Console.Write("Enter your age: "); 
int age = Convert.ToInt32(Console.ReadLine()); 
Console.WriteLine("You are " + age + " years old.");

```

## **6. Operators**
 
1. **Arithmetic Operators**

|Operator |Example |Result              |
|---------|--------|--------------------|
|+        |a + b   |Addition            |
|-        |a - b   |Subtraction         |
|*        |a * b   |Multiplication      |
|/        |a / b   |Division            |
|%        |a % b   |Modulus (Remainder) | 

```javascript

int a = 10, b = 5; 
Console.WriteLine(a + b);  // Output: 15 

```
 
2. **Logical Operators** 
 
|Operator |Example        |Description |
|---------|---------------|------------|
|&&       |a > 0 && b > 0 |AND         |
| 11      |a > 0 11 b > 0 |OR          |
|!        |!(a > b)       |NOT         |

```javascript

bool result = (10 > 5) && (5 < 3);  // false

```

## **7. Conditional Statements**
 
1. **if-else Statement**

```javascript

int num = 10; 
if (num > 0) 
{ 
    Console.WriteLine("Positive Number"); 
} 
else if ( num == 0 ) 
{ 
    Console.WriteLine("Zero"); 
} 
else 
{ 
    Console.WriteLine("Negative Number"); 
}

```

2. **switch-case Statement**
 
```javascript

char grade = 'B'; 
switch (grade) 
{ 
    case 'A': 
        Console.WriteLine("Excellent"); 
        break; 
    case 'B': 
        Console.WriteLine("Good"); 
        break; 
    default: 
        Console.WriteLine("Invalid Grade"); 
        break; 
} 

```

## **8. Loops**

Loops repeat a block of code multiple times. 
 
1. **For Loop**

```javascript

for (int i = 1; i <= 5; i++) 
{ 
    Console.WriteLine(i); 
} 

```

2. **While Loop**

```javascript

int i = 1; 
while (i <= 5) 
{ 
    Console.WriteLine(i);     i++; 
} 

```

3. **Do-While Loop**

```javascript

int i = 1; 
do 
{ 
    Console.WriteLine(i);      i++; 
} while (i <= 5); 

```

4. **Foreach Loop (for arrays & collections)**

```javascript

string[] fruits = { "Apple", "Banana", "Cherry" }; 
foreach (string fruit in fruits) 
{ 
    Console.WriteLine(fruit); 
} 

```

## **9. Array**

An array in C# is a **data structure that stores a fixed-size sequential collection of elements of the 
same type**. Arrays are used to store multiple values in a single variable, instead of declaring 
separate variables for each value. 

1. **Key Features of Arrays:**

 * **Fixed Size:** The size of an array is defined when it is created and cannot be changed. 
 * **Same Type:** All elements in an array must be of the same type (e.g., all integers, all strings, etc.). 
 * **Indexing:** Arrays are zero-indexed, meaning the first element is at index 0, the second at index 1,and so on. 
 * **Efficient Access:** Arrays provide fast access to elements using their index. 

 2. **Declaring and Initializing Arrays**

  * **Declaring an Array** 
You declare an array by specifying the data type of its elements and the number of elements it can hold. 

```javascript

int[] numbers; // Declares an array of integers  

```

 * **Initializing an Array**
After declaring an array, you can initialize it by specifying the size of the array or by assigning values directly. 

Example 1: Initializing with Size

```javascript

int[] numbers = new int[5]; // Initializes an array with 5 elements, all set to 0 by default 

```

Example 2: Initializing with Values 

 ```javascript 

int[] numbers = new int[] { 1, 20, 13, 4, 5 }; // Initializes an array with the values 1, 2, 3, 4, 5 

```
You can also omit the new int[] part when providing the values directly: 

```javascript

int[] numbers = { 1, 2, 3, 4, 5 };  

```

3. **Accessing Array Elements**

You can access elements in an array using their index. Example: 

```javascript
// create array for tank temperature ( single line comment ) 
/* 
Ignored block ( multiline comment ) 
*/ 
int[] TankTempDegrees = { 1, 2, 3, 4, 5 }; 
Console.WriteLine(TankTempDegrees [0]); // Outputs 1 (first element) 
Console.WriteLine(TankTempDegrees [4]); // Outputs 5 (fifth element) 

```

4. **Modifying Elements**

```javascript

numbers[2]; 
numbers[2] = 10; // Sets the third element to 10 
Console.WriteLine(numbers[2]); // Outputs 10 

```

5. **Iterating Over Arrays**

You can use loops to iterate over the elements of an array. 

 * **Using for Loop:**
```javascript

for (int i = 0; i < numbers.Length; i++) 
{ 
} 
Console.WriteLine(numbers[i]); 

```

 * **Using foreach Loop:**

```javascript

foreach (int number in numbers) 
{ 
} 
Console.WriteLine(number);

```

## **10. Multi-Dimensional Arrays**

C# supports multi-dimensional arrays, which can be thought of as arrays of arrays. The most common multi-dimensional array is the two-dimensional array (matrix). 

1. **Declaring a Two-Dimensional Array:**

```javascript

int[,] matrix = new int[3, 3]; // Declares a 3x3 matrix (3 rows, 3 columns) 

```

2. **Initializing a Two-Dimensional Array:**

```javascript

int[,] matrix = { 
{ 1, 2, 3 }, 
{ 4, 5, 6 }, 
{ 7, 8, 9 } 
}; 

```

3. **Accessing Elements:**

```javascript

Console.WriteLine(matrix[0, 0]); // Outputs 1 (element in the first row, first column) 
Console.WriteLine(matrix[2, 2]); // Outputs 9 (element in the third row, third column) 

```

## **11. Jagged Arrays **

A jagged array is an array of arrays, where each "inner" array can have different lengths. 

1. **Declaring a Jagged Array:**

```javascript

int[][] jaggedArray = new int[3][]; // Declares a jagged array with 3 inner arrays

```

2. **Initializing a Jagged Array:**

```javascript

jaggedArray[0] = new int[] { 1, 2, 3 }; 
jaggedArray[1] = new int[] { 4, 5 }; 
jaggedArray[2] = new int[] { 6, 7, 8, 9 }; 

```

3. **Accessing Elements in a Jagged Array:**

```javascript

Console.WriteLine(jaggedArray[0][0]); // Outputs 1 (first element of the first array) 
Console.WriteLine(jaggedArray[1][1]); // Outputs 5 (second element of the second array) 

```

## **12. Array Methods and Properties**

C# provides several useful methods and properties for working with arrays: 

1. **Length:** Returns the number of elements in the array. 

```javascript

int[] numbers = { 1, 2, 3, 4, 5 }; 
Console.WriteLine(numbers.Length); // Outputs 5 

```

2. **Array.Sort():** Sorts the elements of the array. 

```javascript

int[] numbers = { 5, 1, 4, 2, 3 }; 
Array.Sort(numbers); 
Console.WriteLine(string.Join(", ", numbers)); // Outputs 1, 2, 3, 4, 5

```

3. **Array.Reverse():** Reverses the order of the elements in the array. 

```javascript

int[] numbers = { 1, 2, 3, 4, 5 }; 
Array.Reverse(numbers); 
Console.WriteLine(string.Join(", ", numbers)); // Outputs 5, 4, 3, 2, 1 

```

4. **Array.IndexOf():** Returns the index of the first occurrence of a value. 

```javascript

int[] numbers = { 1, 2, 3, 4, 5 }; 
int index = Array.IndexOf(numbers, 3); 
Console.WriteLine(index); // Outputs 2

```

## **13. Nested for Loop**

A **nested for loop** is when a for loop is placed inside another for loop. This structure is useful when dealing with multidimensional problems, such as working with matrices, creating patterns, and performing repetitive calculations. 

```javascript

for (initialization; condition; increment/decrement) 
{ 
    for (initialization; condition; increment/decrement) 
    { 
        // Inner loop statements 
    } 
    // Outer loop statements 
} 

```

~~NOTE:~~ 

- The **outer loop** runs first.
- For each iteration of the **outer loop**, the **inner loop** runs completely.
- The process continues until the **outer loop** condition fails. 

**Example 1:** Printing a Multiplication Table 

```javascript

   for (int i = 1; i <= 5; i++) // Outer loop for rows 
        { 
            for (int j = 1; j <= 5; j++) // Inner loop for columns 
            { 
                Console.Write((i * j) + "\t"); // Print product 
            } 
            Console.WriteLine(); // New line after each row 
        } 

```

_Output:_

```javascript

1   2   3   4   5 
2   4   6   8   10 
3   6   9   12  15 
4   8   12  16  20 
5   10  15  20  25 

```

**Example 2:** Printing a Right-Angled Triangle 

```javascript

for (int i = 1; i <= 5; i++) // Controls rows 
        { 
            for (int j = 1; j <= i; j++) // Controls columns 
            { 
                Console.Write("* "); 
            } 
            Console.WriteLine(); // Move to next line 
        } 

```
 
_Output:_

```javascript

*  
* *  
* * *  
* * * *  
* * * * * 

```
_Explanation:_

- The outer loop determines the number of rows (i) 
- The inner loop prints * according to the row number. 
- Each row has i stars. 

**Example 3:** Printing a Pyramid Pattern

```javascript

int n = 5; // Number of rows 
       for (int i = 1; i <= n; i++) // Controls rows 
      { 
            for (int j = 1; j <= n - i; j++) // Prints spaces 
            {     Console.Write(" ");   } 
            for (int k = 1; k <= 2 * i - 1; k++) // Prints stars 
            {         Console.Write("*");   }            
            Console.WriteLine(); // Move to the next line 
      } 

```

_Output:_

```javascript

*     
***    
*****   
*******  
*********  

```

~~NOTE:~~

**Key Takeaways**

1. Execution Order:  
   * The inner loop completes all its iterations for each outer loop iteration. 

2. Use Cases:  
   * Matrix operations 
   * Printing patterns 
   * Working with multi-dimensional arrays 

3. Performance Consideration:  
   * Nested loops increase time complexity. 
   * Avoid unnecessary nesting to optimize performance. 


## **14. Functions**

In C#, functions (also known as methods) **are blocks of code that perform a specific task**. They are a fundamental concept in programming, allowing you to encapsulate code into reusable units. 

**There are two types of Functions:** 
- Built-in Functions 
- User defined Functions 

### 14.1.  Built-in Functions  

These functions are **available by .Net Framework to perform common tasks**, ranging from mathematical operations to string manipulation, array handling, and more. 

1. **Math Functions:** The Math class provides various mathematical functions. 

 * Math.Abs: Returns the absolute value of a number. 

 ```javascript
int value = -10; 
int absoluteValue = Math.Abs(value); // absoluteValue = 10 
```

 * Math.Pow: Raises a number to a specified power. 

```javascript
double result = Math.Pow(2, 3); // result = 8 
```

 * Math.Sqrt: Returns the square root of a number. 

```javascript
double squareRoot = Math.Sqrt(16); // squareRoot = 4 
```

 * Math.Max and Math.Min: Return the larger or smaller of two numbers. 

 ```javascript
int max = Math.Max(5, 10); // max = 10 
int min = Math.Min(5, 10); // min = 5 
```

 * Math.Round: Rounds a floating-point number to the nearest integer or specified number of decimal places. 

```javascript
double rounded = Math.Round(4.56789, 2); // rounded = 4.57 
```

2. **String Functions:** The String class provides methods to manipulate strings. 

 * string.Length: Gets the length of a string. 

```javascript
string message = "Hello, world!"; 
int length = message.Length; // length = 13 
```

 * string.Substring: Extracts a substring from a string. 
```javascript
string sub = message.Substring(7, 5); // sub = "world" 
```

 * string.ToUpper and string.ToLower: Convert a string to uppercase or lowercase. 

```javascript
string upper = message.ToUpper(); // upper = "HELLO, WORLD!" 
string lower = message.ToLower(); // lower = "hello, world!" 
```

 * string.Trim: Removes leading and trailing white-space characters from a string.

```javascript
string trimmed = "  Hello  ".Trim(); // trimmed = "Hello" 
``` 

 * string.Replace: Replaces all occurrences of a specified string with another string. 

```javascript
string replaced = message.Replace("world", "C#"); // replaced = "Hello, C#!" 
``` 

 * string.Contains: Determines whether a string contains a specified substring. 

```javascript
bool contains = message.Contains("world"); // contains = true 
```

 * string.Split: Splits a string into an array of substrings based on a delimiter. 

```javascript
string[] words = message.Split(' '); // words = ["Hello,", "world!"] 
```

3. ***Date and Time Functions:** The DateTime class provides functions to work with dates and times. 

 * DateTime.Now: Gets the current date and time. 

```javascript
DateTime now = DateTime.Now; 
```

 * DateTime.Today: Gets the current date with the time component set to 00:00:00. 

```javascript
DateTime today = DateTime.Today; 
```

 * DateTime.AddDays: Adds a specified number of days to a DateTime object. 

```javascript
DateTime tomorrow = today.AddDays(1); 
```

 * DateTime.ToString: Converts the date and time to a string in a specified format.

```javascript 
string formattedDate = now.ToString("yyyy-MM-dd HH:mm:ss"); // formattedDate = "2024-08-18 15:30:00" 
```

 * DateTime.Parse and DateTime.TryParse: Parse a string representation of a date and time into a DateTime object. 

```javascript
DateTime parsedDate = DateTime.Parse("2024-08-18"); 
bool success = DateTime.TryParse("2024-08-18", out DateTime result); 
```

4. **Array Functions:** C# arrays have several built-in methods. 

 * Array.Sort: Sorts the elements of an array. 

```javascript
int[] numbers = { 3, 1, 4, 1, 5 }; 
Array.Sort(numbers); // numbers = { 1, 1, 3, 4, 5 } 
```

 * Array.Reverse: Reverses the sequence of the elements in an array. 

```javascript
Array.Reverse(numbers); // numbers = { 5, 4, 3, 1, 1 } 
```

 * Array.IndexOf: Searches for the specified object and returns the index of its first occurrence in an array. 

```javascript
int index = Array.IndexOf(numbers, 4); // index = 1 
```

 * Array.Resize: Changes the size of a one-dimensional array.

```javascript 
Array.Resize(ref numbers, 10); // numbers is now of length 10 
```

5. **Console Functions:** The Console class is used for basic input/output operations. 

 * Console.WriteLine: Writes the specified data, followed by the current line terminator, to the console. 

```javascript
Console.WriteLine("Hello, world!"); 
```

 * Console.Write: Writes the specified data to the console without appending a new line. 

```javascript
Console.Write("Enter your name: "); 
```

 * Console.ReadLine: Reads the next line of characters from the standard input stream. 

```javascript
string name = Console.ReadLine(); 
```

6. **Type Conversion Functions:** C# provides several built-in methods for converting between types. 

 * Convert.ToInt32: Converts a specified value to a 32-bit signed integer.

```javascript 
string numberString = "123"; 
int number = Convert.ToInt32(numberString); // number = 123 
```

 * Convert.ToDouble: Converts a specified value to a double-precision floating-point number. 

```javascript 
string doubleString = "123.45"; 
double doubleNumber = Convert.ToDouble(doubleString); // doubleNumber = 123.45 
```

 * Convert.ToString: Converts a specified value to a string. 

```javascript 
int num = 123; 
string numString = Convert.ToString(num); // numString = "123" 
```

 * int.Parse and int.TryParse: Convert a string representation of a number to its integer equivalent. 

```javascript 
int parsedNumber = int.Parse("456"); // parsedNumber = 456 
bool success = int.TryParse("456"); // success = true 
```

8. **Random Number Functions:** The Random class is used to generate random numbers. 

 * Random.Next: Returns a random integer. 

```javascript
Random random = new Random(); 
int randomNumber = random.Next(); // randomNumber = any integer 
int randomInRange = random.Next(1, 10); // randomInRange = integer between 1 and 9 
```

 * Random.NextDouble: Returns a random floating-point number between 0.0 and 1.0 

```javascript
double randomDouble = random.NextDouble(); // randomDouble = value between 0.0 and 1.0 
```

### 14.2. User Defined Functions  


## **15. Errors**

In programming, errors can generally be categorized into three main types: **syntax errors**, **runtime   errors**, and **logical errors**. Understanding these error types is crucial for effective debugging and 
writing robust code. Let's explore each type with examples and how to handle them in C#. 

1. **Syntax Errors:** Syntax errors occur when the code violates the grammatical rules of the programming language. These errors are usually detected by the compiler before the program runs. 

```javascript
//Example: 
int number = 10 
Console.WriteLine(number);
string number = "10"; 
```

2. **Runtime Errors:** Runtime errors occur while the program is running, usually because of operations that are not logically valid at runtime, such as dividing by zero, accessing an array out of bounds, or attempting to use a null reference. 

```javascript
//Example: 
int divisor = 0; 
int result = 10 / divisor; 
Console.WriteLine(result); 

//---------------------------------------- 
//How to Handle: 

try 
{ 
} 
int divisor = 0; 
int result = 10 / divisor; 
Console.WriteLine(result); 
catch (DivideByZeroException ex) 
{   
 Console.WriteLine("Error: " + ex.Message);} 

//---------------------------------
//OR Validations:  

int divisor = 0; 
if (divisor != 0) 
{ 
} 
int result = 10 / divisor; 
Console.WriteLine(result); 
else 
{ 
} 
Console.WriteLine("Cannot divide by zero."); 

//---------------------------------------------------------------------- 

string message = null; 
Console.WriteLine(message.Length); 

//System.NullReferenceException: Object reference not set to an instance of an object. 

string message = null; 
if (message != null) 
{ 
} 
Console.WriteLine(message.Length); 
else 
{ 
} 

```

3. **Logical Errors:** Logical errors occur when the program compiles and runs, but the output is not what you expected. These errors are the most difficult to detect because the program doesn't crash or show any 
immediate signs of error. 

```javascript
//Example: 
int[] numbers = {1, 2, 3, 4, 5}; 
for (int i = 0; i <= numbers.Length; i++) // Logical error: should be i < numbers.Length; 
{ 
} 
Console.WriteLine(numbers[i]); 

//System.IndexOutOfRangeException: Index was outside the bounds of the array. 

for (int i = 0; i < numbers.Length; i++) 
{ 
} 
Console.WriteLine(numbers[i]); 

//------------------------------------------------------------- 

string input = "yes"; 
if (input == "Yes") // Logical error: comparison is case-sensitive 
{ 
} 
Console.WriteLine("Input is yes"); 
else 
{ 
} 
Console.WriteLine("Input is not yes"); 

//incorrect string comparison 

if (input.Equals ("Yes", StringComparison.OrdinalIgnoreCase)) 
{  
    Console.WriteLine("Input is yes"); 
} 
else 
{   
     Console.WriteLine("Input is not yes"); 
}
```



