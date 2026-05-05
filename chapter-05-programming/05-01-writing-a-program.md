# 05:01 Writing a Program

The translation from model(s) to a set of instructions that can be executed by a computer is known as **programming**. As explained before, this process is iterative because the translation can discover aspects of the problem that were not considered before, requiring updates to the original model.&#x20;

The selection of the [programming language](https://en.wikipedia.org/wiki/Programming_language) is based first on the problem's particularities, then on the programmer's preferences. For example, certain industrial environments require specific programming languages because of the machines that will run the code (e.g., [programmable logic controllers](https://en.wikipedia.org/wiki/Programmable_logic_controller)). The assumption here is that the design will be implemented in Python. Most of the techniques and conventions introduced can be applied when using any other programming language.&#x20;

### Model to Code

All aspects of a problem considered during the analysis phase are critical to program development. Now, out of the blueprint artifacts introduced in Chapter 04, the implementation diagram and pseudocode are especially important. Flowcharts and pseudocode provide a structure and outline of the code. In some cases, the jump from implementation models to instructions can be done directly, but that is not to be expected for all designs. The reader will find that Python code has a highly readable syntax that is very close to pseudocode.&#x20;

Like pseudocode, a programming language uses symbols to represent data (input) and actions to be performed on it (output). The set of rules that defines how data is represented and how instructions are encoded for execution is the **syntax** of the programming language. In general terms, there are some aspects of the syntax that each programming language addresses. In the same way that French and English are different languages, but both have the equivalent of words indicating action or _verbs_. The following list includes aspects of functionality that are provided by most programming languages' syntax.

* **Name data**: Data to be used must be stored in main memory. Syntax must facilitate the assignment of memory for saving and retrieving data. &#x20;
* **Access Hardware Devices**: The syntax must allow moving data from peripheral devices to memory (input) and from memory to peripheral devices (output).
* **Execute Arithmetic and Logic Instructions**: A syntax must exist to execute operations as basic as the ALU (Arithmetic Logic Unit). Nowadays, modern programming languages go beyond those basic operations. Syntax also must support selection and iteration to manage program decision-making.
* **Express Statements**:&#x20;
* **Name Modules**

