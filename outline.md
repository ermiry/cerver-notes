# Outline

### Objective
- Main idea behind creating a dedicated framework.
- Problems that are solved by Cerver.
- Advantages of a framework written in C to work in Linux.

### Software
- Multiple software related definitions.
- Principles for writing a software that can be reliable.
- Framework related definitions.
- Write a large code-base with multiple people.
- Expose a public interface to be used to develop other applications.
- Version Control Systems.
- Tools used to manage software projects (GitHub, GitKraken, Issues, etc.).

## Server
- Server related definitions.
- Different kinds of modern servers.
- Load balancing server applications.
- Server communications and clusters.
- Working with micro-services architecture.

### Languages
- Programming language definition.
- Differences between multiple types of languages.
	- Low level and high level languages.
	- Approach in solving problems (OOP, functional, etc.).
	- Compiled vs Interpreted (Scripting) languages.
- The C Programming Language.
	- General description of the language.
	- History of the C programming language.
	- Main features and advantages over other languages.

### Compilation
- Compilation definitions in the C programming language.
- Tools used for compiling C sources (gcc, clang, make, makefile).
- Custom macros and configuration in config header.
- Divide methods by accessibility to expose an interface.
- Ability to interact with other languages (shared objects, header files).
- Importance of keeping a consistent naming convention and organization across multiple sources.

### Linux
- Linux related definitions.
- Brief history of the Linux kernel and related OS.
- Description of some core Linux Kernel components.
- Linux advantages over other OS.
	- Open Source software.
	- Development cycle.
	- Networking capabilities.
	- Interaction with the C programming language.

### Network
- Brief history of computer networks.
- Networking today (use cases in personal life and business).
- Network Components related definitions.
- Common types of networks.
- Standardization in communications and development (OSI model).

### Protocol
- Network communications protocols definitions.
- Messages related definitions (Encoding, formatting and encapsulation).
- TCP/IP Protocol Suite.

### Sockets
- Sockets descriptions, different types, and configuration.
- Data transfer in sockets.
- Challenges when working with sockets.
	- Different options to handle multiple communications (poll, dedicated threads).
	- Message queues for improved performance.
	- Transfer files using sockets (sendfile method).

### Collections
- Importance of generic collections in a framework written in C.
- Data structures definitions and principles.
- Algorithms related definitions.
- Collections that are implemented in Cerver (Lists, Stacks, Queues, Trees, Hash Tables).
- Importance of thread-safety in Cerver collections.

### Threads
- Process and threads definitions and differences.
- Libraries that enable multi-threaded applications in C.
- Thread pool related definitions.
- Thread Synchronization.
	- Problems when working with multiple threads.
	- Critical Sections and Race Conditions.
	- Mutexes and Semaphores to control flow execution.

### Security
- Possible threats and attack surfaces in modern applications.
- Authentication related definitions.
- Sessions definitions and their use cases.
- Encryption and its implementation.

### Resources
- Tools that can be used to deploy services into production.
- Cloud related definitions.
- Distributed application description (Cloud and On-Premise).
- Docker description and advantages (security, reliability, scalability) to develop code in multiple OS and ease of deployment.
- Use Docker to create micro-services in the cloud.
- Ability to create custom Dockerfiles.

### Utilities
- Importance of a built-in collection of multiple utilities.
- Multiple useful methods ended up as a dedicated utility in the framework.
- Related base64 and sha256 definitions and use cases.

### Tests
- Testing in software development related definitions.
- Different kind of tests (unit, integration, system, etc.).
- Importance of testing at every stage of development.
- Code coverage implementation.
- Tools used for automated testing.
- Performance testing (Benchmarks).

### Implementation
- Collections
	- Importance of well-written collections.
	- Internal usage and public interface.
	- Custom collections like Pool.
- Threads
	- Custom methods to work with built-in C structures.
	- Binary semaphore custom implementation.
	- Thread pool implementation and use cases.
	- Handle asynchronous methods with Job Queue and Worker.
- Types
	- Importance of having standard types definitions.
	- Custom types (single and methods pointers) with use cases.
	- Dedicated String method implementation.
- Utilities
	- General description of the collection of useful utilities methods.
	- Custom base64 and sha256 implementations with use cases.
	- Dedicated log system implementation in Cerver.
- Admin
- Authentication
- Cerver
- Client
- Connection
- Errors
- Events
- Files
- Handler
- Network
- Packets
- System
	- Custom methods to interact with host system (used space checker).
- Tests
	- General description of existent tests.
	- Implementation of unit and integration tests.
	- Automated tests in local machine and cloud when creating releases.
- Benchmarks
	- General benchmarks and comparisons with similar software.

## Examples
- Getting up and running with a basic Cerver service.
- Description and usage of Cerver specific features.
- Ability to connect multiple services together to process different kind of data.
- Create packets with custom structures to increase efficiency.
- Handle clients authentication with an external db.
- Distribute load between multiple services.
- Deploy multiple services into a production like environment.

### Results
- Actual use cases of Cerver in production deployments.
- Advantages of having a custom framework in development environment.
	- Ability to add custom features to better solve common problems.
	- Have a reliable software with a well known implementation.
	- Ability to be used for multi-purpose applications.
	- Available documentation and standardized best-practices.
	- Fast development cycle once a process has been implemented.
	- Ability to patch bugs and errors in the same organization.
- Drawbacks of maintaining a framework in a small team.
	- Critical errors in the early stage of development.
	- Slow code development while framework is developed.
	- Documentation can get behind latest release due to lack of resources.
