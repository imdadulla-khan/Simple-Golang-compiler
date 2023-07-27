# Flex and Bison Program Execution

This repository contains a Flex and Bison program that performs lexical analysis and parsing of a specific language. The steps below will guide you through the process of executing the program and running the provided sample codes.

## Prerequisites

Before you begin, make sure you have the following installed on your system:

- Flex (The Fast Lexical Analyzer)
- Bison (GNU Parser Generator)
- GCC (GNU Compiler Collection)

## Execution Steps

1. Clone or download this repository to your local machine.

2. Open a terminal or command prompt and navigate to the project directory.

3. **Step 1: Lexical Analysis**

   Run the following command to generate the lexer file using Flex:

   ```bash
   flex program.l
   ```

   Flex will generate a file named `lex.yy.c`.

4. **Step 2: Parsing**

   Run the following command to generate the parser file using Bison:

   ```bash
   bison -d program.y
   ```

   Bison will generate two files: `program.tab.c` and `program.tab.h`.

   Ignore any warnings that might be displayed during this step.

5. **Step 3: Compilation**

   Compile the generated lexer and parser files along with the provided sample code using GCC:

   ```bash
   gcc lex.yy.c program.tab.c -o parser
   ```

   The compiled program will be saved as `parser`.

   Ignore any warnings that might be displayed during this step.

6. **Step 4: Run the Program**

   Execute the compiled program using the following command:

   ```bash
   ./parser
   ```

   The program will read the sample code from the provided input files and display the output.

## Sample Codes

The `samples` folder contains sample input files that you can use to test the Flex and Bison program. Modify these input files or create your own to see how the program handles different inputs.

Feel free to explore and modify the Flex and Bison files (`program.l` and `program.y`) to customize the language's lexical rules and grammar based on your requirements.
