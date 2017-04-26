# Divide and Conquer

Divide and conquer is "an algorithm design paradigm that is based on multi-branch recursion. It takes a larger problem and breaks it into 2+ sub-problems" ([Wikipedia](https://en.wikipedia.org/wiki/Divide_and_conquer_algorithm)). [Merge soring](https://github.com/aspittel/coding_cheat_sheets/blob/master/sorting/mergesort.md) and some fibonacci algorithms are implementations of the divide and conquer algorithm. These are especially useful on multi-rocessor systems.

```
		Problem (divide)
	   /				\
	  /					 \
subproblem			 subproblem 
	  \					 /
	   \			    /
	   	    Solution!	

```

## Code Example
```python
def multiply_range(n, m):
	if n == m:
		return m
	if m < n:
		return 1
	else:
		return multiply_range(n, (m+n)/2) * multiply_range((n+m)/2 + 1, m)
```