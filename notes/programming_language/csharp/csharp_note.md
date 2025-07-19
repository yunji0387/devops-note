# C# commands

## Table of Contents
1. [How to create, build & run c#](#how_to_run)
2. [Object type](#object_type)
3. [Type cast](#type_cast)
4. [Console functions](#console_functions)
5. [string functions](#string_functions)
6. [Number type functions](#number_functions)
7. [Expression(boolean)](#expression)
8. [Array type](#array)
9. [Loop](#loop)
10. [Random library](#random)
11. [Array operations](#array_operations)
12. [Methods](#methods)
13. [Debugging](#debugging)
14. [Exception Handling](#exception_handling)
15. [List & Collection](#list_collections)
16. [Classes & Objects](#classes_objects)
17. [Sources](#sources)

<a id="how_to_run"></a>
## How to create, build & run c#
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

1. make sure to have .NET SDK install
   - visit this [link for more detail](https://learn.microsoft.com/en-us/training/modules/install-configure-visual-studio-code/6-exercise-install-dotnet).
2. make sure to have c# extension install in vs code
   - visit this [link for more detail](https://learn.microsoft.com/en-us/training/modules/install-configure-visual-studio-code/5-exercise-configure-visual-studio-code).
3. create c# project
   - in Terminal run:
   ```c#
   dotnet new console -o ./CsharpProjects/TestProject
   ```
4. build c# project
   - first make sure terminal path located in the project folder, then run:
   ```c#
   dotnet build
   ```
5. run c# project
   - first make sure terminal path located in the project folder and has done step 4, then run:
   ```c#
   dotnet run
   ```

<!-- /MarkdownTOC -->
</details>

<a id="object_type"></a>
## Object type
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->
   
- **int** (4 bytes : -2,147,483,648 to 2,147,483,647)
- **long** (8 bytes : -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807)
- **float** (4 bytes : 6 to 7 decimal digits)
- **double** (8 bytes : 15 decimal digits)
- **bool** (1 bit : true/false)
- **char** (2 bytes : character/letter)
- **string** (2 bytes per character)
- **var** (implicitly typed local variable - Must be initialize)

### integral types
- signed integral types
  ```c#
   Console.WriteLine("Signed integral types:");
   Console.WriteLine($"sbyte  : {sbyte.MinValue} to {sbyte.MaxValue}");
   Console.WriteLine($"short  : {short.MinValue} to {short.MaxValue}");
   Console.WriteLine($"int    : {int.MinValue} to {int.MaxValue}");
   Console.WriteLine($"long   : {long.MinValue} to {long.MaxValue}");

   Console.WriteLine("");
   Console.WriteLine("Floating point types:");
   Console.WriteLine($"float  : {float.MinValue} to {float.MaxValue} (with ~6-9 digits of precision)");
   Console.WriteLine($"double : {double.MinValue} to {double.MaxValue} (with ~15-17 digits of precision)");
   Console.WriteLine($"decimal: {decimal.MinValue} to {decimal.MaxValue} (with 28-29 digits of precision)");
   ```
   ```
   Signed integral types:
   sbyte  : -128 to 127
   short  : -32768 to 32767
   int    : -2147483648 to 2147483647
   long   : -9223372036854775808 to 9223372036854775807

   Floating point types:
   float  : -3.402823E+38 to 3.402823E+38 (with ~6-9 digits of precision)
   double : -1.79769313486232E+308 to 1.79769313486232E+308 (with ~15-17 digits of precision)
   decimal: -79228162514264337593543950335 to 79228162514264337593543950335 (with 28-29 digits of precision)
   ```
- unsigned integral types
  ```c#
   Console.WriteLine("");
   Console.WriteLine("Unsigned integral types:");
   
   Console.WriteLine($"byte   : {byte.MinValue} to {byte.MaxValue}");
   Console.WriteLine($"ushort : {ushort.MinValue} to {ushort.MaxValue}");
   Console.WriteLine($"uint   : {uint.MinValue} to {uint.MaxValue}");
   Console.WriteLine($"ulong  : {ulong.MinValue} to {ulong.MaxValue}");
  ```
  ```output
   Unsigned integral types:
   byte   : 0 to 255
   ushort : 0 to 65535
   uint   : 0 to 4294967295
   ulong  : 0 to 18446744073709551615
  ```

<!-- /MarkdownTOC -->
</details>


<a id="type_cast"></a>
## Type cast
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- decimal to int
  ```c#
   int value = (int)1.5m; // casting truncates
   Console.WriteLine(value); // 1
   
   int value2 = Convert.ToInt32(1.5m); // converting rounds up
   Console.WriteLine(value2); // 2
  ```
- number to string
  ```c#
   int first = 5;
   int second = 7;
   string message = first.ToString() + second.ToString();
   Console.WriteLine(message);
  ```
- string to int
  ```c#
   string first = "5";
   string second = "7";
   int sum = int.Parse(first) + int.Parse(second);
   Console.WriteLine(sum);
  ```
  or
  ```c#
   string value1 = "5";
   string value2 = "7";
   int result = Convert.ToInt32(value1) * Convert.ToInt32(value2);
   Console.WriteLine(result);
  ```
- string to decimal
  ```c#
   string first = "5.69";
   int convertFirst = Convert.ToDecimal(first);
   Console.WriteLine(convertFirst);
  ```
- TryParse(<var1>, out <var2>)
  ```c#
   string value = "bad";
   int result = 0;
   if (int.TryParse(value, out result))
   {
       Console.WriteLine($"Measurement: {result}");
   }
   else
   {
       Console.WriteLine("Unable to report the measurement.");
   }
   
   if (result > 0)
       Console.WriteLine($"Measurement (w/ offset): {50 + result}");
  ```

<!-- /MarkdownTOC -->
</details>

<a id="console_functions"></a>
## Console functions
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->
 
- console print new line
  ```c#
    Console.WriteLine("Hello World!");
    Console.WriteLine('H');
    Console.WriteLine(123);
  ```
- console print
  ```c#
    Console.Write("Hello World!");
  ```
- other
  ```c#
    Console.WriteLine("Hello" + " " + "World!");
  ```

<!-- /MarkdownTOC -->
</details>

<a id="string_functions"></a>
## string functions
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

### escape sequences
- ```c#
    Console.WriteLine("Hello\nWorld!"); // add new line
    Console.WriteLine("Hello\tWorld!"); // add tab
    Console.WriteLine("Hello \"World\"!"); // add "
    Console.WriteLine("c:\\source\\repos"); // add \
    Console.WriteLine(@"    c:\source\repos    
        (this is where your code goes)"); // @(verbatim) keep all whitespace and character without need of escape backslash
    Console.WriteLine("\u3053\u3093\u306B\u3061\u306F World!"); // unicode escape character
  ```
### interpolation
- string interpolation
  ```c#
    string message = greeting + " " + firstName + "!";
    // is same as
    string message = $"{greeting} {firstName}!";
  ```
- string interpolation and verbatim
  ```c#
    string projectName = "First-Project";
    Console.WriteLine($@"C:\Output\{projectName}\Data");
  ```

### Composite Formatting 
- composite formatting with index
  ```c#
   string first = "Hello";
   string second = "World";
   Console.WriteLine("{1} {0}!", first, second); // World Hello!
   Console.WriteLine("{0} {0} {0}!", first, second); // Hello Hello Hello!
  ```
- formatting for currency
  ```c#
   decimal price = 123.45m;
   int discount = 50;
   Console.WriteLine($"Price: {price:C} (Save {discount:C})"); // Price: $123.45 (Save $50.00)
  ```
- formatting for numbers
   ```c#
   decimal measurement = 123456.78912m;
   Console.WriteLine($"Measurement: {measurement:N} units"); // Measurement: 123,456.79 units
   Console.WriteLine($"Measurement: {measurement:N4} units"); // Measurement: 123,456.7891 units
   ```
- formatting for percentages
  ```c#
   decimal tax = .36785m;
   Console.WriteLine($"Tax rate: {tax:P2}"); // Tax rate: 36.79 %

   decimal price = 67.55m;
   decimal salePrice = 59.99m;
   string yourDiscount = String.Format("You saved {0:C2} off the regular {1:C2} price. ", (price - salePrice), price);   
   yourDiscount += $"A discount of {((price - salePrice)/price):P2}!"; //inserted
   Console.WriteLine(yourDiscount); // You saved $7.56 off the regular $67.55 price. A discount of 11.19%!
  ```
### PadLeft() & PadRight()
```c#
string input = "Pad this";
Console.WriteLine(input.PadLeft(12)); // Pad this
Console.WriteLine(input.PadLeft(12, '-')); // ----Pad this
Console.WriteLine(input.PadRight(12, '-')); // Pad this----
```

### IndexOf() & Substring()
- IndexOf() gives you the first position of a character or string inside of another string.
- IndexOf() returns -1 if it can't find a match.
- Substring() returns just the specified portion of a string, using a starting position and optional length.
  ```c#
   string message = "Find what is (inside the parentheses)";
   int openingPosition = message.IndexOf('(');
   int closingPosition = message.IndexOf(')');   
   Console.WriteLine(openingPosition); // 13
   Console.WriteLine(closingPosition); // 36
   int length = closingPosition - openingPosition;
   Console.WriteLine(message.Substring(openingPosition, length)); // (inside the parentheses
  ```
### IndexOfAny() & LastIndexOf()
- Retrieve the last occurrence of a sub string
  ```c#
   string message = "(What if) I am (only interested) in the last (set of parentheses)?";
   int openingPosition = message.LastIndexOf('('); 
   openingPosition += 1;
   int closingPosition = message.LastIndexOf(')');
   int length = closingPosition - openingPosition;
   Console.WriteLine(message.Substring(openingPosition, length)); // set of parentheses
  ```
- Retrieve all instances of substrings inside parentheses
  ```c#
   string message = "(What if) there are (more than) one (set of parentheses)?";
   while (true)
   {
       int openingPosition = message.IndexOf('(');
       if (openingPosition == -1) break;
   
       openingPosition += 1;
       int closingPosition = message.IndexOf(')');
       int length = closingPosition - openingPosition;
       Console.WriteLine(message.Substring(openingPosition, length));
   
       // Note the overload of the Substring to return only the remaining 
       // unprocessed message:
       message = message.Substring(closingPosition + 1);
   }
  ```
- IndexOfAny()
  ```c#
   string message = "Help (find) the {opening symbols}";
   Console.WriteLine($"Searching THIS Message: {message}"); // Searching THIS message: Help (find) the {opening symbols}
   char[] openSymbols = { '[', '{', '(' };
   int startPosition = 6;
   int openingPosition = message.IndexOfAny(openSymbols);
   Console.WriteLine($"Found WITHOUT using startPosition: {message.Substring(openingPosition)}"); // Found WITHOUT using startPosition: (find) the {opening symbols}
   openingPosition = message.IndexOfAny(openSymbols, startPosition);
   Console.WriteLine($"Found WITH using startPosition: {message.Substring(openingPosition)}"); // Found WITH using startPosition 6: {opening symbols}
  ```

### Remove() & Replace()
- Remove()
  ```c#
   string data = "12345John Smith          5000  3  ";
   string updatedData = data.Remove(5, 20);
   Console.WriteLine(updatedData); // 123455000  3
  ```
- Replace()
  ```c#
   string message = "This--is--ex-amp-le--da-ta";
   message = message.Replace("--", " ");
   message = message.Replace("-", "");
   Console.WriteLine(message); // This is example data
  ```

### overall built-in methods
- Methods that add blank spaces for formatting purposes (PadLeft(), PadRight())
- Methods that compare two strings or facilitate comparison (Trim(), TrimStart(), TrimEnd(), GetHashcode(), the Length property)
- Methods that help you determine what's inside of a string, or even retrieve just a part of the string (Contains(), StartsWith(), EndsWith(), Substring())
- Methods that change the content of the string by replacing, inserting, or removing parts (Replace(), Insert(), Remove())
- Methods that turn a string into an array of strings or characters (Split(), ToCharArray())
  
### Contains function
- check if a string contains a substring
  ```c#
   string pangram = "The quick brown fox jumps over the lazy dog.";
   Console.WriteLine(pangram.Contains("fox")); // True
   Console.WriteLine(pangram.Contains("cow")); // False
  ```
<!-- /MarkdownTOC -->
</details>

<a id="number_functions"></a>
## Number type functions
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->
   
### integer
- math operations
  ```c#
   int sum = 7 + 5; // 12
   sum += 5; // 17
   sum ++; // 18
   sum --; // 17
   sum -= 5; // 12
   sum = sum + 10; // 22
   int difference = 7 - 5; // 2
   int product = 7 * 5; // 35
   int quotient = 7 / 5; // 1
  ```
- modulus
  ```c#
   int a = 200 % 5; // 0
   int b = 7 % 5; // 2
  ```
### decimal
- decimal quotient
  ```c#
    decimal decimalQuotient = 7.0m / 5; // 1.4
  ```
  
<!-- /MarkdownTOC -->
</details>

<a id="expression"></a>
## Expression(boolean)
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->
 
- basics
  ```c#
   Console.WriteLine("a" != "a"); // False
   Console.WriteLine("a" != "A"); // True
   Console.WriteLine(1 != 2); // True
   string myValue = "a";
   Console.WriteLine(myValue != "a"); // False
  ```
  ```c#
   Console.WriteLine(1 > 2); // False
   Console.WriteLine(1 < 2); // True
   Console.WriteLine(1 >= 1); // True
   Console.WriteLine(1 <= 1); // True
  ```
### Conditional operator
- ```c#
   <evaluate this condition> ? <if condition is true, return this value: <if condition is false, return this value>
  ```
- example
  ```c#
   int saleAmount = 1001;
   int discount = saleAmount > 1000 ? 100 : 50;
   Console.WriteLine($"Discount: {discount}"); // Discount: 100
  ```

### switch statement
```c#
switch (fruit)
{
    case "apple":
    case "grape":
        Console.WriteLine($"App will display information for apple or grape.");
        break;

    case "banana":
        Console.WriteLine($"App will display information for banana.");
        break;

    case "cherry":
        Console.WriteLine($"App will display information for cherry.");
        break;
   default:
        Console.WriteLine($"App will display information for default.");
        break;
}
```

<!-- /MarkdownTOC -->
</details>


<a id="array"></a>
## Array type
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

```c#
int[] array = new int[10];
array[0] = 1;
array[1] = 10;
int[] inventory = { 200, 450, 700, 175, 250 };
string[] fraudulentOrderIDs = new string[3];
string [,] array2D = new array[3][6]; //declare 2d array
```
 
<!-- /MarkdownTOC -->
</details>

<a id="loop"></a>
## Loop
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- foreach loop
```c#
int[] inventory = { 200, 450, 700, 175, 250 };
int sum = 0;
foreach (int items in inventory)
{
    sum += items;
}
```

- for loop
```c#
int[] inventory2 = { 200, 450, 700, 175, 250 };
int sum2 = 0;
for(int i=0 ; i<inventory2.Length ; i++)
{
    sum2 += inventory2[i];
}
Console.WriteLine("for inventory sum: " + sum2);
```

- do while loop
```c#
Random random = new Random();
int current = 0;

do
{
    current = random.Next(1, 11);
    Console.WriteLine(current);
} while (current != 7);
```
 
<!-- /MarkdownTOC -->
</details>

<a id="random"></a>
## Random library
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

```c#
Random dice = new Random();
int roll = dice.Next(1, 7); // limit number from 1 - 6 ( [1, 7) )
int roll1 = dice.Next(); // limit number from 0 - 2,147,483,647(int max) ( [0, int max) )
int roll2 = dice.Next(101); // limit number from 0 - 100 ( [0, 101) )
int roll3 = dice.Next(50, 101); // limit number from 50 - 100 ( [50, 100) )

Console.WriteLine(roll);  // 5
Console.WriteLine($"First roll: {roll1}"); // 342585470
Console.WriteLine($"Second roll: {roll2}"); // 43 
Console.WriteLine($"Third roll: {roll3}"); // 89
```
 
<!-- /MarkdownTOC -->
</details>

<a id="array_operations"></a>
## Array operations
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- Sort()
  ```c#
   string[] pallets = { "B14", "A11", "B12", "A13" };
   Console.WriteLine("Sorted...");
   Array.Sort(pallets);
   foreach (var pallet in pallets)
   {
       Console.WriteLine($"-- {pallet}");
   }
  ```
  ```output
   Sorted...
   -- A11
   -- A13
   -- B12
   -- B14
  ```
  
- Reverse()
  ```c#
   string[] pallets = { "B14", "A11", "B12", "A13" };
   Console.WriteLine("Reversed...");
   Array.Reverse(pallets);
   foreach (var pallet in pallets)
   {
       Console.WriteLine($"-- {pallet}");
   }
  ```
  ```output
   Reversed...
   -- B14
   -- B12
   -- A13
   -- A11
  ```

- Clear() with specific range
  ```c#
   string[] pallets = { "B14", "A11", "B12", "A13" };
   Console.WriteLine($"Before: {pallets[0]}");
   Array.Clear(pallets, 0, 2);
   Console.WriteLine($"After: {pallets[0]}");
   
   Console.WriteLine($"Clearing 2 ... count: {pallets.Length}");
   foreach (var pallet in pallets)
   {
       Console.WriteLine($"-- {pallet}");
   }
  ```
  ```output
   Before: B14
   After:
   Clearing 2 ... count: 4
   --
   --
   -- B12
   -- A13
  ```

- Resize()
  ```c#
   string[] pallets = { "B14", "A11", "B12", "A13" };
   Array.Resize(ref pallets, 6);
   Console.WriteLine($"Resizing 6 ... count: {pallets.Length}");
   
   pallets[4] = "C01";
   pallets[5] = "C02";
   
   foreach (var pallet in pallets)
   {
       Console.WriteLine($"-- {pallet}");
   }
  ```
  ```output
   Resizing 6 ... count: 6
   -- B14
   -- A11
   -- B12
   -- A13
   -- C01
   -- C02
  ```

- Resize() to remove elements
  ```c#
   string[] pallets = { "B14", "A11", "B12", "A13" };
   Array.Resize(ref pallets, 3);
   Console.WriteLine($"Resizing 3 ... count: {pallets.Length}");
   
   foreach (var pallet in pallets)
   {
       Console.WriteLine($"-- {pallet}");
   }
  ```
  ```output
   Resizing 3 ... count: 3
   --
   --
   -- B12
  ```

- ToCharArray()
  ```c#
   string value = "abc123";
   char[] valueArray = value.ToCharArray();
   Array.Reverse(valueArray);
   string result = new string(valueArray);
   Console.WriteLine(result); // 321cbs
  ```

- Split()
  ```c#
   string result = "3,2,1,c,b,a";
   string[] items = result.Split(',');
   foreach (string item in items)
   {
       Console.WriteLine(item);
   }
  ```
  ```output
   3
   2
   1
   c
   b
   a
  ```

- Join()
  ```c#
   string value = "321cba";
   string result = String.Join(",", value);
   Console.WriteLine(result); // 3,2,1,c,b,a
  ```

<!-- /MarkdownTOC -->
</details>

<a id="methods"></a>
## Methods
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

### void methods
  ```c#
   CountTo(5);
   void CountTo(int max) 
   {
       for (int i = 0; i < max; i++)
       {
           Console.Write($"${i}, ");
       }
   }
  ```
  using "return" in void method will terminate the execution of the void method

### optional parameters
- set a default value for the parameter to make it optional
  ```c#
   void RSVP(string name, int partySize = 1, string allergies = "none", bool inviteOnly = true){ ... }
   RSVP("Rebecca"); // partySize = 1 , allergies = "none" , inviteOnly = true
   RSVP("Nadia", 2, "Nuts"); // inviteOnly = true
   RSVP(name: "Linh", partySize: 2, inviteOnly: false);
   RSVP("Tony", allergies: "Jackfruit", inviteOnly: true);
   RSVP("Noor", 4, inviteOnly: false);
   RSVP("Jonte", 2, "Stone fruit", false);
  ```

### return type methods
```c#
double GetDiscountedPrice(int itemIndex)
{
    double result = items[itemIndex] * (1 - discounts[itemIndex]);
    return result;
}

bool TotalMeetsMinimum()
{
    return total >= minimumSpend;
}
```

<!-- /MarkdownTOC -->
</details>

<a id="debugging"></a>
## Debugging
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

### [More detail tutorial in this link](https://learn.microsoft.com/en-us/training/modules/implement-visual-studio-code-debugging-tools/2-examine-visual-studio-code-debugger)

<!-- /MarkdownTOC -->
</details>

<a id="exception_handling"></a>
## Exception Handling
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

### Exception handling keywords, code blocks, and patterns
```c#
try
{   
   // try code block - code that may generate an exception
}
catch
{   
   // catch code block - code to handle an exception
}
finally
{   
   // finally code block - code to clean up resources
}
```
```c#
try
{
    // Step 1: code execution begins
    try
    {
        // Step 2: an exception occurs here
    }
    finally
    {
        // Step 4: the system executes the finally code block associated with the try statement where the exception occurred
    }

}
catch // Step 3: the system finds a catch clause that can handle the exception
{   
   // Step 5: the system transfers control to the first line of the catch code block
}
```

### [Types of exceptions in this link](https://learn.microsoft.com/en-us/training/modules/implement-exception-handling-c-sharp/3-examine-compiler-generated-exceptions)

### try-catch examples
- example 1
   ```c#
   try
   {
       Process1();
   }
   catch
   {
       Console.WriteLine("An exception has occurred");
   }
   
   Console.WriteLine("Exit program");
   
   static void Process1()
   {
       try
       {
           WriteMessage();
       }
       catch
       {
           Console.WriteLine("Exception caught in Process1");
       }
   
   }
   
   static void WriteMessage()
   {
       double float1 = 3000.0;
       double float2 = 0.0;
       int number1 = 3000;
       int number2 = 0;
   
       Console.WriteLine(float1 / float2);
       Console.WriteLine(number1 / number2);
   }
   ```
   ```output
   ∞
   Exception caught in Process1
   Exit program
   ```
   or
  ```c#
   static void Process1()
   {
       try
       {
           WriteMessage();
       }
       catch (Exception ex)
       {
           Console.WriteLine($"Exception caught in Process1: {ex.Message}");
       }
   }
  ```
  
- catch specific exception types
  ```c#
   static void Process1()
   {
       try
       {
           WriteMessage();
       }
       catch (DivideByZeroException ex)
       {
           Console.WriteLine($"Exception caught in Process1: {ex.Message}");
       }
   }
  ```
   or
  ```c#
   // inputValues is used to store numeric values entered by a user
   string[] inputValues = new string[]{"three", "9999999999", "0", "2" };
   
   foreach (string inputValue in inputValues)
   {
       int numValue = 0;
       try
       {
           numValue = int.Parse(inputValue);
       }
       catch (FormatException)
       {
           Console.WriteLine("Invalid readResult. Please enter a valid number.");
       }
       catch (OverflowException)
       {
           Console.WriteLine("The number you entered is too large or too small.");
       }
       catch(Exception ex)
       {
           Console.WriteLine(ex.Message);
       }
   }
  ```

### Create an excepton object
  ```c#
   ArgumentException invalidArgumentException = new ArgumentException();
  ```
  ```c#
   ArgumentException invalidArgumentException = new ArgumentException("ArgumentException: The 'GraphData' method received data outside the expected range.");
   throw invalidArgumentException;
  ```

### When to throw an exception
```c#
string[][] userEnteredValues = new string[][]
{
        new string[] { "1", "two", "3"},
        new string[] { "0", "1", "2"}
};

foreach (string[] userEntries in userEnteredValues)
{
    try
    {
        BusinessProcess1(userEntries);
    }
    catch (Exception ex)
    {
        if (ex.StackTrace.Contains("BusinessProcess1") && (ex is FormatException))
        {
            Console.WriteLine(ex.Message);
        }
    }
}

static void BusinessProcess1(String[] userEntries)
{
    int valueEntered;

    foreach (string userValue in userEntries)
    {
        try
        {
            valueEntered = int.Parse(userValue);

            // completes required calculations based on userValue
            // ...
        }
        catch (FormatException)
        {
            FormatException invalidFormatException = new FormatException("FormatException: User input values in 'BusinessProcess1' must be valid integers");
            throw invalidFormatException;
        }
    }
}
```

### Re-throwing exceptions
```c#
catch (Exception ex)
{
    // handle or partially handle the exception
    // ...

    // re-throw the original exception object for further handling down the call stack
    throw;
}
```
```c#
catch (Exception ex)
{
    // handle or partially handle the exception
    // ...

    // create a new exception object that wraps the original exception
    throw new ApplicationException("An error occurred", ex);
}
```
### complete example
```c#
string[][] userEnteredValues = new string[][]
{
            new string[] { "1", "2", "3"},
            new string[] { "1", "two", "3"},
            new string[] { "0", "1", "2"}
};

try
{
    Workflow1(userEnteredValues);
    Console.WriteLine("'Workflow1' completed successfully.");

}
catch (DivideByZeroException ex)
{
    Console.WriteLine("An error occurred during 'Workflow1'.");
    Console.WriteLine(ex.Message);
}

static void Workflow1(string[][] userEnteredValues)
{
    foreach (string[] userEntries in userEnteredValues)
    {
        try
        {
            Process1(userEntries);
            Console.WriteLine("'Process1' completed successfully.");
            Console.WriteLine();
        }
        catch (FormatException ex)
        {
            Console.WriteLine("'Process1' encountered an issue, process aborted.");
            Console.WriteLine(ex.Message);
            Console.WriteLine();
        }
    }
}

static void Process1(String[] userEntries)
{
    int valueEntered;

    foreach (string userValue in userEntries)
    {
        bool integerFormat = int.TryParse(userValue, out valueEntered);

        if (integerFormat == true)
        {
            if (valueEntered != 0)
            {
                checked
                {
                    int calculatedValue = 4 / valueEntered;
                }
            }
            else
            {
                throw new DivideByZeroException("Invalid data. User input values must be non-zero values.");
            }
        }
        else
        {
            throw new FormatException("Invalid data. User input values must be valid integers.");
        }
    }
}
```
```output
'Process1' completed successfully.

'Process1' encountered an issue, process aborted.
Invalid data. User input values must be valid integers.

An error occurred during 'Workflow1'.
Invalid data. User input values must be non-zero values.
```

<!-- /MarkdownTOC -->
</details>

<a id="list_collections"></a>
## List & Collections
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- List & List's built-in methods
  1. List
     - need to import List library
     ```c#
      using System.Collections.Generic;
     ```
     ```c#
      var names = new List<string> { "<name>", "Scoot", "Kendra" };
     ```
  3. Add()
     ```c#
      names.Add("John");
     ```
  4. Remove()
     ```c#
      names.Remove("John");
     ```
     
<!-- /MarkdownTOC -->
</details>

<a id="classes_objects"></a>
## Classes & Objects
<details close>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->

- Class
  ```c#
   using System;

   namespace MySuperBank
  {
      public class BankAccount
      {
          public string Number { get; }
          public string Owner { get; set; }
          public decimal Balance { get; }

          public BankAccount(string name, decimal initialBalance)
          {
             this.Owner = name;
             this.Balance = initialBalance;
          }
      
          public void MakeDeposit(decimal amount, DateTime date, string note)
          {
          }
      
          public void MakeWithdrawal(decimal amount, DateTime date, string note)
          {
          }
      }
  }
  ```
  ```c#
   using Classes;
  
   var account = new BankAccount("<name>", 1000);
   Console.WriteLine($"Account {account.Number} was created for {account.Owner} with {account.Balance} initial balance.");
  ```
  
<!-- /MarkdownTOC -->
</details>

<a id="sources"></a>
## Sources
<details open>
<summary><b>(click to expand/hide)</b></summary>
<!-- MarkdownTOC -->
   
- [Microsoft learn tutorial](https://learn.microsoft.com/en-us/training/paths/get-started-c-sharp-part-1/)
- [c# videos tutorial c#101](https://www.youtube.com/watch?v=BM4CHBmAPh4&list=PLdo4fOcmZ0oVxKLQCHpiUWun7vlJJvUiN&index=1)

<!-- /MarkdownTOC -->
</details>
