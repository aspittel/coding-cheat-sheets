#Big-O Notation
Big-O Notation refers to either the time or memory complexity of a problem or the solution to it. O stands for order.

## O(1) Complexity
O(1) means that an algorithm is static or constant. The complexity stays the same no matter the inputs.

### Example
```python
def return_first(li):
	return li[0]


def hello_world():
	print('Hello, world!')
```

## O(N) Complexity
O(N) is when the code goes through each input once. If the inputs increase, the processing time or memory use increases linearly.

### Example
```python
def print_each(li):
	for item in li:
		print(item)
```

## O(N^2) Complexity
O(N^2) complexity is when the code doubly iterates over an input, so each n is iterated over n times.

### Example
```python
def print_each_n_times(li):
	for n in li:
		for m in li:
			print(n, m)
```

## O(log n) and O(n log(n)) complexity
These are mostly found in sorting algorithms where processing time increases based on input size. A good example of this is a binary search through a pre-sorted list.

### Example
```python
def binary_search(li, item, first=0, last=None):
	if not last:
		last = len(li)

	midpoint = (last - first) / 2 + first

	if li[midpoint] == item:
		return midpoint

	elif li[midpoint] > item:
		return binary_search(li, item, first, midpoint)

	else:
		return binary_search(li, item, midpoint, last)
```