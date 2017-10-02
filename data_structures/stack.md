# Stacks

## About
Stacks are data structures (or collections) which order removal and insertion in a last in, first out (or LIFO) way. There are two operations that define a stack - push and pop. Pushing an item means adding it to the top of the stack. Popping an item means removing it from the top of the stack. Therefore, newer items are at the top and will be accessed first, older items are near the bottom and are accessed last.

![](http://legacy.earlham.edu/~ltnguyen14/cs%20web/pics/stack.png) 

Back buttons, undo functionality, and function calls in programming are usually implemented using stacks.

## Complexity

The time complexity of stack operations depends on the implementation of a stack. Some implementations use arrays or array lists, which mean that the operations have similar complexities to those of an array. Others use nodes and pointers or linked lists and therefore would have similar complexities.


## Code Example using Nodes
```python
class Node:
	def __init__(self, data, next):
		self.data = data
		self.next = next

class Stack:
	def __init__(self):
		self.head = None
	
	def push(self, data):
		self.head = Node(data, self.head)

	def pop(self):
		data = self.head.data
		self.head = self.head.next
		return data 
```
In the above example, the big-O complexity looks like:

|Operation|Complexity|
|---------|----------|
|Access   |O(n)      |
|Search   |O(n)      |
|Insert   |O(1)      |
|Delete   |O(1)      | 

In order to access an item or search for one we would have to traverse the linked list. Inserting an item will always happen from the top, so it will always happen in constant time.


## Code Example using an Array
```python 
class Stack:
	
	def __init__(self):
		self.data = []

	def push(self, item):
		self.data.append(item)

	def pop(self):
		return self.data.pop()

	def peek(self):
		return self.data[-1]
```
In the above example, the big-O complexity looks like:

|Operation|Complexity|
|---------|----------|
|Access   |O(1)      |
|Search   |O(n)      |
|Insert   |O(1)      |
|Delete   |O(1)      | 

In order to access an item or search for one we would have to traverse the linked list. Inserting an item will always happen from the top, so it will always happen in constant time. Python [optimizes](https://www.ics.uci.edu/~pattis/ICS-33/lectures/complexitypython.txt) append and pop if they are at the end of a list, so the operations also happen in constant time. Some other implementations of arrays would not have similar optimizations and would then have insertion and deletion at O(n).

## Practice Problems

* [Implement a queue using two stacks](https://www.hackerrank.com/challenges/ctci-queue-using-two-stacks)
* [Check to see if a sequence of parentheses is balanced](https://www.hackerrank.com/challenges/ctci-balanced-brackets)
