# Hash Tables

## About
Hash tables are data structures that map keys to values. Hashing functions compute indexes where desired values can be found. The biggest difficulty with hashing functions are collisions, which happen when the hashing function computes the same index for multiple values. 

Dictionaries in Python are an implementation of a hash table.

```python
dict = {
    'hello': 'world',
    'yes': 'please'
}
```

## Hashing Functions
Hashing functions aim to distribute the key-value pairs across buckets  evenly -- a perfect hashing function would allow for constant time lookups in all cases.

Usually, we can't avoid collisions -- if 2,450 random keys are hashed into a million buckets then there is a [95% chance](https://en.wikipedia.org/wiki/Hash_table) of a collision.

There are many ways of resolving those collisions. The most simple is through using separate chaining. This algorithm uses a linked list to store the key value pairs if they share the same hash value.

Another implementation is to use linear probing. This algorithm finds the next available slot if the one for the given hash function is already taken. 


## Example Code - Separate Chaining
```python
class HashEntry:
    def __init__(self, key, value):
        self.key = key
        self.value = value
        self.next = None
    

class HashTable:
    def __init__(self, size):
        self.size = size
        self.table = [None] * self.size

    def hashing_function(self, key):
        return hash(key) % self.size

    def rehash(self, entry, key, value):
        while entry and entry.key != key:
            prev, entry = entry, entry.next
        if entry:
            entry.value = value
        else:
            prev.next = HashEntry(key, value)

    def set(self, key, value):
        slot = self.hashing_function(key)
        entry = self.table[slot]
        if not entry:
            self.table[slot] = HashEntry(key, value)
        else:
            self.rehash(entry, key, value)
    
    def get(self, key):
        hash = self.hashing_function(key)
        if not self.table[hash]: raise KeyError
        else:
            entry = self.table[hash]
            while entry and entry.key != key: entry = entry.next
            return entry.value
```


## Example Code - Linear Probing
```python
class HashTable:
    def __init__(self, size):
        self.size = size
        self.keys = [None] * self.size
        self.values = [None] * self.size
      
    def hash_function(self, key):
        return hash(key) % self.size
    
    def get_slot(self, key):
        slot = self.hash_function(key)
        while self.keys[slot] and self.keys[slot] != key:
            slot = self.hash_function(slot + 1)
        return slot
    
    def set(self, key, value):
        slot = self.get_slot(key)
        self.keys[slot] = key
        self.values[slot] = value
        
    def get(self, key):
        return self.values[self.get_slot(key)]
``` 

## Complexity
|Operation|Complexity|
|---------|----------|
|Access   |O(1) -> O(n)|
|Search   |O(1) -> O(n)|
|Insert   |O(1) -> O(n)|
|Delete   |O(1) -> O(n)| 

The complexities of each of the above operations depend on the hashing function used. A perfect hashing function where keys and values are all known before runtime would run at O(1) for all of the above functions. Most are closer to O(n) in actual applications (like those above). 
