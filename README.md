# sysprog
CSS307 - System Programming, Fall 2018

## Weeks and Topics1. What is an operating system? What does it do? 
The OS is the most important software that runs on a computer. 
It manages memory, processes, and all software and hardware.
 We can say that the OS is a bridge between a computer and a human being. 
Because without an operating system, the computer is useless.

2. What is virtualization? 
The primary way the OS behaves itself in system is through a general technique that we call virtualization.

3.  How does an OS provide access to its features?
CPU virtualization involves a single CPU acting as if it were multiple separate CPUs.
 The most common reason for doing this is to run multiple different operating systems on one machine.
 CPU virtualization emphasizes performance and runs directly on the available CPUs whenever possible. 

4.  What illusion does a virtualized CPU provide? 
It provides some interfaces (APIs), that system calls in order to run programs. Sometimes we call them standard libraries for applications.
- How does this affect the user experience? 
A simple abstraction of CPU virtualization is provided to processes by the operating system: each process has the illusion of "owning" the CPU. 
 - How does this affect the developer experience?
It will help to developer to make time shorter to do task and divide big job into some small pieces.
 - What if the CPU were not virtualized?
It would be much harder to perform several operations together. 

5. What is a memory address? 
A memory address is a unique identifier used by a device or CPU for data tracking.
6. What is memory virtualization?
Each process accesses its own private virtual address space, which the OS somehow maps onto the physical memory of the machine.
  - Why would we want this? 
It allows us to run programs in memory even if there is insufficient memory to begin with. This is the principle behind virtual memory  
7.What happens if you write a C/C++ program that writes past the end of an array? 
 It depends if the buffer was allocated on the stack or on the heap. It also depends on the comp
uter architecture and it depends on the values that were written.
-Can this affect other programs?
The standard says that undefined behavior can mean anything, so you can't really have any expectations, not even with the same compiler. 
8.What is a thread?
 A thread is a part of the operating system, which is responsible for execution of only one instruction.
9.Why would we ever write a multi-threaded program? 
A multi-threaded application takes advantage of running multiple tasks at the same time to speed things up. Multithreading can also take advantage of multiple CPU machines.
10. What is atomicity? 
Atomic means that an operation is done without the chance for another thread to interrupt it and do something in the middle of it.
-Is a C/C++ statement atomic? 
The C standard does not define whether it is atomic or not. In practice it shows it isn't.
- Is a Java statement atomic? 
Most operations are indeed atomic. Operations involving 64 bit structures like double / long are not atomic by themselves. The 64 bit operation can be split into 2 32 bit operations.
  - Is an assembler statement atomic?
You cannot assume one machine code will execute atomically. 
11.What does persistence mean?
 In system memory, data can be easily lost, as devices such as DRAM store values in a volatile manner; when power goes away or the system crashes, any data in memory is lost. Thus, we need hardware and software to be able to store data persistently.
12.How does OS hard drive virtualization differ from CPU & memory virtualization?
 The OS does not create a private, virtualized disk for each application. Rather, it is assumed that often times, users will want to share information that is in files. 
13.How does running multiple programs at the same time increase CPU efficiency? 
Instead of just running one task at a time, the OS would load a lot of tasks into memory and switch between them, which improves CPU utilization. 
14.What is multiprogramming? 
A multiprogramming is a parallel processing in which the multiple programs can run simultaneously.




