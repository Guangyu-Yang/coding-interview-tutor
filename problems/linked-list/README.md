# Linked List

## Pattern Overview
Linked list problems test your ability to manipulate pointers without losing references. The key challenges are handling edge cases (empty list, single node, head/tail modifications) and performing in-place operations. Many problems reduce to a few core techniques: using dummy nodes, fast/slow pointers, and careful pointer reassignment.

## Key Signals (When to Use)
- The problem explicitly involves a linked list data structure
- "Reverse a linked list" or part of one
- "Detect a cycle" or "find where a cycle begins"
- "Find the middle" or "find the kth node from the end"
- Merge, split, or reorder nodes without extra space

## Core Techniques
- **Dummy Head Node**: Create a sentinel node before the real head to simplify edge cases where the head might change
- **Fast and Slow Pointers**: Move one pointer 2 steps and another 1 step to find the middle, detect cycles, or find the cycle start
- **Iterative Reversal**: Use three pointers (prev, curr, next) to reverse links one at a time
- **Merge Two Lists**: Use a dummy node and a tail pointer; compare heads of both lists and append the smaller one
- **Runner Technique**: Advance one pointer k steps ahead, then move both until the leader reaches the end

## Common Complexity
- Time: O(n) typical for single-pass or two-pass algorithms
- Space: O(1) typical for in-place pointer manipulation

## Classic Problems
- Reverse Linked List (Easy)
- Merge Two Sorted Lists (Easy)
- Linked List Cycle (Easy)
- Reorder List (Medium)
- Remove Nth Node From End of List (Medium)
- Copy List with Random Pointer (Medium)
- Merge k Sorted Lists (Hard)
- LRU Cache (Medium) -- combines linked list with hash map

## Tips for Interviews
- Always use a dummy node when the head of the result list might change
- Draw the pointer reassignment step by step before coding -- one wrong order and you lose a reference
- Check your code against edge cases: empty list, single node, two nodes
- When reversing, think about what `prev`, `curr`, and `next` point to at each step
- For problems combining linked lists with other structures (like LRU Cache), a doubly linked list often pairs with a hash map
