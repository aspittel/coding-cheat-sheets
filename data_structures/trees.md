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

## Common Operations
* **Searching** - Searching a binary search tree for a specific key can be programmed recursively or iteratively.

## Recursive Search

```
def search_recursively(key, node):
    if node is None or node.key == key:
        return node
    if key < node.key:
        return search_recursively(key, node.left)
    # key > node.key
    return search_recursively(key, node.right)
```

## Iteratively
```
def search_iteratively(key, node): 
    current_node = node
    while current_node is not None:
        if key == current_node.key:
            return current_node
        if key < current_node.key:
            current_node = current_node.left
        else: # key > current_node.key:
            current_node = current_node.right
    return current_node
```

* **Insertion** - Insertion begins as a search would begin; if the key is not equal to that of the root, we search the left or right subtrees as before. Eventually, we will reach an external node and add the new key-value pair (here encoded as a record 'newNode') as its right or left child, depending on the node's key. In other words, we examine the root and recursively insert the new node to the left subtree if its key is less than that of the root, or the right subtree if its key is greater than or equal to the root.

```
def binary_tree_insert(node, key, value):
   if node is None:
       return NodeTree(None, key, value, None)
   if key == node.key:
       return NodeTree(node.left, key, value, node.right)
   if key < node.key:
       return NodeTree(binary_tree_insert(node.left, key, value), node.key, node.value, node.right)
   return NodeTree(node.left, node.key, node.value, binary_tree_insert(node.right, key, value))
```

* **Deletion** - When removing a node from a binary search tree it is mandatory to maintain the in-order sequence of the nodes.

```
def find_min(self):   # Gets minimum node in a subtree
    current_node = self
    while current_node.left_child:
        current_node = current_node.left_child
    return current_node

def replace_node_in_parent(self, new_value=None):
    if self.parent:
        if self == self.parent.left_child:
            self.parent.left_child = new_value
        else:
            self.parent.right_child = new_value
    if new_value:
        new_value.parent = self.parent

def binary_tree_delete(self, key):
    if key < self.key:
        self.left_child.binary_tree_delete(key)
        return
    if key > self.key:
        self.right_child.binary_tree_delete(key)
        return
    # delete the key here
    if self.left_child and self.right_child: # if both children are present
        successor = self.right_child.find_min()
        self.key = successor.key
        successor.binary_tree_delete(successor.key)
    elif self.left_child:   # if the node has only a *left* child
        self.replace_node_in_parent(self.left_child)
    elif self.right_child:  # if the node has only a *right* child
        self.replace_node_in_parent(self.right_child)
    else:
        self.replace_node_in_parent(None) # this node has no children
```

* **Traversal** - Once the binary search tree has been created, its elements can be retrieved in-order by recursively traversing the left subtree of the root node, accessing the node itself, then recursively traversing the right subtree of the node, continuing this pattern with each node in the tree as it's recursively accessed. As with all binary trees, one may conduct a pre-order traversal or a post-order traversal, but neither are likely to be useful for binary search trees. An in-order traversal of a binary search tree will always result in a sorted list of node items (numbers, strings or other comparable items).

The code for in-order traversal in Python is given below. It will call callback (some function the programmer wishes to call on the node's value, such as printing to the screen) for every node in the tree.

```
def traverse_binary_tree(node, callback):
    if node is None:
        return
    traverse_binary_tree(node.leftChild, callback)
    callback(node.value)
    traverse_binary_tree(node.rightChild, callback)
```
