# Abstract Data Types
Behavior is most important, details of implementation ignored
# Queues
**FIFO** - First In, First Out

## Operations
### Enqueue
Add to end of queue
### Dequeues
Gets first element of the queue
## Queues With Circular Arrays
tail = (head + size - 1) mod length

**When enqueueing:**
tail = (tail + 1) mod length
queue\[tail\] = element
size++

**When dequeueing:**
element = queue\[head\]
head = (head + 1) mod length
size--
return element
### Resizing
Careful when copying, tail = (head + size - 1) mod length must always be true
When coping elements over:
	Copy head at position
	Copy all others sequentially
OR:
	Copy all elements sequentially (head->tail) into the beginning of the list

## Usages
Keyboard buffer
CPU Processes (Unless priorities or threads)
# Stacks
Type of list
No operation to access element $i$ directly
**LIFO** - Last In, First Out
## Operations
### Push
Add element to top of the stack
### Pop
Remove element from top of the stack
### Peek
Gets the top element of the stack, without removing it
## Usages
Call stack
Parsing mathematical equations
## Stack Overflow
If a stack has a finite capacity, and we attempt to push, error is thrown
## Stack Underflow
Popping on an empty stack