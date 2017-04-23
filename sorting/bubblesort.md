# Bubble Sort

Bubble sorting is oen of the simplest sorting algorithms. In order to implement this sort, the script starts on the left of the array and switches elements that are next to each other if they are in the wrong order. This usually requires multiple passes, unless the array is already sorted. 

## Sample Code
```python
def bubble_sort(li):
	keep_going = False
	for index, (item, next_item) in enumerate(zip(li, li[1:])):
		if item > next_item:
			li[index], li[index+1] = next_item, item
			keep_going = True
	if keep_going:
		return bubble_sort(li)
	else:
		return li
```

## Space Complexity: O(1)

## Time Complexity
| Best | Average| Worst |
| -----|:------:| -----:|
| O(N) | O(N^2) | O(N^2)|
