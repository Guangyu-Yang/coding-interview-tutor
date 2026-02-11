# Two Pointers

## Pattern Overview
The two-pointer technique uses two references that move through a data structure (usually a sorted array or linked list) to find pairs, subarrays, or partitions that satisfy a condition. It reduces O(n^2) brute-force pair comparisons to O(n) by eliminating impossible candidates through intelligent pointer movement.

## Key Signals (When to Use)
- The input is sorted (or should be sorted first)
- "Find a pair that sums to a target" in a sorted array
- "Remove duplicates in-place" or "move elements in-place"
- Problems involving comparing elements from both ends of a structure
- Partitioning an array around a pivot or condition

## Core Techniques
- **Opposite-Direction Pointers**: Start one pointer at the beginning and one at the end; move them inward based on a condition (e.g., two-sum on sorted array)
- **Same-Direction (Fast/Slow) Pointers**: One pointer advances faster than the other to detect cycles, find midpoints, or remove duplicates
- **Partitioning**: Use a write pointer and a read pointer to rearrange elements in-place

## Common Complexity
- Time: O(n) typical for a single pass; O(n log n) if sorting is required first
- Space: O(1) typical since pointers use constant extra space

## Classic Problems
- Valid Palindrome (Easy)
- Two Sum II - Input Array Is Sorted (Medium)
- 3Sum (Medium)
- Container With Most Water (Medium)
- Trapping Rain Water (Hard)
- Move Zeroes (Easy)
- Remove Duplicates from Sorted Array (Easy)

## Tips for Interviews
- Always ask if the input is sorted; if not, consider sorting it first
- Be precise about when each pointer moves -- draw out the logic before coding
- For 3Sum-type problems, fix one element and apply two pointers to the rest
- Handle duplicates explicitly to avoid duplicate results in combination problems
- Two pointers on a linked list is a separate sub-pattern (see Linked List)
