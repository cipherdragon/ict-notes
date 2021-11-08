# Operating systems

+ Relationship between the "process" and a "program" in an OS?
    - Process is program in execution. Program can have multiple processes.
    - **"Process" is not an alternative name for "program"**

+ Requirement of "swapped out and waiting" and "swapped out and blocked" states
in the 7 state process model of an OS (2013)?
    - To **suspend a process** **temporary** to the **hard disk** in order to
   	**free the memory (memory full) to place another process in the main memory**

## Events that cause a running process to change its state

+ Termination
+ Time out (end of the time slice)
+ Block for I/O operation

## Context switching

Context switch is the process of storing the state of a process or thread, so
that it can be restored and resume execution at a later point. 

### Main actions performed during context switching

+ Store the current state of a process in a PCB.
+ Load the state of a process to be continued to the CPU from the PCB.
+ Transfer the control to the process to be continued.

## Boot process

1. Running POST (power on self test).
1. Execute BIOS.
1. Transfer the control to the OS.

## Why there's a _page table_?

This structure holds the mapping between process pages and memory frames.

## Uses of virtual memory

+ Virtual memory makes it possible to run applications that require more memory
than the physical memory.

## Common registers

+ program counter / instruction pointer
    - Store the address of the next instruction to be executed.

+ Memory buffer register / memory data register
    - Stores data being transferred from the memory for processing or the data 
    being transferred to the memory after processing.

+ Memory Address Register
    - Store the memory address to be read or write.

+ Instruction Register / Current Instruction Register
    - Holds the instruction currently being decoded or executed.

+ Accumulator
    - Store intermediate values for arithmetic and logical processing.
 
## File allocation methods

### 1. Contiguous allocation

**Space for a file** occupies a **contiguous/continous/adjacent** set of blocks
on the screen. The directory entry for a file with contiguous allocation
contains the address of starting block and the length of the allocated portion.

#### Advantages

1. Both sequential access and direct access are supported.
1. Fast due to number of seeks being limited.

#### Disadvantages

1. Suffers from fragmentation.
1. Increasing the file size is difficult as it depends on the contiguios
memory at a particular instance.
1. Finding space for a new file is difficult.

## FETCH ECECUTION cycle

+ Fetch instruction
+ Decode instruction
+ Execute instruction
1. Expected final file size must be known at the time of creation.

#### Why contiguous allocation is feasible to store files on a CD?

+ Final sizes of the files to be stored are known.
+ On a CDROM, there is no deletion of files thus there is no danger of
fragmentation.
+ There is no need to extend file sizes.

### 2. Linked List Allocation

Each file is saved as a linked list of disk blocks which doesn't need to
be contiguous. Disk blocks can scatter anywhere on the disk. Directory
entry contains a pointer to the starting and ending file blocks. Each
block contains a pointer to the next block and End-of-File marker.

#### Advantages

1. Very flexible in terms of file size. File can be expanded easily
without worring about contiguous chunks of memory.
1. No external fragmentation.

#### Disadvantages

1. Slower than contiguous allocation. (since file blocks are distributed
randomly large number of seeks are needed to access every block
individually)
1. Doesn't support random accesss or direct access. (Supports sequencial
access though).
1. Pointers required in the linked allocation incur some extra overhead.

### Indexed allocation

A special block called the index block contains the pointers to all the
blocks occupied by the file. Each file has its own index block. Directory
entry contains the address of the index block.

#### Advantages

1. Supports direct access, therefore, fast.
1. No external fragmentation.

#### Disadvantages

1. Pointer overhead is greater than linked allocation.
1. For small files (having 2 or 3 blocks), an entire block needs to be
kept for indexes.

## Virtual memory

Virtual memory is a combination of physical memory and swap memory. Instead of
directly managing memory from RAM, programs access to this virtual memory.
Mapping of virtual memory addresses to physical memory addresses is done by
special hardware in the CPU called **MMU (Memory Management Unit),** and
operating system extends the capabilities of MMU.

+ A page, memory page, or virtual page is a fixed-length contiguous block of
virtual memory, described by a single entry in the page table.
+ A page table is the data structure used by a virtual memory system in an
OS to store the mapping between virtual addresses and physical addresses. 
+ **Note: A frame is like a page, but it's a memory block allocated in physical
memory rather than virtual memory.**

![Virtual memory](https://upload.wikimedia.org/wikipedia/commons/thumb/3/32/Virtual_address_space_and_physical_address_space_relationship.svg/470px-Virtual_address_space_and_physical_address_space_relationship.svg.png)

### Reasons why a page of a process could be absent in physical memory

+ That page wouldn't have been accessed before.
+ That page would have got removed from the physical memory.

