# Guidelines for Python Coding

The fundamental building blocks for programs are:

* Data to be processed
* Processes or instructions acting on this data
* The interface of the program with its environment

### Types of Data

Python is a dynamically typed language, meaning the programmer does not explicitly declare the data type before assigning it; the interpreter infers it. However, the standard logical data types remain critical:

* **Numeric Data**: Data on which calculations can be performed. Values are whole numbers (represented in Python as int) or decimal numbers (represented as float). Typically used in arithmetic formulas.
* **Alphanumeric Data** (Strings): Data on which no calculations will be performed. Values are any collection of characters in the language's character set. In Python, these are called strings (str) and are enclosed in quotes. Typically used for demographic data or control data.
* **Logical** or **Boolean Data**: Data on which logical operations can be performed. Values are either True or False. Typically used in conditions for selection constructs and for iteration control.

The programmer must eventually name all the data processed in the program. These names are termed variables and are similar or identical to the data names in the design model. Identifiers (variable names) are collections of contiguous characters, usually letters or digits, concatenated with special characters such as underscores. Identifiers should be of a length to be sufficiently descriptive but not so long as to be cumbersome or verbose. Using similar notation to pseudocode is advised.

#### Literals and Data Structures

Literals are constant data values and can be numeric or non-numeric, such as numbers, characters, or strings. Examples of numeric literals are 21, 3.1415, -75, and 0. Examples of non-numeric literals are "Hello World" and "123 Main Street". Non-numeric literals are usually enclosed in quotes, apostrophes, or double quotes, depending on the language. In Python, both single (') and double (") quotes are acceptable.

Common data structures available in modern languages include arrays, files, and classes. Python uses standard data structures such as **Lists** (ordered, mutable collections of data values) and **Dictionaries** (key-value pairs). A specific value in a list is accessed by using the list name followed by an index corresponding to the value's position.

#### Global and Local Data

A structured program consists of modules. In Python, data can be declared specific to a module (or function), and only the module in which it is declared can access that data. This is known as **local data**. The only access other modules have to that data is through passing or communicating that data when invoking the module. Global data is available to all program modules. While Python supports global data, relying heavily on local data and parameter passing is considered best practice.

#### Assignment and Arithmetic Operators

A program must be able to assign values or change values in a storage location represented by a variable. The equals symbol  `=` is the mechanism for assignment. The assignment should be thought of as "replace the target data value with the value determined by the source". The target is usually to the left of the equals sign, and the source is to the right, and this symbol must not be confused with the mathematical equals.

A programming language must be able to support common arithmetic operations such as addition `+`, subtraction `-`, multiplication `*`, and division `/`. Python supports more complex mathematical operations, such as the modulus `%`) and exponentiation `**`.

#### Logical Data and Conditions

The necessity of managing or processing logical data centers based on circumstances (conditions) to determine a branch or choice of modules to execute, or to terminate (or continue) a loop. Logical data are data constrained to store only Boolean (`True`/`False`) values. The most common conditions are constructed using relational operators and logical operators.

#### Relational Operators

Conditions generally arise from the need to compare data values to determine whether the first is equal to, greater than, or less than the second, and from the negations of these conditions: not-equal, less-than-or-equal, and greater-than-or-equal. The syntax of most languages, including Python, uses the symbols `>` for greater-than, `<` for less-than, `<=` for less-than-or-equal, and `>=` for greater-than-or-equal.

A problem arises for equality because the language must be able to distinguish a test for equality from an assignment. Logical equality is written in Python using a double equal sign `==`. Logical inequality is written in Python using the combination of the exclamation point and equals `!=`. These operators are known as relational or comparison operators, and they are used to form the simplest conditions that compare two operands and return a Boolean value.

#### Logical Operators and Compound Conditions

The simplest compound conditions are the result of connecting two conditions with "and", "or", or attaching "not" to a single condition. The first is called conjunction, the second, disjunction, and the last, negation. In programming languages, these are called logical operators.

Unlike languages that use symbols like && or ||, Python opts for highly readable keywords: `and`, `or`, and `not`. They all have Boolean operands and have Boolean values.

#### Iteration and Control Flow

Beyond simple branching conditions, logic structures must allow repeated execution of code, known as iteration. In Python, this is accomplished primarily through `while` and `for` loops.

* The `while` Loop: This structure utilizes the logical conditions and Boolean evaluations mentioned earlier. A `while` loop continuously executes a target block of statements as long as its controlling condition evaluates to `True`. It is uniquely suited for scenarios where the required number of iterations is unknown before the loop begins.
* The `for` Loop: Rather than relying purely on a condition, Python's `for` loop acts as an iterator over a sequence. It steps through items in data structures (such as the strings, Lists, or Dictionaries discussed previously) one by one, executing a block of code for each element. This construct is highly efficient for data traversal and predictable, finite repetitions.

#### Procedures and Structure

The processing or procedure portion of a program is realized using statements. The statements must be placed within a framework or structure. Modules generally provide the basic mechanism for structure. Each language has its own term for modules (e.g., methods, functions, subroutines); in Python, these are primarily called _functions_ or _methods_.

Statements are the building blocks of what is termed program logic. Statements serve to assign data to storage locations, perform arithmetic and logical operations, input data from the environment, output data to the environment, and invoke modules.

Programming languages must also provide a way to insert text or dialogue to support commenting on code sections. Such comments or remarks are known as documentation and are not executable. Python uses the hash symbol `#`  for single-line comments. Interpreters simply ignore the remarks as far as translation. Remarks are inserted to provide guideposts for those attempting to follow the program's logic of the program, which is vital for later modifications.

#### Measuring the Quality of Modularity: Cohesion and Coupling

Structured analysis and design measures the goodness or quality of design with a variety of metrics. Among them are module **cohesion** and **coupling**.

Coupling is the measure of the strength of association between modules. A module becomes more complicated when it is strongly coupled to or highly interrelated with other modules, making it harder to understand, modify, or correct. Thus, loose coupling is desirable. In programming, this means that there should not be a high level of dependency between modules. Sharing data, rather than passing it, gives rise to tight coupling. A reliable metric for coupling in programming is the number of data items passed when one module invokes another.

Cohesion is the degree of connectivity among the elements that make up the module. One extreme of (undesirable) cohesion is having entirely unrelated elements in a module. A high degree of connectivity is desirable in that it simplifies the module. In programming, this means that a module should not consist entirely of unrelated statements. A rule of thumb is that the primitive module should perform a single task.

Thus, it is desirable that program modules be loosely coupled and that primitive modules be highly cohesive.
