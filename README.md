# ch02intro
Introduction to OS, Chapter 02

Read [Introduction to OS](http://pages.cs.wisc.edu/~remzi/OSTEP/intro.pdf) and answer the following review questions.

1. **What is an operating system? What does it do?
An operating system is the most important program that runs on a computer. Every computer must have an operating system to run programs and other applications. Computer operating systems performs basic tasks, such as recognizing input from the keyboard, sending output to the display screen, keeping track of files and directories on the storage drives, and controlling peripheral devices, such as printers.
2. **What is virtualization?
Virtualization refers to the creation of a virtual version of something, virual resource, such as a server, desktop, operating system, file, storage or network.
3. **How does an OS provide access to its features?
We can run a program in operating system through both GUI and CLI. Computing devices that save data files have also file management capability. In Windows, this feature is called File Explorer, In macOS, this feature is called Finder; in Linux it’s called Files. With Chrome OS, you can access Google Drive directly or use the Files app for file management. We have many options available like copy, move, paste, delete a file. We have also a search box through which we can search different files, folders, programs.
4. **What illusion does a virtualized CPU provide?
The illussion that the system has a very large number of virtual CPU's which is turning a single CPU into a seemingly infinite number of CPU's and this allows to many program run at the same time.
    - **How does this affect the user experience?
    It will be more easy to use more programs in the same time, don't have some bugs and so on.
    - **How does this affect the developer experience?
    We know that when we run one or more programs we should save some data to a memory, it would be more times bigger, and in this memory we also have temporary data. That is why we need virtual memory. And will be harder to realize for developer but easy to use user.
    - **What if the CPU were not virtualized?
    It gives us some problems with operating system, also have some bugsin software and so on.
5. **What is a memory address?
Memory adresses are fixed-length sequences of digits conventionally displayed and manipulated as unsigned integers.
6. **What is memory virtualization?
In computer science, memory virtualization decouples volatile random access memory resources from indivisual systems in the data center, and then aggregates those resources into a virtualized memory pool available to any computer in the cluster.
    - **Why would we want this?
    To begin the execution of program, the entire program need not be loaded into memory. As and when CPU makes references, and if the physical pages corresponding to those references are not present in DRAM, then system generates a page fault - the physical page of memory that needs to be accessed is not resident in memory.
8. **What happens if you write a C/C++ program that writes past the end of an array?
The practical answer is it depends. It depends if the buffer was allocated on the stack or on the heap. It also depends on the computer architecture and it depends on the values that were written.In the bad old days before protected mode memory architectures, this was a big problem. Since all the processes could write to all the memory space it was fairly easy for one badly behaved poorly written process to corrupt memory.
      - **Can this affect other programs?
      The behavior is only undefined from the language perspective. The c++ standards committee doesn't want compiler vendors to gave to be responsible for the exact failure mode once you write and execute some buggy/dangerous code. So UB is the legal phrase that frees the compiler vendor from any liability.
9. **What is a thread?
You can think of a thread as a function running within the same memory space as other functions, with more than one of them active at a time.
10. **Why would we ever write a multi-threaded program?
Unfortunately, the problems of concurrency are no longer limited just to the OS itself. Indeed, modern multi-threaded programs exhibit the same problems.
11. **What is atomicity?
Atomicity is a feature of databases systems dictating where a transaction must be all-or-nothing. That is, the transaction must either fully happen, or not happen at all. It must not complete partially.
    - **Is a C/C++ statement atomic?
    Use atomic operations like Interlocked on Windows and the equivalent on Linux. C++ will have an "atomic" template to wrap these in a nice and cross-platform interface.
    - **Is a Java statement atomic?
    Yes, because any looping or conditional construct is a java statement.
    - **Is an assembler statement atomic?
    It depends. Here is some confusion around, what an assembler instruction is. Normally, one assembler instruction is translated into exactly one machine instruction. The excemption is when you use macros -- but you should be aware of that.

13. **What does persistence mean?
The perisistence we need to hardware and software to be able to store  data perisistenly; such storage is thus critical to anu system as users care a great deal about their data.

14. **How does OS hard drive virtualization differ from CPU & memory virtualization?
Virtual memory is a memory management capability of an OS that uses hardware and software to allow a computer to compensate for physical memory shortages by temporarily transferring data from random access memory to disk storage. And the distributed memory pool can then be utilized as a high-speed cache, a messaging layer, or a large, shared memory resource for a CPU or a GPU application.
15. **How does running multiple programs at the same time increase CPU efficiency?
In computing, multitasking is the concurrent execution of multiple tasks  over a certain period of time. New tasks can interrupt already started ones before they finish, instead of waiting for them to end. As a result, a computer executes segments of multiple tasks in an interleaved manner, while the tasks share common processing resources such as central processing units  and main memory. 
16. **What is multiprogramming?
The multiprogramming became commonplace due to the desire to make better use of machine resources.Instead of just running one job at a time, the OS would load a number of jobs into memory and switch rapidly between them, thus improving CPU utilization.
A multiprogramming is a parallel processing in which the multiple programs can run simultaneously. We all mostly use uniprocessor PC/Mobile/Tablet but never wonder how the processor works.
