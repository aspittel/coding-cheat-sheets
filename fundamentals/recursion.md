# Recursion
Recursion is when a function calls itself. This requires at least O(n) memory usage for the stack storing the function calls. [Here](https://www.youtube.com/watch?v=k0bb7UYy0pY) is a great explanation of stack usage in recursive functions.

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
## Tail Recursion
Tail recursion is where calculations are performed first and then the recursive call is executed. Some programming languages, usually functional ones, optimize tail calls so they take up less room on the call stack. 

```python
def factorial(n, running_total=1):
	if x <= 1:
		return running_total
	return factorial(x-1, x * running_total)
```

## Practice Problems
|Problem   |My Solution|
|----------|-----------|
|[See how many ways given coins can add up to a sum*](https://www.hackerrank.com/challenges/ctci-coin-change)|https://github.com/aspittel/coding_problems/blob/master/recursion/coin_change.py|
|[See how many ways someone can walk up stairs](https://www.hackerrank.com/challenges/ctci-recursive-staircase)|https://github.com/aspittel/coding_problems/blob/master/recursion/davis_staircase.py|
|Calculate a factorial|https://github.com/aspittel/coding_problems/blob/master/recursion/factorial.py|
|[Generate the nth number in the fibonacci sequence](https://www.hackerrank.com/challenges/ctci-fibonacci-numbers)|https://github.com/aspittel/coding_problems/blob/master/recursion/fibonacci_numbers.py|
|[Find the number of ways numbers to the nth power can add up to a given number](https://www.hackerrank.com/challenges/the-power-sum)|https://github.com/aspittel/coding_problems/blob/master/recursion/possible_powers.py|
|[Add the digits of a number until there is only one digit left](https://www.hackerrank.com/challenges/recursive-digit-sum/)|https://github.com/aspittel/coding_problems/blob/master/recursion/super_sum_digits.py|
|[Calculate how fast an advertisement goes viral](https://www.hackerrank.com/challenges/strange-advertising)|https://github.com/aspittel/coding_problems/blob/master/recursion/viral_advertising.py|

*My solution was not recursive, but this is a typical recursion problem