# Linux

**From Book APUE**
An operating system can be defined as the software that controls the hardware resources of the computer and provides an environment under which programs can run. We can call this software the Kernel, since it is small and resides at the core of the environment. The interface to the kernel is a layer of system calls. Libraries of common functions are build on top of the system call interface, but applications are free to use both.

**From Book APUE**
An OS consists of the kernel and all the other software hat makes a computer useful and gives the computer its personality. This other software includes system utilities, applications, shells, libraries of common function.

Linux is the kernel used by The GNU operating system. This combination may be referenced as GNU/Linux.

**From linux.com**
The Linux OS comprises several different pieces:
- **Bootloader** The software that manages the boot process of a computer.
- **Kernel** Is the core of the system and manages the CPU, memory, and peripheral devices. The kernel is the lowest level of the OS.
- **Init system** This is a sub-system that bootstraps the user space and is charged with controlling daemons. One of the most widely used init systems is systemd, which also happens to be one of the most controversial. It is the init system that manages the boot process, once the initial booting is handed over from the bootloader (GRUB or GRand Unified Bootloader).
- **Daemons** These are background services (printing, sound, scheduling, etc.) that either start up during boot or after you log into the desktop.
- **Graphical server** This is the sub-system that displays the graphics on your monitor. It is commonly referred to as the X server or just X.
- **Desktop environment** This is the piece that the users actually interact with. There are many desktop environments to choose from (GNOME, Cinnamon, Mate, Pantheon, Enlightenment, KDE, Xfce, etc.). Each desktop environment includes built-in applications (such as file managers, configuration tools, web browsers, and games).
- **Applications** Linux offers thousands upon thousands of high-quality software titles that can be easily found and installed.

**From redhat.com**
The Linux Kernel is the main component of a Linux operating system (OS) and is the core interface between a computer’s hardware and its processes. It communicates between the 2, managing resources as efficiently as possible.

The kernel has 4 jobs:
1.  **Memory management** Keep track of how much memory is used to store what, and where.
2.  **Process management** Determine which processes can use the central processing unit (CPU), when, and for how long.
3.  **Device drivers** Act as mediator/interpreter between the hardware and processes.
4.  **System calls and security** Receive requests for service from the processes.

The kernel is invisible to the user, working in its own little world known as kernel space, where it allocates memory and keeps track of where everything is stored. What the user sees (web browsers and files) is known as the user space. These applications interact with the kernel through a system call interface (SCI).

Code executed by the system runs on CPUs in 1 of 2 modes: kernel mode or user mode. Code running in the kernel mode has unrestricted access to the hardware, while user mode restricts access to the CPU and memory to the SCI.

## Why use Linux?
Linux has evolved into one of the most reliable computer ecosystems on the planet. Combine that reliability with zero cost of entry and you have the perfect solution for a desktop platform.

### Open Source
**From linux.com**
Linux is distributed under an open source license. Open source follows these key tenants:
- The freedom to run the program, for any purpose.
- The freedom to study how the program works, and change it to make it do what you wish.
- The freedom to redistribute copies so you can help your neighbor.
- The freedom to distribute copies of your modified versions to others.

**From redhat.com**
Linux is a free, open source operating system, released under the GNU General Public License (GPL). Anyone can run, study, modify, and redistribute the source code, or even sell copies of their modified code, as long as they do so under the same license. Linux has become the largest open sources software project in the world. Professional and hobbyist programmers from around the world contribute to the Linux kernel, adding features, finding and fixing bugs and security flaws, and providing new ideas—all while sharing their contributions back to the community.

## Linux Networking

General Linux Concepts

Advantages of using Linux against other OS to create network applications?
TODO:

How does Linux handles networking?
TODO:

File Descriptors

Possible ideas to be covered in paper:
- Why everything in Linux is handled as a file?
- What are file descriptors and how are they handled in the Linux kernel?
- Avoiding the need to copy from kernel space to user space and back.
- Performance advantages of handling everything as file descriptors.
Example piping from file to socket or between sockets.
- Differences between the standard I/O and file I/O.
- What are the optional buffer sizes when performing multiple files operations?

What are file descriptors?
- Most file I/O on a UNIX system can be performed using only five functions: open, read, write, lseek, and close. These functions are often referred to as unbuffered I/O which means that each read or write invokes a system call in the kernel.
- Whenever we describe the sharing of resources among multiple processes, the concept of atomic operations becomes important.
- To the kernel, all open files are referred to by file descriptors. A file descriptor is a non-negative integer. When a file and existing file is opened or a new one is created, the kernel returns a file descriptor to the process that requested to operation.
- By convention, UNIX System associate file descriptor 0 with the standard input of a process (stdin), file descriptor 1 with the standard output (stdout), and file descriptor 2 with the standard error (stderr).
