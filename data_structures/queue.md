# Queue
A queue is a data structure that operates on a first in first out basis, similar to a line for a movie. These are often used for breadth-first searching where nodes are stored in order for processing. Common methods include:

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
