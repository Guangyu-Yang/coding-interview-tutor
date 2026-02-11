# Sorting & Searching

## Pattern Overview
Sorting and searching problems test your knowledge of fundamental algorithms and your ability to apply them creatively. Beyond implementing standard sorts, these problems often involve custom sorting criteria, leveraging sorted order for efficient queries, or recognizing that sorting is the key preprocessing step that unlocks a simpler solution. Searching problems extend beyond binary search to include order-statistic queries and specialized search strategies.

## Key Signals (When to Use)
- The problem asks to "sort by a custom criterion" or "find the kth element"
- Sorting the input simplifies the problem significantly (e.g., two pointers, greedy)
- "Find the median" or "find the kth largest/smallest"
- The problem involves merging sorted sequences
- Bucket sort or counting sort is efficient when the value range is bounded

## Core Techniques
- **Custom Comparators**: Sort with a lambda/comparator to order by problem-specific criteria (e.g., Largest Number: compare by which concatenation is larger)
- **Merge Sort Applications**: Count inversions, sort linked lists, or merge k sorted arrays using merge sort's divide-and-conquer structure
- **Quick Select**: O(n) average-case algorithm for finding the kth smallest/largest element without fully sorting; partition around a pivot and recurse on only one side
- **Counting Sort / Bucket Sort**: O(n + k) sorting when values fall in a bounded range k; useful for problems like Sort Colors (Dutch National Flag)
- **Index-Based Sorting**: Place element `i` at index `i` to find duplicates or missing numbers in O(n) time and O(1) space

## Common Complexity
- Time: O(n log n) for comparison-based sorting; O(n) for counting/bucket sort; O(n) average for Quick Select
- Space: O(1) for in-place sorts (heap sort, Quick Select); O(n) for merge sort

## Classic Problems
- Sort Colors (Medium) -- Dutch National Flag
- Kth Largest Element in an Array (Medium) -- Quick Select
- Largest Number (Medium)
- Sort List (Medium)
- Find the Duplicate Number (Medium)
- First Missing Positive (Hard)
- Count of Smaller Numbers After Self (Hard)
- Merge Intervals (Medium) -- sorting as preprocessing

## Tips for Interviews
- Know the time/space trade-offs of major sorting algorithms: quick sort (O(n log n) avg, O(1) space), merge sort (O(n log n), O(n) space), heap sort (O(n log n), O(1) space)
- Quick Select is the answer when you need the kth element without fully sorting
- If the value range is small, counting sort or bucket sort can beat O(n log n)
- Many problems are not "sorting problems" on the surface but become easy once you sort the input
- For linked list sorting, merge sort is preferred because it does not require random access
- The Dutch National Flag algorithm (3-way partition) is a classic technique for sorting with 3 categories in one pass
