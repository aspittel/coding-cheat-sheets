# Recursion
Recursion is when a function calls itself. This requires at least O(n) memory usage for the stack storing the function calls. 

### Code Example
```python
def factorial(n):
	if n <= 1:
		return 1
	return n * factorial(n - 1)
```

## Memoization
Memoization is often useful in recursion. This is when the results of a function call are remembered so they can be used again in later function calls. This is like cahching your results to use again.

### Code Example
```python
factorial_memo = {}

def factorial(n):
	if n <= 1:
		return 1
	elif n not in factorial_memo:
		factorial_memo[n] = n * factorial(n-1)
	return factorial_memo[n]
```