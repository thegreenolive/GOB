# 05:01 Writing a Program

The translation from model(s) to a set of instructions that can be executed by a computer is known as **programming**. As explained before, this process is iterative because the translation can discover aspects of the problem that were not considered before, requiring updates to the original model.&#x20;

The selection of the [programming language](https://en.wikipedia.org/wiki/Programming_language) is based first on the problem's particularities, then on the programmer's preferences. For example, certain industrial environments require specific programming languages because of the machines that will run the code (e.g., [programmable logic controllers](https://en.wikipedia.org/wiki/Programmable_logic_controller)). The assumption here is that the design will be implemented in Python. Most of the techniques and conventions introduced can be applied when using any other programming language.&#x20;

### Model to Code: the Language

All aspects of a problem considered during the analysis phase are critical to program development. Now, out of the blueprint artifacts introduced in Chapter 04, the implementation diagram and pseudocode are especially important. Flowcharts and pseudocode provide a structure and outline of the code. In some cases, the jump from implementation models to instructions can be done directly, but that is not to be expected for all designs. The reader will find that Python code has a highly readable syntax that is very close to pseudocode.&#x20;

Like pseudocode, a programming language uses symbols to represent data (input) and actions to be performed on it (output). The set of rules that defines how data is represented and how instructions are encoded for execution is the **syntax** of the programming language. In general terms, there are some aspects of the syntax that each programming language addresses. In the same way that French and English are different languages, but both have the equivalent of words indicating action or _verbs_. The following list includes aspects of functionality that are provided by most programming languages' syntax.

* **Name data**: Data to be used must be stored in main memory. Syntax must facilitate the assignment of memory for saving and retrieving data. &#x20;
* **Access Hardware Devices**: The syntax must allow moving data from peripheral devices to memory (input) and from memory to peripheral devices (output).
* **Execute Arithmetic and Logic Instructions**: A syntax must exist to execute operations as basic as the ALU (Arithmetic Logic Unit). Nowadays, modern programming languages go beyond those basic operations. Syntax also must support selection and iteration to manage program decision-making.
* **Express Statements**: Rules of how to order a set of instructions that can be considered a single sentence, including the data names, arithmetic, and logic performed on the data. Correct sets are called statements.&#x20;
* **Name Modules**: Syntax must exist to aggregate statements into a single module. Syntax for invoking these modules must exist (including selection, iteration, and nesting capabilities) to support structured programming.

The syntax for the Python language can be found [here](https://docs.python.org/3/reference/index.html).&#x20;

### Model to Code: Composing

Once the language's syntax is known, the designer can proceed to write the program or **source code**. The writing is done using the language's instructions, which are usually expressed in [ASCII](https://en.wikipedia.org/wiki/ASCII) or [UTF-8](https://en.wikipedia.org/wiki/UTF-8) characters (early programming languages, and some still in use, were written only in numbers). Just as a word processor facilitates the crafting of documents, some programs (Integrated Development Environment or IDE) have been developed to assist in composing code.

Although most programming languages can be written in almost any text editor, IDEs are recommended since they can catch errors, test code, manage versions, and even suggest code (AI is a common included feature). IDEs also handle the correct way to store files that contain code. Python files must be saved with the " **.py** " extension. Again, with a general-purpose text editor, coders must pay special attention when saving and manipulating files so they can be executed.

### Code to Action

The syntax of a language like Python is considered high-level relative to the language internally used in a computer. This means that the source code can be read by the programmer but not directly by the computer. Therefore, the program's high-level language must be translated into machine-readable code (ultimately represented in binary form) for execution. Compilers and interpreters are two common alternatives for this translation.

#### Compilers

Compilers translate source code into intermediate code, known as object code. As the code is translated, the syntax is checked. If syntax errors occur, a list of these errors is output to the screen, and if the errors are serious, the object code is not created. Traditional compilers will then call on another program, called a linkage editor, which links the object code written by the programmer with other object code, thereby providing access to standardized routines. The resulting code is called executable and can indeed be executed in the appropriate operating system environment. A programming language that uses a compiler does not create an executable until all syntax errors are corrected. Therefore, the program is never run until it is free of such errors. [Java](https://en.wikipedia.org/wiki/Java_\(programming_language\)) is an example of a compiler-based programming language.

#### Interpreters&#x20;

Interpreters run the program during the translation. In contrast to compilers, the translation occurs at execution time. Each statement is translated and executed. The important difference is that a traditional compiler translates the entire source code into a separate file before execution, whereas an interpreter translates at execution time.

Python utilizes a hybrid approach. When a Python script is executed, the source code is first compiled into a lower-level, platform-independent format called _bytecode_. This bytecode is then immediately interpreted and executed by the Python Virtual Machine (PVM). Nevertheless, Python is considered an interpreted language.

#### Compilers vs Interpreters

The obvious advantage of a pure compiler is execution speed, since the translation is done once and the program can thereafter be executed. Compiled programs typically run faster than interpreted programs. The disadvantage is that the executable code is tied to a particular machine or machine architecture. Interpreted code is slower to execute because of translation time, but it has the advantage of being more portable, since the translation takes place at runtime on the machine where it is executed. However, the interpreter must reside on the machine executing the program.

[The following page provides a brief history of programming languages.](05-01-writing-a-program/programming-languages-a-brief-history.md)

#### Debugging

As noted above, when syntax errors occur, the compiler or interpreter notifies the programmer. The programmer is responsible for correcting these errors in the source code and rerunning the translation steps. The act of correcting syntax errors is often called debugging the program. Although debugging syntax errors can be stressful and tedious, the process usually converges, resulting in a bug-free program as far as syntax is concerned.

Even if a program is syntactically correct, it may still not run correctly or at all. Problems that cause the program to end abnormally are called run-time errors. Problems that prevent the program from running correctly (yielding incorrect output) are called logic errors.

Run-time errors are detected when execution is attempted, and the computer informs the user of the error's nature (in Python, this is called a Traceback). Often these errors are related to accessing data, attempting to divide by zero, or passing the wrong data type. Logic errors are detected by scrutinizing the program's execution results on data for which the outcome is known. Such data is referred to as test data, and the programmer is responsible for developing such data and testing the program against it. The term debugging also refers to eliminating run-time, logic, and syntax errors from the program.

There is no recipe to follow that guarantees a program is free of bugs. Continued, methodical testing is a good approach, but the problem's complexity and the number of instructions can make debugging an endless task. Additionally, tacit requirements can cause the perception of a software behavior as a bug. For example, early ATM transactions didn't have a timeout to cancel transactions when the customer didn't provide input (i.e., customers who got the money and left the ATM without finishing the transaction and taking their card); that program behavior originated fraudulent transactions.

