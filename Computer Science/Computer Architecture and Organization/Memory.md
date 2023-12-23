### Primary Memory & Secondary Memory

| Primary (Main) Memory                            | Secondary Memory                                                             |
| ------------------------------------------------ | ---------------------------------------------------------------------------- |
| Short term storage                               | Long term storage                                                            |
| Contains less data                               | Contains more data                                                           |
| Faster to access ([[Memory Acess Order \| MAO]]) | Slower to access ([[Memory Acess Order \| MAO]])                             |
| Can be directly accessed by the CPU at run time  | First needs to be transferred to the main memory to be accessible by the CPU |
| E.g.: RAM, ROM and Virtual Memory                | E.g.: Hard drives, SSDs, USBs, CDs, Cloud Storage                            | 

---

### Random Access Memory (RAM)
- Where data is stored at runtime
- Can be written and read quickly
- Volatile (information is lost when power is turned off)

### Read Only Memory (ROM)
- Contains instructions, that are written in manufacturing, for booting the computer
- Can be read but can't be written easily
- Non-volatile (information is not lost when power is turned off)

### Virtual Memory
- Utilized when RAM is fully occupied, to extend available memory
- The [[Operating System | operating system]] temporarily transfers data from RAM to a designated space on the hard drive
- Contains the less important or less frequently accessed data
- Slower than RAM

---

#### Non-Volatile Memory
- Non-volatile storage devices can hold data even when power is turned off
- In hard disks this is done through magnetic storage to store data on spinning disks
	- The read/write heads on the drive can magnetize specific regions on the disk to represent binary data (0s and 1s)
	- Since the magnetic state of these regions persists even when the power is off, the data remains intact.
- In SSDs and USBs this is done through flash memory
	- Flash memory is made up of memory cells which can store a bit of information (0 or 1)
	- When data is written to a flash memory cell, an electric charge is applied to the floating gate which traps electrons, changing the electrical characteristics of the cell
	- The presence or absence of a charge represents the binary data (0 or 1)

