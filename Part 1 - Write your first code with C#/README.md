<h2 align="center">
    Write your first C# code 
</h1>

In this module, I learnt: 
- To write my first lines of C# code.
- Two different techniques to print a message as output.
- To diagnose errors when code is incorrect.
- Identify different C# syntax elements like operators, classes, and methods.

### The difference between Console.Write / WriteLine (Notes) 
- Console.WriteLine() prints a message to the output console. At the end of the line, it adds a line feed similar to pressing Enter or Return to create a new line.<br>
- To print to the output console, but without adding a line feed at the end, you use the second technique, Console.Write(). 

Example:<br>
<i>Code</i><br>
```c#
`Console.Write("Congratulations!");
`Console.Write("You wrote your first lines of code.");
```

<i>Output</i><br>
```
Congratulations!You wrote your first lines of code.
```

<i>Code</i><br>
```c#
`Console.WriteLine("Congratulations!");
`Console.Write("You wrote your first lines of code.");
```
<i>Output</i><br>
```c#
Congratulations!
You wrote your first lines of code.
```

<h2 align="center">
    Store and retrive data using literal and variable values
</h1>

In this module, I learnt: 
- To create literal values for five basic data types
- To declare and initialize variables
- To retrieve and set values in variables
- To allow the compiler to determine the data type for your variable when initializing

###  Display literal and variable values (Challenge)
1. Store the following values in variables using the correct data type: 
- Bob
- 3
- 34.4
2. Write code to display the following message:<br>
```
Hello, Bob! You have 3 messages in your inbox. The temperature is 34.4 celsius.
```

<i>Code</i><br>
```c#
string firstName = "Bob";
int firstNumber = 3;
decimal secondNumber = 34.4m;
Console.Write("Hello, " + firstName + "!" + " You have " + firstNumber + " messages in your inbox. The temperature is " + secondNumber + " celsius.");
```

<i>Output</i><br>
```
Hello, Bob! You have 3 messages in your inbox. The temperature is 34.4 celsius.
```

<h2 align="center">
    Basic string formatting
</h1>

In this module, I learnt: 
- To create string data containing tabs, new lines, and other special characters
- To create string data containing Unicode characters
- To combine string data into a new string value via concatenation
- To combine string data into a new string value via interpolation

###  Character escape sequences (Notes)
- `\n` adds a new line. `\t` adds a tab.

Example:<br>
<i>Code</i><br>
```c#
Console.WriteLine("Hello\nWorld!");
Console.WriteLine("Hello\tWorld!");
```

<i>Output</i><br>
```
Hello<br>
World!<br>
Hello   World!<br>
```

- To insert a double-auotation mark in a literal string, use `\"`.

Example:<br>
<i>Code</i><br>
```c#
Console.WriteLine("Hello "World"!"); // Wrong
Console.WriteLine("Hello \"World\"!"); // Correct
```

<i>Output</i><br>
```
Hello "World"!
```

- To display a file path, use `\\` to display a single backslash.

Example:<br>
<i>Code</i><br>
```c#
Console.WriteLine("c:\source\repos"); // Wrong
Console.WriteLine("c:\\source\\repos"); // Correct
```

<i>Output</i><br>
```
c:\source\repos
```

###  Verbatim string literal (Notes)
- A verbatim string literal will keep all whitespace and characters without the need to escape the backslash, use `@` before the literal string.

Example:<br>
<i>Code</i><br>
```c# 
Console.WriteLine(@"    c:\source\repos    
        (this is where your code goes)");
```

<i>Output</i><br>
```
c:\source\repos    
        (this is where your code goes)
```

###  String interpolation (Notes)
- Interpolation expression is indicated by an opening and closing curly brace symbol `{}`. 
- The literal string becomes a template when it's prefixed by the `$` character.

Example:<br>
<i>Code</i><br>
```c# 
string firstName = "Bob";
string greeting = "Hello";
string firstMessage = greeting + " " + firstName + "!";
string secondMessage = $"{greeting} {firstName}!"; // More concise line of code
Console.Write(secondMessage);
```

<i>Output</i><br>
```
Hello Bob!
```

###  Combine verbatim liters and string interpolation (Notes)
- You can use both the verbatim literal prefix symbol `@` and the string interpolation `$` symbol together.
- The `$` symbol allows you to reference the projectName variable inside the braces, while the `@` symbol allows you to use the unescaped `\` character.

Example:<br>
<i>Code</i><br>
```c# 
string projectName = "First-Project";
Console.WriteLine($@"C:\Output\{projectName}\Data");
```

<i>Output</i><br>
```
C:\Output\First-Project\Data
```

###  Format and display instructions (Challenge)
1. Solve the challenge with the two following lines of code:
```c# 
string projectName = "ACME";
string russianMessage = "\u041f\u043e\u0441\u043c\u043e\u0442\u0440\u0435\u0442\u044c \u0440\u0443\u0441\u0441\u043a\u0438\u0439 \u0432\u044b\u0432\u043e\u0434";
```
2. Use either the Console.WriteLine() or the Console.Write() method twice.
3. Write code to display the following message:<br>
```
View English output:
  c:\Exercise\ACME\data.txt

Посмотреть русский вывод:
  c:\Exercise\ACME\ru-RU\data.txt
```
<i>Code</i><br>
```c# 
string projectName = "ACME";
string russianMessage = "\u041f\u043e\u0441\u043c\u043e\u0442\u0440\u0435\u0442\u044c \u0440\u0443\u0441\u0441\u043a\u0438\u0439 \u0432\u044b\u0432\u043e\u0434";
string englishMessage = "View English output:";

Console.WriteLine(englishMessage + "\n" + "\t" + $@"C:\Exercise\{projectName}\data.text" + "\n");
Console.Write(russianMessage + "\n" + "\t" + $@"C:\Exercise\{projectName}\data.text");
```

<i>Output</i><br>
```
View English output:
	C:\Exercise\ACME\data.text

Посмотреть русский вывод
	C:\Exercise\ACME\data.text
```

<h2 align="center">
    Basic operations on numbers
</h1>

In this module, I learnt: 
- To perform mathematical operations on numeric values
- To observe implicit type conversion between strings and numeric values
- To temporarily convert one data type into another

