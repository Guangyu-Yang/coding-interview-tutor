# Trees

## Pattern Overview
Tree problems are among the most frequently tested in interviews because they naturally involve recursion, and solutions require thinking about base cases, recursive structure, and combining subproblem results. Most binary tree problems follow a pattern of processing the current node and recursing on left and right subtrees, either top-down (passing information to children) or bottom-up (collecting information from children).

## Key Signals (When to Use)
- The input is a binary tree or binary search tree (BST)
- "Find the height/depth/diameter" of a tree
- "Validate BST" or "find kth smallest in BST"
- "Lowest common ancestor" or "path between nodes"
- Level-order or zigzag traversal questions
- Serialization/deserialization of tree structures

## Core Techniques
- **DFS (Preorder/Inorder/Postorder)**: Recursive traversal choosing when to process the node relative to its children. Inorder on a BST gives sorted order.
- **BFS (Level-Order Traversal)**: Use a queue to process nodes level by level; useful for level-order output, minimum depth, or rightmost node per level
- **Top-Down Recursion**: Pass accumulated state (like a path sum) from parent to children
- **Bottom-Up Recursion**: Collect results from subtrees and combine at the current node (e.g., height, diameter)
- **BST Properties**: Left < Node < Right. Use this to prune search, validate, or find elements in O(h) time.

## Common Complexity
- Time: O(n) typical -- visit every node once
- Space: O(h) for recursion stack where h is tree height; O(n) worst case for skewed trees; O(n) for BFS queue on a complete tree

## Classic Problems
- Invert Binary Tree (Easy)
- Maximum Depth of Binary Tree (Easy)
- Same Tree (Easy)
- Subtree of Another Tree (Easy)
- Lowest Common Ancestor of a BST (Medium)
- Binary Tree Level Order Traversal (Medium)
- Validate Binary Search Tree (Medium)
- Kth Smallest Element in a BST (Medium)
- Construct Binary Tree from Preorder and Inorder Traversal (Medium)
- Binary Tree Maximum Path Sum (Hard)
- Serialize and Deserialize Binary Tree (Hard)

## Tips for Interviews
- Start by identifying whether the problem is top-down or bottom-up -- this determines your recursive structure
- Always define the base case first (usually `if not node: return ...`)
- For BST problems, leverage the sorted property to avoid visiting all nodes
- If a problem asks for level-by-level results, use BFS with a queue
- When the problem asks about paths, decide if the path must go through the root or can start/end anywhere -- this changes the approach significantly
