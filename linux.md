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

**From The Linux Foundation**
The Linux kernel is one of the largest and most successful open-source projects that has ever come about. The huge rate of change and number of individual contributors show that it has a vibrant and active community, constantly causing the evolution of the kernel in response to number of different environments it is used in.

### Open Source
**From linux.com**
Linux is distributed under an open source license. Open source follows these key tenants:
- The freedom to run the program, for any purpose.
- The freedom to study how the program works, and change it to make it do what you wish.
- The freedom to redistribute copies so you can help your neighbor.
- The freedom to distribute copies of your modified versions to others.

**From redhat.com**
Linux is a free, open source operating system, released under the GNU General Public License (GPL). Anyone can run, study, modify, and redistribute the source code, or even sell copies of their modified code, as long as they do so under the same license. Linux has become the largest open sources software project in the world. Professional and hobbyist programmers from around the world contribute to the Linux kernel, adding features, finding and fixing bugs and security flaws, and providing new ideas—all while sharing their contributions back to the community.

## Linux Distribution
A Linux distribution is a version of the open source Linux OS that is packaged with other components, like an installation program, management tools, a desktop environment, and multiple user related applications.

**From TechTarget**
Linux distributions are often easier for users to deploy than the traditional open source version of Linux. This is because most distributions eliminate the need for users to manually compile a complete Linux operating system from source code, and because they are often supported by a specific vendor.

**Erick Salas**
Multiple Linux distributions are available today, some have specific targets like desktops, services, mobile, and even IOT devices. Some distributions such as Fedora and Red Hat Enterprise Linux from Red Hat, openSUSE from SUSE, Ubuntu from Canonical, and Oracle Linux from Oracle, are commercial, while others, such as Debian and Slackware, are community-developed. Some commercial distributions vendors may charge users for services like support or custom development, although open source licensing prohibits charging for the open source software itself.

**From TechTarget**
A Linux distribution also includes a package management system, which is used to install, uninstall and manage software packages. These systems also allow for package searches, automatic software upgrades and verification that all package dependencies are fulfilled.

## Linux in the Cloud
**From The Linux Foundation**
Linux runs 90 percent of the public cloud workload, 82 percent of the world's smartphones, 62 percent of the embedded market, and 99 percent of the supercomputer market.

**From redhat.com**
Linux has become the standard for highly available, reliable, and critical workloads in data centers and cloud computing environments. It supports multiple use cases, target systems, and devices, depending on user needs and workloads. Every major public cloud provider, like Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform (GCP), and Alibaba Cloud, offers multiple distributions of Linux in their marketplaces.

**From Alibaba Cloud**
Many enterprises have adopted Linux based systems as they are cost-effective, secure, scalable, open-source, and community optimized.

- **Consistent Operating Model:** No matter what version or distribution of Linux is used, whether it is on a very powerful machine or in an embedded machine, the general operation of Linux is the same. Things like process management, basic networking capabilities, command line execution are very similar.
- **Scalability:** Linux is able to very easily scale to up and down based on the available resources, which is great when developing distributed applications.
- **Networking Capabilities:** Linux has developed a string set of network capabilities, including networking tools for providing and managing to route, bridging, DNS, DHCP, network troubleshooting, virtual networking, and network monitoring.

## Linux Networking
**From Linux Kernel Labs**
The development of the Internet has led to an exponential increase in network applications and, as a consequence, to increasing the speed and productivity requirements of an operating system's networking subsystem. The networking subsystem is not an essential component of an operating system kernel (the Linux kernel can be compiled without networking support). It is, however, quite unlikely for a computing system (or even an embedded device) to have a non-networked operating system due to the need for connectivity. Modern operating systems use the TCP/IP stack. Their kernel implements protocols up to the transport layer, while application layer protocols are typically implemented in user space (HTTP, FTP, SSH, etc.).

Advantages of using Linux against other OS to create network applications?
TODO:

How does Linux handles networking?
TODO:

## File Descriptors

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
