The [[Operating System]] manages the memory:
![[Operating System#Memory Management]]

#### Stack Memory
- Typically used for storing **local variables and functions** (variables with a limited scope)
- Memory is **automatically allocated and deallocated** as functions are called and returned ^8edada
- It follows the **last-in-first-out (LIFO)** order (e.g. recursive functions)

#### Heap Memory
- Typically used for **dynamic memory allocation** for storing variables with a longer lifetime or unknown size at compile time (like data structures created with `malloc`) are often stored in the heap
- Memory in the heap needs to be explicitly managed by the programmer (allocated and freed)

#### Overflow
- When more memory is written to either [[#Heap Memory]] or [[#Stack Memory]]  than they can hold, it can exceed into the other's boundaries. This overflow can result in specific issues:
- **Heap Overflow**: Occurs when more data is written to dynamically allocated memory in the heap than it was originally allocated to hold
- **Stack Overflow**: Occurs when the call stack exceeds the available stack space, often due to excessive function calls
- Both heap and stack overflows are instances of **buffer overflow**

![[Memory Management 2023-12-17 12.35.04.excalidraw | 250]]
