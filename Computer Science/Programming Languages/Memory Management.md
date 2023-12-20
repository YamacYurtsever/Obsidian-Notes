- Allocating and deallocating memory resources effectively to ensure that programs run smoothly without memory-related issues like leaks or access violations

- **Garbage Values**: 
	- Undefined or unpredictable data stored in a variable or memory location
	- When a variable is declared but not initialized with a specific value, or when a variable is used before it is assigned a value, the variable may contain whatever data happened to be in that memory location at the time
	- This data could be leftover from previous operations, or it might be arbitrary values that were present in the memory

- **Nul**l:
	- A value that represents the absence of a meaningful or valid value in programming
	- It is often used to indicate that a variable or pointer does not point to any memory location or the failure of a memory allocation request

### Automatic Memory Management (Garbage Collection):
-  The runtime environment is responsible for allocating and deallocating memory automatically, identifying and reclaiming memory that is no longer in use
- This reduces the risk of memory leaks, but it introduces some overhead
- E.g.: Python, Javascript, Java

### Manual Memory Management
- The programmer has explicit control over allocating and deallocating memory
- While this provides flexibility, it also introduces the risk of memory leaks and dangling pointers if not handled carefully
- E.g.: C, C++

#### Memory Management in C

- **Reference Operator: &** 
	- Tells the address of a [[Variables | variable]] in [[Memory | memory]]

- **Dereference Operator: \***
	- Goes to a specific address and retrieves the data

- **Pointer: datatype \*name**
	- A variable that contains the memory address of a value in the computers memory 
	- The `*` is used to indicate that the variable is a pointer, not the dereference operator

- **Malloc** 
	- Allocates Memory 
	- Inputs the number of [[Data Representation#^ff39e6 | bytes]]
	- sizeof(datatype) tells how many [[Data Representation#^ff39e6 | bytes]] a data type is

- **Free** 
	- Deallocates (Frees) Memory 
	- Inputs the pointer or memory block to deallocate

#### Dynamic Memory Allocation