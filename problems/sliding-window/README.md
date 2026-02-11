# Sliding Window

## Pattern Overview
The sliding window technique maintains a dynamic window (subarray or substring) over a sequence and slides it to efficiently compute aggregates or find optimal sub-sequences. Instead of recalculating from scratch for every possible window, you incrementally update the state as the window expands or contracts, turning O(n*k) brute force into O(n).

## Key Signals (When to Use)
- "Find the longest/shortest substring/subarray satisfying a condition"
- "Maximum sum subarray of size k" or any fixed-size window aggregate
- The problem involves contiguous elements in a string or array
- You need to track a constraint (character count, sum, distinct elements) over a range
- "At most k distinct" or "at most k replacements"

## Core Techniques
- **Fixed-Size Window**: Slide a window of exactly size k; add the new element, remove the old one each step
- **Variable-Size Window (Expand/Shrink)**: Expand the right boundary to include more elements; shrink the left boundary when a constraint is violated. Track the optimal window seen so far.
- **Hash Map + Window**: Use a frequency map inside the window to track character/element counts and validate constraints

## Common Complexity
- Time: O(n) typical -- each element is added and removed from the window at most once
- Space: O(1) to O(k) depending on what state the window tracks

## Classic Problems
- Best Time to Buy and Sell Stock (Easy)
- Longest Substring Without Repeating Characters (Medium)
- Longest Repeating Character Replacement (Medium)
- Permutation in String (Medium)
- Minimum Window Substring (Hard)
- Sliding Window Maximum (Hard)
- Minimum Size Subarray Sum (Medium)

## Tips for Interviews
- Clearly define what your window represents and what invariant it maintains
- The shrink condition is the hardest part -- get this right before coding
- Use a hash map for character frequency problems; update it incrementally
- When the window is invalid, shrink from the left until it becomes valid again
- For "minimum window" problems, track the best answer every time the window is valid; for "maximum window" problems, track it every time you expand
