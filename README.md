# ch02intro
Introduction to OS, Chapter 02

Read [Introduction to OS](http://pages.cs.wisc.edu/~remzi/OSTEP/intro.pdf) and answer the following review questions.
1. **What is an operating system? What does it do?** Operating system - a software module that is responsible for simplifying the launch of programs and for ensuring that the system works correctly and efficiently.
Allows programs to share memory and interact with devices and other entertainment like that. The OS also provides some interfaces (APIs). OS - Resource Manager
2. **What is virtualization?** OS takes a physical resource and converts it into a more general, powerful and convenient to use virtual form. OS takes a physical resource and converts it into a more general, powerful and convenient to use virtual form. OS can also be called virtualization
3. **How does an OS provide access to its features?** A typical OS, in fact, exports several hundred system calls available for applications. Because the OS provides these calls to run programs, access memory and devices, and other related activities, we also sometimes say that the OS provides a standard library for applications. Finally, since virtualization allows you to run many programs (thus sharing CPUs), and many programs simultaneously access their own instructions and data (thus sharing memory) and many programs for accessing devices (thus dividing disks etc.) 
4. **What illusion does a virtualized CPU provide?** The illusion that one CPU turns into an infinite number of CPU's and allows you to run several programs at once.
    - **How does this affect the user experience?** To run programs, they must be stopped by some interfaces (APIs). The APIs are the main way for most users to interact with operating systems.
    - **How does this affect the developer experience?** Since you can run multiple processors at the same time, it speeds up the developer experience
    - **What if the CPU were not virtualized?**  If the processor is not virtualized, then questions will arise which program should work if two programs want to work at a certain time
5. **What is a memory address?** Memory is an array of bytes. To read this byte array, you need to specify an address so that you can access the data stored there; To write or update the memory, you must also specify the data that must be written to this address.
A memory address is a unique identifier used by a device or CPU for data tracking.
6. **What is memory virtualization?** Memory virtualization separates volatile random access memory (RAM) resources from individual systems in the data center, and then combines these resources into a virtual memory pool.
Virtualized memory is when each process accesses its own virtual address space, which the OS somehow displays in the physical memory of the machine. Each running program has a physical memory for itself
    - **Why would we want this?** Each running program has its own personal memory in order to use one physical memory with other programs running. It control save memory. If physical memory runs out, it stores information on the hard disk.
8. **What happens if you write a C/C++ program that writes past the end of an array?**  When the translator of the source code does certain assumptions, but these assumptions are not satisfied during execution. There may be two variants: Access not issued location of memory and Segmentation fault.
      - **Can this affect other programs?** Only in two cases: 1. Access non allocated location of memory and  2. Segmentation fault
9. **What is a thread?** A thread is smallest sequence of programmed instructions that can be managed independently by a scheduler, which is typically a part of the operating system.
10. **Why would we ever write a multi-threaded program?** It gives us a useful abstraction of concurrent execution.A single process can have many different "functions" executing concurrently, so the application may efficiently use the available hardware. 
11. **What is atomicity?** It is database transactions which are guaranteed to either completely occur, or have no effects.
    - **Is a C/C++ statement atomic?** No
    - **Is a Java statement atomic?** yes
    - **Is an assembler statement atomic?** yes
13. **What does persistence mean?** Persistance  is data that outlives the process that created it which refers to storing anything to any level of persistence using.
14. **How does OS hard drive virtualization differ from CPU & memory virtualization?** Hard Drive: Like a physical hard drive, a virtual hard drive file contains a file system, and it can contain an operating system, applications and data. Virtual hard drive files are normally attached to virtual machines (VMs), and function as system or data drives for the VM.
CPU&Memory: Each virtual machine appears to run on its own CPU (or a set of CPUs), fully isolated from other virtual machines. Registers, the translation look aside buffer, and other control structures are maintained separately for each virtual machine
15. **How does running multiple programs at the same time increase CPU efficiency?** Direct proportionality: the more program are running, the more program executed successfully.
16. **What is multiprogramming?** Multiprogramming is a rudimentary form of parallel processing in which several programs are run at the same time
