- High level programming languages are necessary for humans to communicate with the computer efficiently
- In order for readable high level code to be understood by the computer, it needs to be translated into machine code or an equivalent form that can be executed

### Compilation
- **Compiler**: 
	- A compiler is a specialized program that translates the entire source code of a high-level programming language into machine code at once
	- The resulting executable file is generated before the program is run (which can be distributed without revealing the source code)

- **Steps**:
	1. *Preprocessing*: 
		- The compiler performs preprocessing tasks, such as including header files
	2. *Compilation*: 
		- The source code is translated into [[ARM Assembly | assembly]]
	3. *Assembling*:
		- The assembly code is converted into machine code ([[Data Representation#^79c0a2 | binary]])
	4. *Linking*: 
		- The compiled code is linked with libraries and other modules to produce the final executable file
	5. *Execution*: 
		- The executable file is run independently of the source code

- **Langauges**:
	- C
	- C++
	- C#
	- Java

! If there is an error, the whole program will not compile
! Compilation is slow, execution is fast

### Interpretation
- **Interpreter**:
	- An interpreter translates the source code of a high-level programming language into machine code or an intermediate code line by line 
	- The translation and execution happen simultaneously during runtime

- **Steps**:
	1. *Parsing*: 
		- The interpreter parses the source code to understand its structure
	2. *Translation*: 
		- Each line is translated into an intermediate code (such as bytecode)
	3. *Execution*: 
		- The translated code is executed immediately after translation
		- The execution involves the interpretation of the generated intermediate code 
		- This can be done either by the interpreter itself or by a [[]] designed for executing the specific intermediate code.

- **Langauges**:
	- Python
	- Javascript
	- Lua
	- Go
	- Rust
	- Zig

! If there is an error, the program will run until the line with the error is translated
! Translation is fast, execution is slow