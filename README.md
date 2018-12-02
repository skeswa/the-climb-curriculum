# The Climb Curriculum
Curriculum for those bold enough to attempt the climb

## Data Structures
## 1. Linked List
### Description
In computer science, a Linked list is a linear collection of data elements, whose order is not given by their physical placement in memory. Instead, each element points to the next. It is a data structure consisting of a collection of nodes which together represent a sequence. In its most basic form, each node contains: data, and a reference (in other words, a link) to the next node in the sequence. This structure allows for efficient insertion or removal of elements from any position in the sequence during iteration. More complex variants add additional links, allowing more efficient insertion or removal of nodes at arbitrary positions. A drawback of linked lists is that access time is linear (and difficult to pipeline). Faster access, such as random access, is not feasible. Arrays have better cache locality compared to linked lists.

![Linked list image](https://upload.wikimedia.org/wikipedia/commons/6/6d/Singly-linked-list.svg)

### Prompt
#### Pre-requisites
##### The C Programming Language 2nd Edition
- Most of _A Tutorial Introduction_ **(1.2 - 1.10)**
- All of _Types, Operators, and Expressions_ **(2.1 - 2.12)** 
- Most of _Control Flow_ **(3.1 - 3.6)**
- All of _Functions and Program Structure_ **(4.1 - 4.11)**
- Most of _Pointers and Arrays_ ***(5.1 - 5.6, 5.11)**
- Most of _Structures_ **(6.1 - 6.7)**

#### Core Features
You must create a Linked list with the following features:
- You must be able to **insert** a value of an arbitrary type, and, optionally, specify an index for the insertion
- You must be able to **remove** a value of an arbitrary type from the list
- You must be able to get the current **length** of the list
- You must be able to iterate through the list by passing a function pointer to **for_each** which invoked the pointed function on each element of the list
- You must be able to **get** an element at a specific index
- You must be able to serialize the entire list **to_string** to view its contents in a convenient way

##### Further Requirements
- Every method implemented for the Linked list must have a robust description of its behavior, and its runtime complexity (Big-O).
- Furthermore, the Linked list implementation should be linkable via its own header file for optimal re-use.
- Lastly, each of the methods exposed by Linked list should have an option to log the inner operations of the list.

#### Testing
##### CLI
You must also create a command-line program capable of showcasing all of the linked list features described above. It must have a call-and-response text-based interface that allows the user to interact with an underlying linked list. Consider this example of the interface we have in mind:
```sh
$ ./linked-list-cli
Welcome to the Linked list CLI!
There are several different commands that you may use to interact with the underlying Linked list.
Commands: `insert`, `remove`, `length`, `get`, and `print`
You can type `quit` to exit the CLI.
> insert 1
Inserted 1.
> insert 2
Inserted 2.
> print
[1, 2]
> remove 1
Removed 1.
> length
1
> insert 3
Inserted 3.
> get 1
3
> get 99
ERROR: no element at index `99`
> print
[1, 3]
> quit
Goodbye!
```

##### Unit tests
Write a program that tests every major function of Linked list using the testing library [Check](https://libcheck.github.io/check/web/install.html).
