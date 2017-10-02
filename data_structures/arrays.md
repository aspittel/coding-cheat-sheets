# Arrays

## About
Arrays are collections of elements that can be identified by an index. They are used to implement a ton of other data structures -- like queues, stacks, lists, and sometimes strings.

```python
x = [1, 2, 3]
```

In most languages, indexing starts at 0. The first item in an array can be found at the index 0. Arrays can also have multiple dimensions so matrix operations commonly use them in computer science.

Arrays are stored in memory contiguously, or in one chunk of space, so the memory address of each element in the array can be computed using this formula `address = start + (cellsize * index)`. So an array with three 32-bit integer variables could be stored at addresses 2000, 2004, 2008 so then the address of an item would be 2000 + 4 * index.

Arrays have a fixed size when they are created, so insertion and deletion is not natively supported. Arrays traditionally are stored in contiguous blocks of memory which makes them very efficient to index. If you were able to change the size of an array during runtime, there would be no guarantee that there would be more memory in its reserved block to use.

Many high level languages take care of resizing behind the scenes by using dynamic arrays, so the user doesn't need to initialize the array with a certain size. For example, in Python, lists are initialized automatically with overfill (or additional unused slots). They resize at 4, 8, 16, 25 etc. items ([source](https://www.laurentluce.com/posts/python-list-implementation/)). From a computational perspective, this makes them less efficient but a lot more programmer friendly!


## Complexity

|Operation|Complexity|
|---------|----------|
|Access   |O(1)      |
|Search   |O(n)      |
|Insert   |O(n)      |
|Delete   |O(n)      | 

### Explanation
* Accessing can be done using the formula `start + (cellsize * index)`
* Searching is done by iterating through the array and seeing if the value equals the item you are searching for.
* Insertion is done by recreating the array, which means that each item must be recreated.
* Deletion is done by recreating the array, which means that each item must be recreated.


## Practice Problems
* [Check to see if two strings are anagrams of one another.](https://www.udemy.com/python-for-data-structures-algorithms-and-interviews/learn/v4/overview)
* [Check to see if two strings are permutations of each other.](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)
* [Compress a string](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)
* [Count the differences between two strings](https://www.hackerrank.com/challenges/ctci-making-anagrams)
* [Count the positive, negative, and zero values in an array](https://www.hackerrank.com/challenges/plus-minus?h_r=next-challenge&h_v=zen)
* [Count the valleys in a hike](https://www.hackerrank.com/challenges/counting-valleys)
* [Draw a pyramid given its height](https://www.hackerrank.com/challenges/staircase?h_r=next-challenge&h_v=zen)
* [What is the number of deletions needed to make two arrays equal?](https://www.hackerrank.com/challenges/equality-in-a-array)
* [Array left rotation](https://www.hackerrank.com/challenges/ctci-array-left-rotation)
* [Find the item in an array that doesn't have a match](https://www.hackerrank.com/challenges/ctci-lonely-integer)
* [Find the diagonal difference in a matrix](https://www.hackerrank.com/challenges/diagonal-difference)
* [Find the maximum and minimum sums in an array](https://www.hackerrank.com/challenges/mini-max-sum/submissions/code/42826333)
* [Check to see if a string can be rearranged as a palindrome](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)
* [Check to see if a string can be made from a list of substrings](https://www.hackerrank.com/challenges/password-cracker)
* [See if a word is in a list of words](https://www.hackerrank.com/challenges/ctci-ransom-note)
* [Check if a string contains only unique characters](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)
* [Find the max subarray](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)
* [URLify a string](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)
* [Zero a matrix](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)
* [Add the even numbers in the Fibonacci sequence](https://projecteuler.net/problem=2)
* [Find the largest prime factor of a number](https://projecteuler.net/problem=3)
* [Find the largest palindrome project](https://projecteuler.net/problem=4)
* [Smallest multiple](https://projecteuler.net/problem=5)
* [Smallest square difference](https://projecteuler.net/problem=6)
* [10001st prime product](https://projecteuler.net/problem=8)
* [Largest product in a grid](https://projecteuler.net/problem=11)
* [Large sum](https://projecteuler.net/problem=13)
* [Find longest Collatz sequence](https://projecteuler.net/problem=14)
* [Number letter counts](https://projecteuler.net/problem=17)
* [Maximum path sum I](https://projecteuler.net/problem=18)
* [Non-abundant sums](https://projecteuler.net/problem=23)
* [Lexicographic permutations](https://projecteuler.net/problem=24)
* [Quadratic primes](https://projecteuler.net/problem=27)
* [Number spiral diagonals](https://projecteuler.net/problem=28)
* [Pandigital products](https://projecteuler.net/problem=32)
* [Circular primes](https://projecteuler.net/problem=34)
* [Double base palindromes](https://projecteuler.net/problem=36)
* [Truncatable primes](https://projecteuler.net/problem=37)
* [Maximum path sum II](https://projecteuler.net/problem=67)
