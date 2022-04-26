# Sockets

From APUE - Network IPC Introduction 16.1
The socket network IPC interface can be used by processes to communicate with other processes,
regardless of where they are running, on the same machine or on different machines.

Sockets can be used as IPC (Inter Process Communication) with two or more process in the same machine,
or to communicate with another computer that might be on the other side of the planet using the Internet.

What is a socket?
From APUE - Socket Descriptors 16.2
A socket is an abstraction of a communication endpoint. Just as they would use file descriptors
to access files, applications can use socket descriptors to interact with sockets. Socket descriptors
are implemented as file descriptors in the UNIX System. Indeed, many of the functions that deal with
the first type, such as read and write, can be used to interact with sockets.

Different kind of sockets?
TODO:

Maybe some sockets configuration?
TODO:

Data Transfer
From APUE - Data Transfer 16.5
Since a socket endpoint is represented by a file descriptor, the read and write methods can
be used to communicate with the socket; however these methods do not take full advantages of
the sockets capabilities; if options are to be specified to better handle data, the correct functions
should be used.
To transmit data the method send is used; it is similar to write, but allows the developer to
specify flags to change how the data is treated.
If the send method returns success, it does not necessarily mean that the process at the other end
of the connection has received the data. What is guaranteed when send succeeds is that the data
has been delivered to the network drivers without error.

Extra from APUE - Data Transfer 16.5
The send method will fail ith a protocol that supports message boundaries and the program is trying
to send more data than the maximum supported by the protocol. With a byte-stream protocol,
the send method will block until the entire amount of data has been transmitted.

Message Queues to improve program execution (Magic Client example)
TODO:

The sendfile method
TODO:
