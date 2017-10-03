# Graphs

##about

Graphs are non-linear data structures that can show any type of relationship. Many data structures fall under the parent category of graphs -- like linked lists and trees. Graphs have nodes (also called vertices) and edges. The node holds the data and then the edges point to related nodes. There are two types of edges: directed and undirected. Directed edges point in a direction whereas undirected edges point both ways. 

Good examples of graphs in use are Facebook friends, Twitter following (which would be directed), or a map of Metro stops.

There are many ways to store a graph data structure. You can use pointers and nodes, or you could use an adjacency list or matrix.


## Example Graph
```
     A –→ B ←–––– C → D ↔ E
     ↑    ↕     ↙ ↑     ↘
     F –→ G → H ← I ––––→ J
           ↓     ↘ ↑
           K       L
```
Image from [itsy-bitsy-data-structures](https://github.com/thejameskyle/itsy-bitsy-data-structures/blob/master/itsy-bitsy-data-structures.js).

## Glossary

* **Edges** - connections between nodes.
* **Directed** - edges point in a direction.
* **Undirected** - edges point in both directions.
* **Euler Path** - path that visits each edge just once. A graph must have either zero or two vertices with an odd degree to have an euler path. 
* **cycle** - circle made of edges.

## Sample Code
```python
class Node:
      def __init__(self, data):
            self.data = data
            self.edges = []
```