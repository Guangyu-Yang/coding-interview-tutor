# Graphs

## Pattern Overview
Graph problems involve navigating relationships between entities represented as nodes and edges. The two fundamental traversal strategies are BFS (for shortest path in unweighted graphs and level-order processing) and DFS (for exploring all reachable nodes, detecting cycles, and topological ordering). Recognizing the graph structure hidden in a problem is often the hardest part.

## Key Signals (When to Use)
- The problem explicitly gives an adjacency list, matrix, or edge list
- "Find if a path exists" or "shortest path" between nodes
- "Number of connected components" or "number of islands"
- Dependency ordering or scheduling (topological sort)
- Problems on grids where cells are nodes and neighbors are edges
- "Detect a cycle" in directed or undirected graphs

## Core Techniques
- **BFS (Breadth-First Search)**: Use a queue; explores nodes level by level. Optimal for shortest path in unweighted graphs.
- **DFS (Depth-First Search)**: Use recursion or a stack; explores as deep as possible before backtracking. Good for connectivity, cycle detection, and topological sort.
- **Topological Sort (Kahn's / DFS)**: Order nodes so every directed edge u->v has u before v. Use BFS with in-degree counting (Kahn's) or DFS with post-order recording.
- **Union-Find (Disjoint Set Union)**: Efficiently track connected components with near O(1) union and find operations using path compression and union by rank.
- **Dijkstra / Bellman-Ford**: Shortest path in weighted graphs. Dijkstra uses a min-heap (non-negative weights); Bellman-Ford handles negative weights.

## Common Complexity
- Time: O(V + E) for BFS/DFS; O(E log V) for Dijkstra; O(V * E) for Bellman-Ford
- Space: O(V + E) for adjacency list; O(V) for visited set and queue/stack

## Classic Problems
- Number of Islands (Medium)
- Clone Graph (Medium)
- Pacific Atlantic Water Flow (Medium)
- Course Schedule (Medium)
- Course Schedule II (Medium)
- Graph Valid Tree (Medium)
- Number of Connected Components in an Undirected Graph (Medium)
- Redundant Connection (Medium)
- Word Ladder (Hard)
- Alien Dictionary (Hard)
- Network Delay Time (Medium)

## Tips for Interviews
- Always build the adjacency list first if given edges -- it makes traversal cleaner
- For grid problems, treat each cell as a node with up to 4 neighbors; use a visited set or modify the grid in place
- For cycle detection in directed graphs, track three states: unvisited, in-progress, and completed
- Topological sort is the key to any problem involving prerequisite or dependency ordering
- When the problem says "minimum number of steps," think BFS first
- Union-Find is often simpler than DFS for pure connectivity queries
