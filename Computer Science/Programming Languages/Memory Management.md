- Allocating and deallocating memory resources effectively to ensure that programs run smoothly without memory-related issues like leaks or access violations

- **Garbage Values**: 
	- Undefined or unpredictable data stored in a variable or memory location
	- When a variable is declared but not initialized with a specific value, or when a variable is used before it is assigned a value, the variable may contain whatever data happened to be in that memory location at the time
	- This data could be leftover from previous operations, or it might be arbitrary values that were present in the memory

- **Null**:
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

- **Reference Operator : `&`** 
	- Tells the address of a [[Variables | variable]] in [[Memory | memory]]

- **Dereference Operator: `*`**
	- Goes to a specific address and retrieves the data

- **Pointer: `datatype* name`**
	- A variable that contains the memory address of a value in the computers [[Memory | memory]] 
	- The `*` is used to indicate that the [[Variables | variable]] is a pointer, not the dereference operator

- **Arrow Operator: `->`**
	- When you have a pointer to a structure, you use the arrow operator to access its members
	- It is equivalent to `(*pointer).member`

- **Malloc** 
	- Allocates Memory 
	- Inputs the number of [[Data Representation#^ff39e6 | bytes]]
	- sizeof(datatype) tells how many [[Data Representation#^ff39e6 | bytes]] a data type is

- **Free** 
	- Deallocates (Frees) Memory 
	- Inputs the pointer or memory block to deallocate

#### Dynamic Memory Allocation
```C
int m;
int* a = null;
int* b = malloc(sizeof(int));
```
![[Memory Management 2023-12-21 01.10.51.excalidraw | 200]]
```C
a = b;
m = 10;
*a = m + 3;
```
![[Memory Management 2023-12-21 01.17.43.excalidraw | 200]]
```C
free(b)
```
![[Memory Management 2023-12-21 01.20.14.excalidraw | 200]]

#### Static vs Dynamic Memory Allocation
- Say we have a struct called node
```C
node node1; 
// Static Memory Allocation -> Stack Memory
node* node2 = malloc(sizeof(node)) 
// Dynamic Memory Allocation -> Heap Memory
```
- Both statements functionally achieve the same thing
- However, [[Computer Science/Computer Architecture and Organization/Memory Management#Heap Memory | heap memory]] is usually larger [[Computer Science/Computer Architecture and Organization/Memory Management#Stack Memory | stack memory]]
