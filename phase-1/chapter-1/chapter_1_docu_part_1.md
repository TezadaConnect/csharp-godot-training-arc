## Chapter 1 Part 1

#### Download and setup .NET and VSCode

- Download and install VSCode
  
  - Mac: https://code.visualstudio.com/docs/setup/mac
  - Linux: https://code.visualstudio.com/docs/setup/linux
  - Windows: https://code.visualstudio.com/docs/setup/windows
- Download and install .NET: https://dotnet.microsoft.com/en-us/download
- Open Vscode after installation and install the following extensions
  
  - C# Dev Kit
- **Note:** Make sure that the .NET and VSCode can be accessed in the terminal (Vscode and dotnet CLI).
  
  ```sh
  # Start
  # ONLY RUN THIS CODE IN TERMINAL
  
  # E.g.: opening vscode in the current 
  # directory using terminal type: 
  code .
  
  # E.g.: creating dotnet project in terminal type: 
  dotnet new console -o my_folder
  
  # E.g.: running a console project in 
  # dotnet from vscode terminal
  dotnet run
  # End
  ```

#### Create, Compile and Execute C# programs.

- This is how you create a new console project in C#. Open to terminal and follow the instruction below:
  
  ```sh
  # Start
  # ONLY RUN THIS CODE IN TERMINAL
  
  # E.g.: creating dotnet project in terminal type: 
  dotnet new console -o chapter_one
  
  # E.g.: entering to the new project folder:
  cd chapter_one
  
  # E.g.: Opening the new project in vscode:
  code .
  
  ## End
  ```
- Look for a file called Program.cs in the file explorer in the left and click it.
- Remove all the code written in the file and paste this code snippet. Try to read and understand the snippet.
  
  ```c#
  // Start
  // ONLY PASTE THIS IN Program.cs FILE
  class Program { //<-- Name a class base on the file name
  
      static void Main(){ //<-- This is the main function which will be executed by the system automatically.
  
          string myName = "Gabby"; //<-- A variable named myName with a type of string and assigned a string "Gabby".
  
          Console.WriteLine("Hello, " + myName); //<-- Print the string in the console.
  
      } // This things must be confusing but worry not, you will learn this along the way.
  
  } 
  // End
  ```
- Open a terminal in you vscode and type the following:
  
  ```sh
  # Start
  # ONLY RUN THIS IN TERMINAL
  
  # E.g.: compile and execute the console project in dotnet Open vscode terminal and type: 
  dotnet run
  
  # End
  ```
- Terminal output should print ```Hello, Gabby```.

#### Learn some of the basic C# features necessary for every C# programs

- Let's copy this code snippet and replace our current code in our Program.cs file.
  
  ```c#
  // Start Code 1.1
  // ONLY PASTE THIS IN Program.cs FILE
  class Program {
  
      /*  
      ================================================================
          This is the Main function every program in c# starts here!
      ================================================================
      */  
      static void Main() {
  
          Console.WriteLine("Enter you name: ");
  
          string name = Console.ReadLine();
  
          Console.WriteLine("Enter you age: ");
  
          int age = Convert.ToInt32(Console.ReadLine());
  
          Console.WriteLine("My name is " + name + " and my age is " + age);
  
      }
  
  }
  // End
  ```
- Everytime we create a C# project there will be a Program.cs file, this is the starting point of the c# program.
- We will skip the ```class Program {}``` syntax because it is an advance topic.
- What we need to know for now is that the class name which is the ```Program``` should be the same name with the file name.
- Always start the file name and the class name with an uppercase letter.
- This main code includes a function signature ```static void Main()```.
- This function is a special function. When we run the program, the computer will always find this function to compile and execute it.
- The open and close curly brace ```{}``` represent a block, and everything inside it is encapsulated.
- The complete function will be written as;
  
  ```c#
  static void Main() { 
     /* Anything inside here is the function behavior */ 
  }
  ```
- A function signature has a function name, in this case the function name is ```Main```.
- Notice the class name and the function name starts with an uppercase letter. function name and class name follows a naming convention called **Pascal case**.
  
  ```c#
  // E.g: A Pascal case naming convention starts with an uppercase letter followed by lower case letters to form a word, when two words is needed, the second word first letter must be in uppercase.
  
  // YourName
  
  // StartToSink
  
  // CommonGround
  ```
