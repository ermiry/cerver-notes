# Threads

A thread of execution is often regarded as the smallest unit of processing that a scheduler works on. A process can have multiple threads of execution which are executed asynchronously. This asynchronous execution brings in the capability of each thread handling a particular work or service independently. Hence multiple threads running in a process handle their services which overall constitutes the complete capability of the process.

**From APUE**
A typical UNIX process can be thought of as having a single thread of control; each process is doing one thing at a time. With multiple threads of control, we can design our programs to do more than one thing a at a time withing a single process, with each thread handling a separate task. This approach can have several benefits:
- We can simplify code that deals with async events by assigning a separate thread to handle each event type.
- Multiple processes have to use complex mechanisms provided by the OS to share resources. Threads, in contrast, automatically have access o the same memory address space and file descriptors.
- With multiple threads of control, the processing of independent tasks can be interleaved by assigning a separate thread per task.

**From APUE**
A thread consists of the information necessary to represent an execution context within a process. This includes a thread ID that identifies the thread within the process, a set of register values, a stack, a scheduling priority and policy, a signal mask, an errno variable, and thread specific data.

## pthreads
**From APUE**
One of the most common threads interface is from POSIX.1-2001. The threads interfaces, also known as "pthreads" for "POSIX threads"...

**From man pages - pthreads (7)**
POSIX.1 specifies a set of interfaces (functions, header files) for threaded programming commonly known as POSIX threads.

**From Carnegie Mellon University - School of Computer Science - www.cs.cmu.edu**
The POSIX thread libraries are a standards base thread API for C/C++. It allows one to spawn a new concurrent process flow. A thread is spawned by defining a function and its arguments
which will be processed in the thread. Thread operations include thread creation, termination, synchronization (joins, blocking), scheduling, data management and process interaction.

## Thread Pool
Creating and destroying new threads can be time consuming and may slow the performance of a heavy application if it has to be done to handle every request.

A thread pool is a collection of pre-initialized threads. It facilitates the execution of N number of tasks using the same threads. If there are more tasks than threads, then tasks need to wait in a queue like structure. When any thread completes its execution, it can pickup a new task from the queue and execute it.

## Thread Synchronization
**From APUE - Thread Synchronization 11.6**
When multiple threads share the same memory, we need to make sure that each thread sees a consistent view of its data. If each thread uses variables that other threads don't read or modify, no consistency problems will exist. In the other hand, when a thread can modify a variable that is accessed by another thread, weed to synchronize the threads execution to ensure that they don't use and invalid value when accessing the shared memory space.

### Critical Section
Critical section is any piece of code that has the possibility of being executed concurrently by more than one thread of the application and exposes any shared data or resources used by the application for access.

### Race Conditions
Race conditions happen when threads run through critical sections without thread synchronization. The threads “race” through the critical section to write or read shared resources and depending on the order in which threads finish the “race”, the program output changes. In a race condition, threads access shared resources or program variables that might be worked on by other threads at the same time causing the application data to be inconsistent. These can be avoided with proper thread synchronization within critical sections by using techniques like locks, atomic variables, and message passing.

### Mutexes
**From APUE - Mutexes 11.6.1**
The data in the shared memory spaces can be protected in order to ensure access by only one thread at a time by using the pthreads mutual-exclusion interfaces. A mutex is basically a lock that is set by a thread before accessing a shared resource and released when it is done with the data. While the mutex is locked, any other thread that tries acquire the mutex will be blocked until it is released. This mutual-exclusion mechanism works only if the correct approach is being followed by the developer to design its system to follow the same data-access rules.

### Mutexes Problems
**From APUE - Deadlock Avoidance 11.6.2**
A thread might deadlock itself if it tries to lock the same mutex twice. A deadlock can also occur if it is allowed to hold a mutex and block while trying to lock a second mutex at the same time that another thread is holding while trying to lock the first mutex; in this case neither thread can't proceed with its execution as they need and unavailable resource. Deadlocks can be avoided by carefully controlling the order in which mutexes are locked. As an application grows in functionality and complexity, it becomes increasingly difficult to apply a lock ordering.

### Semaphores
**From APUE - Semaphores 15.8**
A semaphore is a counter used to provide access to a shared data object for multiple processes. When a process is done with a shared resource that is controlled by a semaphore, the semaphore values is incremented by 1. If any other processes are asleep, waiting for the semaphore, they are awakened. A common form of semaphore is called a binary semaphore. It controls a single resource, and its value is initialized to 1.
