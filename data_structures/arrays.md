# Arrays
Arrays are the most basic data structure. For an array, the user must declare its size upfront (though most modern languages handle this behind the scenes) since arrays are stored in adjacent blocks of memory. If you were able to change its size then there would be no guarentee that there would be more memory to use in that block of memory. 
* Arrays hold values referenced by index, so accessing items is very quick. 
* Strings are arrays of characters, tuples are immutable arrays, and Python lists are dynamically resized arrays.
* Each cell in an array uses the same number of bytes, so usually the array will actually just store a pointer to the actual object rather than storing it within the contiguous block of memory.
* ```address = start + (cellsize * index)```


|Operation|Complexity|
|---------|----------|
|Access   |O(1)      |
|Search   |O(n)      |
|Insert   |O(n)      |
|Delete   |O(n)      | 

## Practice Problems

|Problem   |My Solution|
|----------|-----------|
|[Check to see if two strings are anagrams of one another.](https://www.udemy.com/python-for-data-structures-algorithms-and-interviews/learn/v4/overview)| https://github.com/aspittel/coding_problems/blob/master/arrays/anagram_check.py|
|[Check to see if two strings are permutations of each other.](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)|https://github.com/aspittel/coding_problems/blob/master/arrays/check_if_permutation.py|
|[Compress a string](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)| https://github.com/aspittel/coding_problems/blob/master/arrays/compress_string.py|
|[Count the differences between two strings](https://www.hackerrank.com/challenges/ctci-making-anagrams)|https://github.com/aspittel/coding_problems/blob/master/arrays/count_differences.py|
|[Count the positive, negative, and zero values in an array](https://www.hackerrank.com/challenges/plus-minus?h_r=next-challenge&h_v=zen)|https://github.com/aspittel/coding_problems/tree/master/arrays|
|[Count the valleys in a hike](https://www.hackerrank.com/challenges/counting-valleys)|https://github.com/aspittel/coding_problems/blob/master/arrays/count_valleys.py|
|[Draw a pyramid given its height](https://www.hackerrank.com/challenges/staircase?h_r=next-challenge&h_v=zen)|https://github.com/aspittel/coding_problems/blob/master/arrays/create_pyramid.py|
|[What is the number of deletions needed to make two arrays equal?](https://www.hackerrank.com/challenges/equality-in-a-array)|https://github.com/aspittel/coding_problems/blob/master/arrays/equality_in_array.py|
|[Array left rotation](https://www.hackerrank.com/challenges/ctci-array-left-rotation)|https://github.com/aspittel/coding_problems/blob/master/arrays/left_rotation.py|
|[Find the item in an array that doesn't have a match](https://www.hackerrank.com/challenges/ctci-lonely-integer)|https://github.com/aspittel/coding_problems/blob/master/arrays/lonely_integer.py|
|[Find the diagonal difference in a matrix](https://www.hackerrank.com/challenges/diagonal-difference)|https://github.com/aspittel/coding_problems/blob/master/arrays/matrix_diagonal_difference.py|
|[Find the maximum and minimum sums in an array](https://www.hackerrank.com/challenges/mini-max-sum/submissions/code/42826333)|https://github.com/aspittel/coding_problems/blob/master/arrays/max_and_min_sum.py|
|[Check to see if a string can be rearranged as a palindrome](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)|https://github.com/aspittel/coding_problems/blob/master/arrays/palindrome_permutation.py|
|[Check to see if a string can be made from a list of substrings](https://www.hackerrank.com/challenges/password-cracker)|https://github.com/aspittel/coding_problems/blob/master/arrays/password_cracker.py|
|[See if a word is in a list of words](https://www.hackerrank.com/challenges/ctci-ransom-note)|https://github.com/aspittel/coding_problems/blob/master/arrays/ransom_note.py|
|[Check if a string contains only unique characters](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)|https://github.com/aspittel/coding_problems/blob/master/arrays/string_unique_chars.py|
|[Find the max subarray](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)|https://github.com/aspittel/coding_problems/blob/master/arrays/sum_max_subarray.py|
|[URLify a string](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)|https://github.com/aspittel/coding_problems/blob/master/arrays/urlify.py|
|[Zero a matrix](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)|https://github.com/aspittel/coding_problems/blob/master/arrays/zero_matrix.py|
|[Add the even numbers in the Fibonacci sequence](https://projecteuler.net/problem=2)|Not posted, ask if interested!|
|[Find the largest prime factor of a number](https://projecteuler.net/problem=3)|Not posted, ask if interested!|
|[Find the largest palindrome project](https://projecteuler.net/problem=4)|Not posted, ask if interested!|
|[Smallest multiple](https://projecteuler.net/problem=5)|Not posted, ask if interested!|
|[Smallest square difference](https://projecteuler.net/problem=6)|Not posted, ask if interested!|
|[10001st prime product](https://projecteuler.net/problem=8)|Not posted, ask if interested!|
|[Largest product in a grid](https://projecteuler.net/problem=11)|Not posted, ask if interested!|
|[Large sum](https://projecteuler.net/problem=13)|Not posted, ask if interested!|
|[Find longest Collatz sequence](https://projecteuler.net/problem=14)|Not posted, ask if interested!|
|[Number letter counts](https://projecteuler.net/problem=17)|Not posted, ask if interested!|
|[Maximum path sum I](https://projecteuler.net/problem=18)|Not posted, ask if interested!|
|[Non-abundant sums](https://projecteuler.net/problem=23)|Not posted, ask if interested!|
|[Lexicographic permutations](https://projecteuler.net/problem=24)|Not posted, ask if interested!|
|[Quadratic primes](https://projecteuler.net/problem=27)|Not posted, ask if interested!|
|[Number spiral diagonals](https://projecteuler.net/problem=28)|Not posted, ask if interested!|
|[Pandigital products](https://projecteuler.net/problem=32)|Not posted, ask if interested!|
|[Circular primes](https://projecteuler.net/problem=34)|Not posted, ask if interested!|
|[Double base palindromes](https://projecteuler.net/problem=36)|Not posted, ask if interested!|
|[Truncatable primes](https://projecteuler.net/problem=37)|Not posted, ask if interested!|
|[Maximum path sum II](https://projecteuler.net/problem=67)|Not posted, ask if interested!|
