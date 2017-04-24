# Arrays
Arrays are the most basic data structure. For an array, the user must declare its size upfront (though most modern languages handle this) since arrays are stored in adjacent blocks of memory. If you were able to change its size then there would be no guarentee that there would be more memory to use in that block of memory. 
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

