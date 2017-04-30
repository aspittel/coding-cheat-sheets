# Linked Lists
Linked lists are graph data structures that consist of nodes and pointers. There can be doubly or singly linked lists. Singly linked lists have nodes that store the value of the node and a pointer to the next node. Doubly linked lists additionally store a pointer to the previous node as well.

* The first item is called the head and the rest of the list is called the tail.
* Insertion and deletion is relatively simple since the nodes do not need to be stored adjacently in memory.
* Indexing and accessing elements is pretty slow since you must traverse the list to do so.

|Operation|Complexity|
|---------|----------|
|Access   |O(n)      |
|Search   |O(n)      |
|Insert   |O(1)      |
|Delete   |O(1)      | 

|Problem   |My Solution|
|----------|-----------|
|[Check to see if a linked list has a cycle](https://www.hackerrank.com/challenges/ctci-linked-list-cycle)|https://github.com/aspittel/coding_problems/blob/master/linked_lists/has_cycle.py|
|[Find the Nth to last node in a linked list](https://www.udemy.com/python-for-data-structures-algorithms-and-interviews/learn/v4/overview)|https://github.com/aspittel/coding_problems/blob/master/linked_lists/nth_to_last_node.py|
