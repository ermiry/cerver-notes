# Collections

**Erick Salas**
The main ISO C standard libraries do not provide the developers with an existent implementation of common data structures like lists, trees, hash tables, etc.

Although a problem can be solved in many different ways and data can be stored in multiple structures, the engineer is responsible of selecting the organization that best suits the applications to gain an advantage in performance and resources consumption. Some data structures are better suited for insert and remove operations while others offer greater speed when searching once the data has been added.

Cerver comes pack with a set of common data structures built-in that are in use by internal methods to perform multiple tasks. They are well tested and provide a public interface to be used by user applications, thus eliminating the need of including another package to solve common problems.

## Data Structures
**From Mastering Algorithms in C**
Data comes in all shapes and sizes, but often it can be organized in the same way.
**Efficiency:** Data structures organize data in ways that make algorithms more efficient. For example when an application requires to search trough loaded data, there might exist multiple ways to organize the information. One approach is to to place the data in an array and search by traversing element by element until the desired match is found. By using another type of data structure (hash map or tree) we can search data considerably faster.
**Abstraction:** Data structures provide a more understandable way to look at data; thus, they offer a level of abstraction in solving problems.
**Re-usability:** Data structures are reusable because they tend to be modular and context free. They are modular because each has a prescribed interface trough which access to the data structure is restricted. The data is accessed using only those operations the interface defines. Data structures are context-free because they can be used with any type of data and in a variety of situations.

In C, we make a data structure store data of any type by using void pointers to the data rather than by maintaining private copies of the data in the structure itself.

## Algorithms
**From Mastering Algorithms in C**
Algorithms are well defined procedures for solving problems. They are essential because they serve as the systematic procedures that computers require. A good algorithm does the jobs with the right amount of effort. Using the wrong algorithm or one that is not clearly defined may get the job done but it may had taken a long time.

## Cerver Collections
### Linked Lists
**From Mastering Algorithms in C**
Linked Lists are some of the most fundamental data structures. They consist of a number of elements grouped, or linked, together in a specific order. They are useful in maintaining collections of data, similar to the way that arrays are often used. However, linked lists offer important advantages over arrays. Linked lists are more efficient in performing insertions and deletions. They make use of dynamically allocated storage.

**Single linked lists:** The simplest linked list, in which elements are linked by a single pointer.
**Double linked lists:** Linked lists in which elements are linked by two pointers. This structure allows the list to be traversed both forward and backward.
**Circular linked lists:** Linked lists in which the last element is linked to the first instead of being set to NULL. This structure allows the list to be traversed in a circular fashion.

**Erick Salas**
A well implemented linked list can be used to represent other data structures with minimal effort just by adding some rules to how data is inserted and retrieved from the list.

### Stacks
**From Mastering Algorithms in C**
The distinguishing characteristic of a stack is that it stores and retrieves data in a last-in, first-out (LIFO) manner. This means that the last element placed on the stack is the first to be removed.

### Queues
**From Mastering Algorithms in C**
A queue is a data structure that stores and retrieves data in a first-in, first-out (FIFO) manner. This means that the first element placed in the queue is the first to be removed.

### Hash Tables
**From Mastering Algorithms in C**
Hash tables support one of the most efficient types of searching: hashing. A hash table consists of an array in which data is accessed via a special index called a key. The primary idea behind a hash table is to establish a mapping between the set of all possible keys and positions the array using a hash function. A hash function accepts a key and returns a hash coding. Since both computing a hash value and indexing into an array can be performed in constant time, it enables really fast searches compared to other data structures.

### Trees
Trees consist of elements called nodes organized in a hierarchical arrangement. The node at the top of the hierarchy is called the root. The nodes directly below the root are the children, which in turn, usually have children of their own. With the exception of the root, each node in the tree has exactly one parent, which is the node directly above it. The number of children a node may parent depends on the type of the tree. This number is the tree's balancing factor, which dictates how fast the tree will branch out as nodes are inserted.

## Importance of Thread-Safety in Collections
**From IBM Documentation - Thread Safety**
A function is thread-safe if you can start it simultaneously in multiple threads within the same process. A function is thread-safe only if all the functions it calls are also thread-safe.

**Erick Salas**
Developing a server requires to use multiple threads to handle multiple communications at the same time and to take advantage of all the available resources in a modern system; thus the need to create a reliable set of tools that can enable the engineers to correctly work in a multi-threaded environment using data structures that can guarantee data consistency.
