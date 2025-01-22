---
{"dg-publish":true,"permalink":"/dstest/binary-tree-new/","created":"2024-11-15T08:58:01.490+05:30","updated":"2025-01-22T23:46:21.625+05:30"}
---



### What is full binary tree
> Here every node has either 
	> 0 children or 2 children

### What is Complete Binary tree
> All levels except possible the last level are completely filled 

### What is Application of BST
> file system organization
> Priority queues
> Maintaining sorted data


## What is height of binary tree?


> [!NOTE] Title
> - Height of empty tree = -1
> - Height of tree with single node = 0


> [!tips] Title
> Maximum nodes possible with height h
> 2^(h+1)-1
> minimum nodes possible = h+1
> Level i has maximum of 2^i nodes
> Given n nodes
> minimum height = floor(log2(n))
> maximum height = n-1


## What is time complexity of various operation in tree


1) Binary tree

> Every operation in tree cost O(n)
> average height : O(log n)

2) Binary search tree

> Every operation in bst except find height average case is O(log n) and worst case  O(n)(skewed)
> finding height is average case is O(n)


3) Avl tree
>  Here average and worst case is O(log n)
> Balancing and rotation in bst is O(1)


> [!NOTE] Title
> Space complexity of all tree is O(n)


### Common tree traversal

1. Depth first serach
> Inorder(left-root-Right)
> Preorder(root-left-Right)
> Postorder(left-Right-root)

2. breadth first serach(bfs)
- Level Order Traversal


> [!NOTE] Title
> Traversal always requires visiting all nodes, hence O(n) 




### What is depth of binary tree

> log2n+1


## Internal node

> 2 children





