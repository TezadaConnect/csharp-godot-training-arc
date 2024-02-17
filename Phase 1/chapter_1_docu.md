## Chapter 1

### Objective

- Download and setup .NET and VSCode.
- Create, Compile and Execute C# programs.
- Learn some of the basic C# features necessary for every C# programs
- Discover how to output and input text information to and from the user.
- Understanding the concept of variables.
- Perform simple arithmetic operations in C#.

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

- This is how you create a new console project in csharp. Open to terminal and follow the instruction below:
    
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
     
        static void Main() {
         
            Console.WriteLine("Enter you name: ");
             
            string name = Console.ReadLine() ?? "Gabby";
             
            Console.WriteLine("Enter you age: ");
             
            int age = Convert.ToInt32(Console.ReadLine());
             
            Console.WriteLine("My name is " + name + " and my age is " + age);
         
        }
     
    }
    // End
    ```
 
- Everytime we create a project there will be a Program.cs file.

- Our main code of the program resides here.

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
