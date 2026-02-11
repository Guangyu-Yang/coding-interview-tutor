# Backtracking

## Pattern Overview
Backtracking systematically explores all possible solutions by building candidates incrementally and abandoning ("backtracking" from) a candidate as soon as it cannot lead to a valid solution. It is essentially DFS on the decision tree with pruning. Use it when the problem asks you to generate all valid configurations, permutations, combinations, or subsets.

## Key Signals (When to Use)
- "Generate all permutations/combinations/subsets"
- "Find all valid configurations" (e.g., N-Queens, Sudoku)
- "Partition a string into valid parts" (e.g., palindrome partitioning)
- The problem asks for all solutions, not just one or the count
- Constraint satisfaction where choices must be explored and undone

## Core Techniques
- **Choose-Explore-Unchoose**: Make a choice, recurse to explore further, then undo the choice to try alternatives
- **Pruning**: Skip branches early when they cannot lead to a valid solution (e.g., remaining sum too small, duplicate element)
- **Subset/Combination Template**: Use a start index to avoid revisiting earlier elements; include or skip each element
- **Permutation Template**: Use a visited set or swap elements to generate all orderings
- **Constraint Checking**: Validate constraints at each step rather than only at the end to prune aggressively

## Common Complexity
- Time: O(2^n) for subsets, O(n!) for permutations, problem-specific with pruning
- Space: O(n) for the recursion stack and current path

## Classic Problems
- Subsets (Medium)
- Subsets II (Medium)
- Combination Sum (Medium)
- Combination Sum II (Medium)
- Permutations (Medium)
- Word Search (Medium)
- Palindrome Partitioning (Medium)
- Letter Combinations of a Phone Number (Medium)
- N-Queens (Hard)

## Tips for Interviews
- Draw the decision tree for a small example first to understand the branching structure
- To handle duplicates, sort the input first and skip consecutive equal elements at the same decision level
- Always think about what pruning you can add -- it dramatically affects practical runtime
- The backtracking template is almost always the same; practice it until you can write it from muscle memory
- Clearly define: (1) what a "choice" is, (2) what the base case is, (3) how to undo a choice
