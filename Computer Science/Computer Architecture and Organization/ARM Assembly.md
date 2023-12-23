- A low-level programming language that is a human-readable representation of the machine code instructions executed by a computer's central processing unit
---
#### Glossary
- *R7*: A special [[CPU#Registers | register]] that makes calls to the [[Operating System | operating system]]
- *LR (Link Register)*: Stores the location that a function should return back to ^cacb96
- *CPSR (Current Program Status Register)*: Stores information about the program, each bit is a associated with a flag ^ed2c7f
	- Negative Flag
	- Zero Flag
	- Overflow Flag
---
#### Two's Complement: 
- A method used to represent signed integers in computers and digital systems
- The most significant bit (leftmost bit) is used as the sign bit, determining whether the number is positive or negative and the remaining bits represent the magnitude of the number
---
#### Endianness
- Endianness refers to the byte order in which the bytes of a multi-byte data are stored in computer memory
- Big-Endian:
	- The most significant byte is stored at the lowest memory address (first), and the least significant byte is stored at the highest memory address (last).
	- Example: The 32-bit integer 0x12345678 is stored in memory as 12 34 56 78 in big-endian
- Little-Endian (x86 and x86-64):
	- The least significant byte is stored at the lowest memory address (first), and the most significant byte is stored at the highest memory address (last).
	- Example: The same 32-bit integer 0x12345678 is stored in memory as 78 56 34 12 in little-endian
- ARM assembly is bi-endian, so it can support both endiannesses
---
### Instructions
- General Structure
```
.global
_start: 

.data:       @ accesses stack memory
list:        @ data structure name)
	.word 8  @ type of data: int and value: 8
```
- MOV -> Move
```assembly
MOV R0, #5   @ Decimal
MOV R1, R0
MOV R2, 0x0A @ Hexadecimal
MOV R7, #1   @ Exit code
```
! In assembly languages, [[Data Representation#^79c0a2 | binary]] values are usually represented as [[Data Representation#^94fc55 | hexadecimal]]
- SWI -> Software [[Operating System#^64825e | Interrupt]]
```assembly
SWI 0        @ Checks the value of R7
```
- LDR - Load Data into Register
```assembly
LDR R0, =list     @ Loads the address of list to R0
LDR R1, [R0]      @ Loads the value of R0 in the memory
LDR R2, [R0, #4]  @ Loads the value of R0 with a +4 byte offset, 
                    so the next word because each word has a size of 4 bytes
LDR R3, [R0, #4]! @ Pre-increments R0
LDR R4, [R0], #4  @ Post-increments R0
```
- ADD -> Addition
- SUB -> Subtraction
- MUL -> Multiplication
```assembly
ADD R3, R1, R2    @ R3 = R1 + R2
SUB R3, R1, R2    @ R3 = R1 - R2
MUL R3, R1, R2    @ R3 = R1 * R2
```
!!! If an addition operation results in overflow, [[#^ed2c7f | CPSR]]'s Overflow Flag becomes 1
!!! -2 is represented as `fffffffe` in hexadecimal, but `ffffffff` - 1 is also represented the same. Therefore, to see if the number is negative, we can look at the Negative Flag in the  [[#^ed2c7f | CPSR]] register. Subtracting with the instruction `SUBS` subtracts and also updates the Negative Flag in the [[#^ed2c7f | CPSR]] register based on the result.
- AND -> AND gate ([[Logic Gates]])
- ORR -> OR gate ([[Logic Gates]])
- EOR -> XOR gate ([[Logic Gates]])
- MVN -> Move and Negate
```assembly
MOV R0, #0xAA     @ 0x000000AA = 170
MVN R0, R0.       @ 0xffffff55 = -170
```
- LSL -> Logical Shift to the Left
- LSR -> Logical Shift to the Right
- ROR -> Rotation Shift to the Right
! There are no rotation shifts to the left
! These are **bitwise operations** that shift single bits
```
MOV R0, 0x0A.     @ 00001010 = 10
LSL R1, R0, #1    @ 00010100 = 20 (doubles)
LSR R2, R0, #1    @ 00000101 = 5  (halves)
LSR R3, R2, #1    @ 00000010 = 2. (the last 1 shifts out)
ROR R4, R2, #1    @ 10000010 = 130(the last 1 rotates to the beginning)
```
- CMP -> Compare  ^3b3679
	- Subtracts one operand from the other and updates the [[#^ed2c7f | CPSR]] registry without saving the result
	- If the Negative Flag is 0 we know that the first operand is greater than the second and vice versa
	- Also the Zero Flag is checked to see if they are equal
- BL -> Branch Linked
	- Stores the current location of the statement in the [[#^cacb96 | LR]] and moves to branch)
	- Branches are commonly used for functions  
	![[Computer Science/Computer Architecture and Organization/Memory Management#^8edada]]
- BX -> Branch to Location
	- BX LR branches back to where the  [[#^cacb96 | LR]] points
- Comparison Symbols
	- BGT -> Branch Greater Than
	- BGE -> Branch Greater Than or Equal to
	- BAL -> Branch Always
	- BLT -> Branch Less Than
	- BLE -> Branch Less Than or Equal to
	- BEQ -> Branch Equal to
	- BNQ -> Branch Not Equal to
  ! These are used after the the comparison (CMP) is done
```assembly
CMP R0, R1
BGT branch_name
```
- PUSH -> Pushes to [[Computer Science/Computer Architecture and Organization/Memory Management#Stack Memory| Stack Memory]]
- POP -> Pops From [[Computer Science/Computer Architecture and Organization/Memory Management#Stack Memory| Stack Memory]]
! These are especially useful when you want to reserve the variables that were changed in a branch