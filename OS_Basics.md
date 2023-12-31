# Operating Systems: Basics at a Glance

**31 - December - 2023**

## Functions of an Operating System:

1. Load and manage processes
2. Provide filesystem
3. Interact with and manage hardware through system calls
4. Provide an user–interface


* **Device Drivers**: Plug-in module for controlling external devices.
* **CPU Cores**: Processors of a CPU. 
* Intel i7: 4 cpu cores — quad core cpu.
* No. of Cores range: 2 – 18, 256, 512.


## Running Processes

**Concurrent processes**: Cores of a CPU can run many processes simultaneously by having each core alternate between processes. 

See also: Multithreading, Hyperthreading

**Hyperthreading**: Splitting a core into multiple virtual cores which can run multiple distinct threads. 

![Concurrent Processes](https://www.baeldung.com/wp-content/uploads/sites/4/2022/01/vs-1024x462-1.png "Concurrent Processes.")

* Delegation of processes to cores and running of OS processes is handled by **scheduler**.
  
**Preemptive multitasking**:

1. CPU receives interrupt (If no interrupt, System has clock which times self-interrupts often, ensuring the scheduler is invoked several times every second)
2. Interrupt saves program counter
3. Interrupt invokes handler
4. Handler saves other CPU registers (rest of process state)
5. Handler does its business
6. Handler invokes scheduler
7. Scheduler selects a process to run (Round-Robin algorithm & Priority Call)
8. Scheduler restores state for that process
9. Scheduler jumps to execution for that process.


![Memory space](https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/images/Chapter8/8_01_LogicalAddressSpace.jpg "Memory space for OS and Processes.")


## Delegation of Processes

The OS can handle any memory space it wants. External processes cannot touch memory outside its delegated memory space. To initiate requests to the OS, and to invoke requests within an address in the OS, it uses system calls, which can be called by unique system call numbers, each of which have particular instructions. 

**System calls**: Processes need to invoke certain routines within fixed addresses within the OS’s memory space. Initiating requests to the operating system. 

### Process Memory:

![Process Memory space](https://www.cs.uic.edu/~jbell/CourseNotes/OperatingSystems/images/Chapter3/3_01_Process_Memory.jpg "Process Memory space.")

Three main components:

1. **Stack**: Stores local variables pertaining to the process.
2. **Heap**: Stores everything else other than stack and text
3. **Text**: Stores the binary instructions of the process and is never changed for the duration of the program. 









