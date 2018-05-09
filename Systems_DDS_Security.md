---
layout: default
---

[Home](index.md)


## [](#header-2)Linux Barrier Mechanism for multi threaded program
[Link to Github Repo](https://github.com/jadhavhninad/Linux-Barrier-Mechanism-for-multi-threaded-program).

### [](#header-3) Goals:
To Develop a barrier synchronization mechanism in Linux kernel which can be invoked by user processes via system call interface. The mechanism consists of 3 Linux kernel system calls which are resemble to the pthread barrier i.e barrier-init, barrier-wait, barrier_destroy

### [](#header-3) Implementation:
A barrier synchronization synchronization mechanism was developed in Linux kernel which can be invoked by user processes via system call interface. The mechanism consists of 3 Linux kernel system calls which are resemble to the pthread barrier:

*   barrier_init(unsigned int count, unsigned int *barrier_id, signed int timeout) – to initiate a barrier in the caller’s address space. 

*   barrier_wait(unsigned int barrier_id) – to wait for a barrier synchronization.

*   barrier_destroy(unsigned int barrier_id) – to destroyed the barrier of the id barrier_id.

Since Linux system calls are statically defined and compiled into the kernel, the kernel was rebuilt with new system calls. To demonstrate your barrier implementation, a testing program was developed. The testing program forks two child processes. In each child process, there are 5 threads to exercise the 1 st barrier and additional 20 threads use the 2nd barrier. Each thread sleeps a random amount of time.

### [](#header-3) Output:
*   New Kernal image.

<br><br>
## [](#header-2)Dynamic Instrumentation In Kernel Modules
[Link to Github Repo](https://github.com/jadhavhninad/Kprobes-on-RB-tree-kernel-data-structure).

### [](#header-3) Goals:
Linux has static and dynamic tracing facilities with which callback functions can be invoked when trace points (or probes) are hit. A kernel module was developed that uses kprobe API to add and remove dynamic probes in any kernel programs. With the module’s device file interface, a user program can place a kprobe on a specific line of kernel code, access kernel information and variables.

### [](#header-3) Implementation:

!["Implementation Schema"]({{ site.url }}/assets/images/kprobes.png)


### [](#header-3) Output:
Trace data items to be collected by kprobe handler
*   the address of the kprobe, the pid of the running process that hits the probe, 
*   time stamp (x86 TSC), 
*   rb_object objects traversed in the RB tree while performing the corresponding functions

<br><br>
---










