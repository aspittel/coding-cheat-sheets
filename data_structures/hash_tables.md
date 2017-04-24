# Hash Tables
Hash tables are often very efficient data structures. They store data using a computed index. The function that computes the index is called a hashing function. Each item in the hash table has a key and value. The biggest difficulty with hashing is collisions, which happen when the hashing function computes the same index for multiple values. There are many ways around this, including creating a new key or using arrays to store the values at that index.

* Dictionaries in Python are an implementation of a hash table.

|Operation|Complexity|
|---------|----------|
|Access   |N/A       |
|Search   |O(1)->O(n)|
|Insert   |O(1)->O(n)|
|Delete   |O(1)->O(n)| 

The complexities of each of the above operations depend on the hashing function used.
