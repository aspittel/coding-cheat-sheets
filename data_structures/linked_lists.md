# Linked Lists

## About
Linked lists are linear collections of data that consist of nodes with data and pointers. Singly linked lists have nodes that store the value of the node and a pointer to the next node. Doubly linked lists additionally store a pointer to the previous node.

Linked lists do not need to be stored contiguously in memory like an array, so insertion and deletion is relatively simple. They do not natively support accessing one data node or indexing through operations. These operations are normally performed just by looping through the nodes. They also use more memory than arrays since they also store pointers to the next link(s).

They are commonly used to implement stacks, queues, and associative arrays.

Linked lists can be categorized as directed graph data structures since each node points to others. Singly linked lists are acyclical, doubly linked lists are cyclical.

A less common form of linked lists is a circular linked list where the tail points back to the head rather than being a null pointer.

Some linked lists use sentinel nodes, which are "dummy" nodes that ensure the first and or last nodes still point to another. These simplify some algorithms.

### Singly linked list
!()[https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Singly-linked-list.svg/408px-Singly-linked-list.svg.png]

### Doubly linked list
!()[https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Doubly-linked-list.svg/610px-Doubly-linked-list.svg.png]

## Complexity

|Operation|Complexity|
|---------|----------|
|Access   |O(n)      |
|Search   |O(n)      |
|Insert   |O(1)      |
|Delete   |O(1)      | 

In order to access an item or search the list, you must traverse the whole thing. In order to insert or delete nodes, you only need to move the position of pointers.

## Singly Linked List
```python
class Node:

    def __init__(self, data, next):
        self.data = data
        self.next = next


class SinglyLinkedList:

    def __init__(self):
        self.head = None
        self.length = 0
    
    def insert(self, data):
        self.head = Node(data, self.head)
        self.length += 1
    
    def search(self, data):
        idx = 0
        node = self.head
        while node:
            if node.data == data: return idx
            node = node.next
            idx += 1
        return -1
```

## Doubly Linked List
```python
class Node:

    def __init__(self, data, next=None, prev=None):
        self.data = data
        self.next = next
        self.prev = prev


class DoublyLinkedList:
    
    def __init__(self):
        self.head = None
        self.tail = None
        self.length = 0

    def insert(self, data):
        new_node = Node(data, None, self.head)
        if not self.head:
            self.head = new_node
        else:
            self.tail.next = new_node
            new_node.prev = self.tail
        self.tail = new_node
        self.length += 1
```

## Practice Problems
* [Check to see if a linked list has a cycle](https://www.hackerrank.com/challenges/ctci-linked-list-cycle)
* [Find the Nth to last node in a linked list](https://www.udemy.com/python-for-data-structures-algorithms-and-interviews/learn/v4/overview)
