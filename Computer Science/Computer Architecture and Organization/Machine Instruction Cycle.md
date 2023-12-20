![[Machine Instruction Cycle.png  | 300]]
![[MIC Diagram.png | 500]]

#### 1. Fetching 
- The [[CPU#^0aeee0| program counter]] contains the [[Memory#Random Access Memory (RAM)| memory]] address of the next instruction to be executed
- The address is transferred to the [[CPU#^a40da3 | memory address register]] and then carried to the memory through the [[CPU#^40e646 | address bus]]
- The [[CPU#Control Unit (CU)]| control unit]] sends a signal over the [[CPU#^62759e| control bus]] to instruct the memory to read from that address
- The memory responds by sending the instruction located at that address over the [[CPU#^516a41 | data bus]]
- The fetched instruction is temporarily stored in the [[CPU#^31a1d2 | memory buffer register]] within the CPU and then transferred to the [[CPU#^69d700| instruction register]]

#### 2. Decoding 

- The [[CPU#Control Unit (CU)]| control unit]]  decodes the information in the [[CPU#^69d700| instruction register]]

#### 3. Executing 

- The [[CPU#Arithmetic Logic Unit (ALU)| arithmetic logic unit]] performs the necessary arithmetic or logic operation specified by the instruction

#### 4. Store (Optional)
 - If the instruction involves storing the result in [[Memory#Random Access Memory (RAM)| memory]], the data is written back to the appropriate location.
 - The [[CPU#^0aeee0| program counter]] is updated to point to the next instruction in memory.