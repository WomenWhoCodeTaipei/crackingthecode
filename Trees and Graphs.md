# Trees and Graphs
Angel Chien

---

## What is Tree
1.with a root value and subtrees of children with a parent node, represented as a set of linked nodes.
2.defined recursively (locally) as a collection of nodes (starting at a root node), where each node is a data structure consisting of a value, together with a list of references to nodes (the "children"), with the constraints that no reference is duplicated, and none points to the root.


---

Alternatively, a tree can be defined abstractly as a whole (globally) as an ordered tree, with a value assigned to each node.


---

![](https://i.imgur.com/HkU1ilP.png)


---

![](https://i.imgur.com/EbCH9bk.png)
<!-- .slide: data-background="#FFF000" -->


---

Root
The top node in a tree.
Child
A node directly connected to another node when moving away from the Root.
Parent
The converse notion of a child.
Siblings
A group of nodes with the same parent.


---

Descendant
A node reachable by repeated proceeding from parent to child.
Ancestor
A node reachable by repeated proceeding from child to parent.
Leaf (less commonly called External node)
A node with no children.


---

Branch
Internal node
A node with at least one child.
Degree
The number of subtrees of a node.
Edge
The connection between one node and another.
Path
A sequence of nodes and edges connecting a node with a descendant.


---

Level
The level of a node is defined by 1 + (the number of connections between the node and the root).
Height of node
The height of a node is the number of edges on the longest path between that node and a leaf.
Height of tree
The height of a tree is the height of its root node.
Depth
The depth of a node is the number of edges from the tree's root node to the node.

---

# Binary Tree
its left descendents are less than or equal to the current node, which is less than the right descendents. 
O(log n)
Same level
Back to book P.114
