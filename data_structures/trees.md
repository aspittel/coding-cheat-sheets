# Trees

## About
Trees are graph data structures that are hierarchical and unidirectional. They have a root value, and then sub-trees of children that each have parents. They are represented as a series of linked nodes. Each node has a value and then pointers to its children.

Trees have nodes and vertices without any cycles. They are also directed - the parents point down to the children rather than having bidirectional relationships. 

The most common tree is a binary tree - where where every node has at most two children.

## Sample Code

```python
class BinaryTree:

    def __init__(self, data, left, right):
        self.data = data
        self.left = left
        self.right = right
```


## Glossary
* **Root** - the top node of the tree.
* **Child** - a node below the parent.
* **Parent** - a node above a child. Note - a node can be both a parent and a child!
* **Siblings** - nodes with the same parent.
* **Leaf** - a node with no children.
* **Branch** - a node with a child.
* **Edge** - Connection between nodes.


## Tree Visual
```
          A                     
        ↙   ↘              
      B       C                
    ↙  ↘
   D    E
```