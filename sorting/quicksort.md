# Quicksort
Quicksorting is an algorithm in which a random element is selected from the array and then the array is partitioned so that all the numbers less than the element are placed before it and the ones greater than it are placed after it. This algorithm is efficient since swapping two elements in an array is usually a very quick process. If the randomly selected element isn't near the median, quicksorting can be inefficient. 

## Sample Code
```python
def partition(li, start, end):
	pivot = li[start]
	left = start + 1
	right = end
	done = False

	while not done:
		while left <= right and li[left] <= pivot:
			left += 1
		while right >= left and li[right] >= pivot:
			right -= 1
		if right < left: 
			done = True
		else:
			li[left], li[right] = li[right], li[left]
	li[start], li[right] = li[right], li[start]
	return right


def quicksort(li, start=0, end=None):
	if end == None: end = len(li) - 1
	if start < end:
		pivot = partition(li, start, end)
		# Recursively perform same operation on first and last halves of list
		quicksort(li, start, pivot-1)
		quicksort(li, pivot+1, end)
	return li
```	

## Space Complexity: O(log(n))

## Time Complexity
| Best          | Average     | Worst |
| --------------|:-----------:| -----:|
| O(n (log(n))) | O(n log(n)) | O(N^2)|

* [Animated Quick Sort Display](https://www.toptal.com/developers/sorting-algorithms/quick-sort)