- ```void``` is a type of function. There are many types of function, same goes with variable which we will discuss as the training progresses.
- ```static```, any function, classes, variable etc. that has a static on it cannot be recreated and or inherited.
- There are much more deeper explanation about ```static``` but for now let's settle for that.
- A line that starts with ```//``` is just a single line comment, programers typically use this to explain what a code is doing, the compiler ignores it and goes to another line.
- This is a multiline comment ```/* document comment */``` programmers typically use this to document a file, class or a function. It's same as the singline line but obviously it's multiline. In Code 1.1 you will find it starting at line 5 and ending in line 9

#### Discover how to output and input text information to and from the user.

- Consider the code under Code 1.1, build it and run the program by typing ```dotnet run``` in the vscode terminal.
- The terminal then asked you for your name.
- If you look up to Code 1.1, the code that has been executed was the line 12.
- The syntax ```Console.WriteLine(<string>);``` is responsible for outputting text in the terminal/console.
- We will be calling the text as string from now on, because the text is a data, and the data text such as word, sentence, or paragraph is a type of string.
- A string commonly determined with an open and close double qoutes ```"Text inside here"```
- C# has plenty of classes built out of the box to be use by programmer to make their life easier.
- One of this classes is the ```Console```. The console class has many static functions regarding to terminal/console that can be utilized by a programmer.
- One of this function is ```WriteLine(<string>)```. This function needs a string inside its parenthesis which then this string will be printed in console.
- That's the behavior of the function ```WriteLine(<string>)``` of the class ```Console```.
- After casting the ```Console.WriteLine(<string>)``` we need to add a semicolon ```;``` to end the code in a line. Forgetting this will cause an individual a head ache specially when the source code reaches 1000 lines and more.
- In line 14 of Code 1.1, there's a variable named ```name``` and it only accept data that is in type string, hence it is written as ``` string name```.
- A variable is simply a storage of data that can be access and modify anytime inside a block.
- The whole code in line 14 of Code 1.1 is written as ```string name = Console.ReadLine();```, that means we are storing a data called ```Console.ReadLine()``` to the variable ```name```.
- Notice that again we are using console class, but this time another function was utilized.
- The ```ReadLine()``` function is responsible for getting a data from one line in the console.
- This function pauses the execution of the program and waits for the user to press enter before continuing to execute the next line.
- Try to click the console and type your name, if you're satisfied press enter.
- Now it ask for your age meaning line 16 in the Code 1.1 was fired or executed.
- Again at line 18 a variable is defined, but this time it isn't string but an int.
- **Variable is defined** means making a variable and assigned a value on it to store to.
- An ```int``` is another type of data, or we will call it datatype from now on. ```int``` means Integer or a whole number from zero to positive number and or negative numbers.
- This time another class was introduced, ```Convert``` class. The convert class has a collection of functions that convert a data type into another data type.
- Here we use ```Int32(<string>)``` function. This function is responsible for converting string numeral value into integer, hence we pass the ```Console.ReadLine()``` inside its the open and close parenthesis.
- This is interesting because now we logically know that everything that we type in the console is a string.
- Again a function has many datatypes, if a variable was able to receive a string from ```ReadLine()``` that means the function is a type of string.
- And the function ```Int32(<string>)``` is a type of integer because it was stored in an integer variable.
- A void type function means it give nothing or what we called ```Null``` in programming. We will discuss about returns in function later on in this training, for now let's settle for that.
- Now write your age, if you're satisfied press enter.
- The line 20 is kinda wierd ```WriteLine(<string>);```. Here we are able to sum up all data we need to print it out in the console.
- In C# we can combine string using ```+``` sign operator, hence ```"My name is " + name + " and my age is " + age```.
- Everything is alright, but age isn't a string, how come we are able to add it into a string? The answer to that question is that C# is smart enough to determine what a programmer wanted to do. So it converted automatically into string and append it to our desired output string.
- We have a variable ```name``` and ```age``` which we store our data that inputed from console. Again a variable is a storage of data that we can modify and access. In line 20, we access the variable. In line 14 and 18 we modify the variable.

[**Return Back**]([https://](https://github.com/TezadaConnect/csharp-godot-training-arc/blob/main/phase-1/chapter-1/README.md)https://github.com/TezadaConnect/csharp-godot-training-arc/blob/main/phase-1/chapter-1/README.md) [**Next Lecture**]([https://](https://github.com/TezadaConnect/csharp-godot-training-arc/blob/main/phase-1/chapter-1/chapter_1_docu_part_2.md)https://github.com/TezadaConnect/csharp-godot-training-arc/blob/main/phase-1/chapter-1/chapter_1_docu_part_2.md)

