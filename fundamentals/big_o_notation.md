# Big-O Notation
Big-O Notation is used to describe how well an algorithm scales. There are two types of complexity that are normally measured with Big-O: time complexity and space complexity. Time complexity refers to the number of operations that execute depending on the number or size of the inputs. Space complexity refers to how much memory the algorithm will use when executing. O(1) complexity is really good, O(N) complexity is usually pretty good as well, O(N^2) and up complexity is typically avoided when possible.

## Scalability
The following table shows how algorithms with different complexities scale when given different numbers of inputs. Note: some values are rounded.

|Complexity |1|10      |100  |
|-----------|-|--------|-----|
|O(1)       |1| 1      |1    |
|O(log N)   |0| 2      |5    |
|O(N)       |1|10      |100                            |
|O(N log N) |0|20      |461                            |
|O(N^2)     |1|100     |10000                          | 
|O(2^N)     |1|1024    |1267650600228229401496703205376|       
|O(N!)      |1|3628800 |93326215443944152681699238856266700490715968264381621468592963895217599993229915608941463976156518286253697920827223758251185210916864000000000000000000000000 |


## O(1) Complexity (Constant)
O(1) means that an algorithm is static or constant. The complexity stays the same no matter the inputs.

### Example
```python
def return_first(li):
	return li[0]


def hello_world():
	print('Hello, world!')
```

## O(N) Complexity (Linear)
O(N) is when the code goes through each input once. If the inputs increase, the processing time or memory use increases linearly.

### Example
```python
def print_each(li):
	for item in li:
		print(item)
```

## O(N^2) Complexity (Quadratic)
O(N^2) complexity is when the code doubly iterates over an input, so each n is iterated over n times.

### Example
```python
def print_each_n_times(li):
	for n in li:
		for m in li:
			print(n, m)
```

## O(log n) and O(n log(n)) complexity
These are mostly found in sorting algorithms where processing time increases based on input size. A good example of this is a binary search through a pre-sorted list. [Here](http://stackoverflow.com/questions/2307283/what-does-olog-n-mean-exactly) is a great explanation of these complexities.

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

## Other helpful links
* [Stack Overflow: What is a plain English explanation of “Big O” notation?](http://stackoverflow.com/questions/487258/what-is-a-plain-english-explanation-of-big-o-notation?page=1&tab=votes#tab-top)

* [Big O Cheat Sheet](http://bigocheatsheet.com/)