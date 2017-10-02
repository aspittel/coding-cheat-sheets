# Arrays

## About
Arrays are the most basic data structure. For an array, the user must declare its size upfront (though most modern languages handle this behind the scenes) since arrays are stored in adjacent blocks of memory. If you were able to change its size then there would be no guarantee that there would be more memory to use in that block of memory. 


* Arrays hold values referenced by index, so accessing items is very quick. 
* Strings are arrays of characters, tuples are immutable arrays, and Python lists are dynamically resized arrays.
* Each cell in an array uses the same number of bytes, so usually the array will actually just store a pointer to the actual object rather than storing it within the contiguous block of memory.
* ```address = start + (cellsize * index)```

## Complexity

|Operation|Complexity|
|---------|----------|
|Access   |O(1)      |
|Search   |O(n)      |
|Insert   |O(n)      |
|Delete   |O(n)      | 

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
