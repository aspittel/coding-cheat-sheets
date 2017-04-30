# Stack
A stack is a data structure that operates in a last in first out nature. Newer items are at the top of the stack and will be accessed first whereas older items are near the bottom and will be accessed last. A back button is a good example of an implementation of a stack. Common methods include:
* Push - add an item to the top of the stack.
* Pop - remove the top item from the stack.
* Peek - check to see the top item of the stack.

## Code Example
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
## Practice Problems
|Problem   |My Solution|
|----------|-----------|
|[Implement a queue using two stacks](https://www.hackerrank.com/challenges/ctci-queue-using-two-stacks)|https://github.com/aspittel/coding_problems/blob/master/stacks_and_queues/queue_from_two_stacks.py|
|[Check to see if a sequence of parentheses is balanced](https://www.hackerrank.com/challenges/ctci-balanced-brackets)|https://github.com/aspittel/coding_problems/blob/master/stacks_and_queues/balanced_parentheses.py|
