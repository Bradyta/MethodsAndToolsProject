Lesson 1: Structure of a C++ Program
==========

Welcome to Lesson 1 of C++ tutorials! This lesson will introduce the basic structure of a C++ program. You will also implement your first program called "Hello World". Although it is a very simple, it contains the fundamental components of a C++ program.

Hello World
---------

The best way to learn a programming language is by writing programs. Here, we have a basic program that prints "Hello World" (which is typically the first program that beginners write). We have broken down the program line by line to discuss what each component of our program does.

	//my first program in C++
	#include <iostream>
	
	int main()
	{
		std::cout << "Hello World!";
	}

+ **Line 1: // My first program in C++**:
The two slash signs, "//"  indicate that the line is a comment by the programmer. Typically, programmers use these comments as observations or descriptions of the program or function that succeeds the comment. Comments have no effect on the behavior of the program itself, but they are useful tools that help the user understand what the actual code is doing. In this example, the comment just states what the name of the program is.

+ **Line 2: #include <iostream>**:
Lines beginning with a hash sign (#) are directives read and interpreted by what is known as the preprocessor. They are special lines interpreted before the compilation of the program itself begins. In this case, the directive #include <iostream>, instructs the preprocessor to include a section of standard C++ code, known as header iostream, that allows to perform standard input and output operations, such as writing the output of this program (Hello World) to the screen.

* **Line 3: A blank line.**:
Blank lines have no effect on a program. They simply improve readability of the code.

* **Line 4: int main ()**:
This line initiates the declaration of a function. A function is a section of code that performs a certain task. Every function is given first be a data type: in this case is **int**. After the data type is declared, the function is given a name: in this case, the name given is **main**. The name of functions are introduced with a succession of a type of data that they are processing. The **()** following main are parameters. The function named main is a special function in all C++ programs; it is the function called when the program is run. The execution of all C++ programs begins with the main function, regardless of where the function is actually located within the code. We will discuss functions in greater detail in a later chapter.
* **Lines 5 and 7: { and }**:
The open brace **{** at line 5 indicates the beginning of main's function definition, and the closing brace **}** at line 7, indicates its end. The statements within the brackets form defines what happens when main is called. All functions use braces to indicate the beginning and end of their definitions.

+ **Line 6: std::cout << "Hello World!";**:
This line is a C++ statement. A statement is an expression that can actually produce some effect. It specifies what the program does, essentially encapsulating the bulk of the program. Statements are executed in the same order that they appear within a function's body.

This statement has three parts: 

1. **std::cout** Identifies the standard character output device (usually, this is the computer screen). 

2. **<<** Is the insertion operator. This indicates what follows **<<** is inserted into std::cout. 

3. **"Hello world!"** The sentence we wish to print within quotes. This sentence is the content inserted into the standard output. Be sure to include the quotation marks!

Notice that the statement ends with a semicolon (;). Similar to how a period ends a sentence in English, a semicolon marks the end of a statement in C++. All C++ statements must end with a semicolon character. One of the most common syntax errors in C++ is forgetting to end a statement with a semicolon.




Comments
---------

As noted above, comments do not affect the operation of the program. Though they do not change the nature of the program itself, they are useful tools to document the source code directly on what the program does and how it operates.

C++ supports two ways of commenting code
	
	//line comment
	/* Block Comment */

1. **Line Comments**: Line comments discard everything from where the pair of slash signs (//) are found up to the end of that same line. 
2. **Block Comments**: Block comments discard everything between the /* characters and the first appearance of the */ characters, with the possibility of including multiple lines.

As a programmer, it is always good to practice using comments often. Generally, we use comments in functions to help us understand and keep track of what the program is doing. Let's practice by adding comments to the "Hello World" program we previously implemented.

	//my first program in C++
	#include <iostream>
	
	int main()
	{
		std::cout << "Hello World!"; //standard output stream that takes and prints "Hello World"
	}



Using namespace std
--------

More often than not, there are generally multiple ways to write and implement code that yield in the same results. As you begin to write more code, you will develop your own style to implementing programs that will differ from other programmers. For this lesson, we will show you how to implement your own "Hello World" program without using **std::cout**.

If you have seen C++ code before, you may have seen cout being used instead of std::cout. Both name the same object. The first one uses its unqualified name **(cout)**, while the second qualifies it directly within the namespace std **(std::cout)**.

**cout** is part of the standard library, and all the elements in the standard C++ library are declared within what is a called a namespace: the namespace std.

In order to refer to the elements in the std namespace, a program shall either qualify each and every use of elements of the library (as we have done by prefixing cout with std::), or introduce visibility of its components. The most typical way to introduce visibility of these components is by means of using declarations:
	
	using namespace std;

The above declaration allows all elements in the std namespace to be accessed in an unqualified manner (without the std:: prefix).

We can implement the Hello World program using std namespace in an unqualified manner. Running the program will yield the same results as our previous implementation, but we see that this version has improved readability.

	// my second program in C++
	#include <iostream>
	using namespace std;

	int main ()
	{
		cout << "Hello World! ";
	}

Assignment #1: Hello World
--------

For our first practice assignment, we will implement our own version of our "Hello World" program.
Open the **HelloWorld.cpp** file and edit/implement your code there.

In order to pass the test file, your code must include a function **int main()** that:

1. Prints **Hello World** 
2. Prints **This is my first C++ program**.

Remember that C++ is a case sensitive language and that spelling matters, so be sure to double check your work before running the test file.

Good luck!
