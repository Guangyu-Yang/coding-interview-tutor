# Binary Search

## Pattern Overview
Binary search eliminates half the search space in each step, achieving O(log n) time on sorted or monotonic data. Beyond simple "find a target," it generalizes to any problem where you can define a condition that partitions the search space into two halves -- one where the answer cannot exist and one where it might.

## Key Signals (When to Use)
- The input is sorted, or the problem has a monotonic property
- "Find the position of a target" or "find the first/last occurrence"
- "Minimize the maximum" or "maximize the minimum" (binary search on the answer)
- You need O(log n) time and the search space can be halved with a yes/no condition
- Searching in a rotated sorted array or a matrix with sorted rows/columns

## Core Techniques
- **Standard Binary Search**: Find exact target in a sorted array with `lo, hi, mid` pointers
- **Left-Bound / Right-Bound Search**: Find the first or last position where a condition holds; use `lo < hi` with careful boundary updates
- **Binary Search on Answer**: When the answer is a number in a range and you can check feasibility in O(n), binary search over possible answers
- **Search in Rotated Array**: Determine which half is sorted, then decide which half to search

## Common Complexity
- Time: O(log n) for the search; O(n log n) if combined with an O(n) feasibility check
- Space: O(1) typical for iterative; O(log n) for recursive

## Classic Problems
- Binary Search (Easy)
- Search a 2D Matrix (Medium)
- Koko Eating Bananas (Medium)
- Find Minimum in Rotated Sorted Array (Medium)
- Search in Rotated Sorted Array (Medium)
- Time Based Key-Value Store (Medium)
- Median of Two Sorted Arrays (Hard)

## Tips for Interviews
- Decide your loop invariant before coding: what is always true about `lo` and `hi`?
- Be explicit about whether you use `lo <= hi` or `lo < hi` -- each has different update rules
- Off-by-one errors are the most common bug; test with arrays of size 0, 1, and 2
- For "binary search on the answer" problems, clearly define your `check(mid)` function first
- When in doubt, prefer the `lo < hi` template with `mid = lo + (hi - lo) // 2` to avoid infinite loops
