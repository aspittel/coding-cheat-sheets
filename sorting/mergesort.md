# Merge Sort

Merge sorting is usually more efficient than bubble sorting unless the array is pre-sorted. It always has O(n log(n)) complexity. The algorithm involves using divide and conquer recursion to a split an array until it consists of many arrays with lengths of one. It then merges those sub-arrays back together incrementally, moving the smallest number to the far left and the largest to the far left.

## [Sample Code](https://github.com/aspittel/coding_problems/blob/master/sorting/merge_sort.py)
```python

def merge_sort(li):
	# recursively split the lists
	if len(li) <= 1: return li
	middle = round(len(li) / 2)
	left = li[:middle]
	right = li[middle:]
	return merge(merge_sort(left), merge_sort(right))


def merge(left, right):
	# Merge the two lists back together
	result = []
	while left or right:
		if left and right:
			if left[0] < right[0]:
				result.append(left.pop(0))
			else:
				result.append(right.pop(0))
		elif left:
			result.append(left.pop(0))
		else:
			result.append(right.pop(0))
	return result
```

## Space Complexity: O(n)

## Time Complexity: O(n log(n))

## Additional Links
* [Animated Merge Sort Display](https://www.toptal.com/developers/sorting-algorithms/merge-sort)
