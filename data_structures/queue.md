# Queue
A queue is a data structure that operates on a first in first out basis, similar to a line for a movie. These are often used for breadth-first searching where nodes are stored in order for processing. These are usually implemented using either a singly linked list or an array. Common methods include:

* Enqueue: add an item to the queue
* Dequeue: remove item from the queue
* Peek: return the next item in the queue

## Code Example
```python 
class Queue:

	def __init__(self):
		self.data = []

	def enqueue(self, item):
		self.data.insert(0, item)

	def dequeue(self):
		return self.data.pop()

	def peek(self):
		return self.data[-1]
```
## Practice Problems
|Problem   |My Solution|
|----------|-----------|
|[Implement a queue using two stacks](https://www.hackerrank.com/challenges/ctci-queue-using-two-stacks)|https://github.com/aspittel/coding_problems/blob/master/stacks_and_queues/queue_from_two_stacks.py|
