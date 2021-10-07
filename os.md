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
