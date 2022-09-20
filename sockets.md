# Sockets

**From APUE - Network IPC Introduction 16.1**
The socket network IPC interface can be used by processes to communicate with other processes, regardless of where they are running, on the same machine or on different machines.

Sockets can be used as IPC (Inter Process Communication) with two or more process in the same machine, or to communicate with another computer that might be on the other side of the planet using the Internet.

**From APUE - Socket Descriptors 16.2**
A socket is an abstraction of a communication endpoint. Just as they would use file descriptors to access files, applications can use socket descriptors to interact with sockets. Socket descriptors are implemented as file descriptors in the UNIX System. Indeed, many of the functions that deal with the first type, such as read and write, can be used to interact with sockets.

**From Linux Kernel Labs**
In user space the abstraction of network communication is the socket. The socket abstracts a communication channel and is the kernel-based TCP/IP stack interaction interface. An IP socket is associated with an IP address, the transport layer protocol used (TCP, UDP, etc.) and a port. Common function calls that use sockets are: creation (socket), initialization (bind), connecting (connect), waiting for a connection (listen, accept), closing a socket (close).

Network communication is accomplished via read/write or recv/send calls for TCP sockets and recvfrom/sendto for UDP sockets. Transmission and reception operations are transparent to the application, leaving encapsulation and transmission over network at the kernel's discretion. However, it is possible to implement the TCP/IP stack in user space using raw sockets (the PF_PACKET option when creating a socket), or implementing an application layer protocol in kernel.

Different kind of sockets?
TODO:

Maybe some sockets configuration?
TODO:

## Data Transfer
**From APUE - Data Transfer 16.5**
Since a socket endpoint is represented by a file descriptor, the read and write methods can be used to communicate with the socket; however these methods do not take full advantages of the sockets capabilities; if options are to be specified to better handle data, the correct functions should be used. To transmit data the method send is used; it is similar to write, but allows the developer to specify flags to change how the data is treated. If the send method returns success, it does not necessarily mean that the process at the other end of the connection has received the data. What is guaranteed when send succeeds is that the data has been delivered to the network drivers without error.

**Extra from APUE - Data Transfer 16.5**
The send method will fail with a protocol that supports message boundaries and the program is trying to send more data than the maximum supported by the protocol. With a byte-stream protocol, the send method will block until the entire amount of data has been transmitted.

Message Queues to improve program execution (Magic Client example)
TODO:

The sendfile method
TODO:
