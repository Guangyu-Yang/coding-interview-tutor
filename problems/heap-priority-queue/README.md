# Heap / Priority Queue

## Pattern Overview
A heap (priority queue) efficiently maintains access to the minimum or maximum element in a dynamic collection. Use it when you need to repeatedly extract the smallest or largest element, maintain a running top-k, or merge multiple sorted sequences. Heaps provide O(log n) insert/extract and O(1) peek at the extremum.

## Key Signals (When to Use)
- "Find the kth largest/smallest element"
- "Merge k sorted lists/arrays"
- "Continuously process the smallest/largest available item"
- "Find the median from a data stream" (two heaps)
- Scheduling problems where you pick the next task by priority
- "Top k frequent elements" or "k closest points"

## Core Techniques
- **Min-Heap for Top-K Largest**: Maintain a min-heap of size k; when it exceeds k, pop the smallest. The heap always holds the k largest seen so far.
- **Max-Heap for Top-K Smallest**: Mirror of the above (negate values in languages without a max-heap)
- **Two Heaps (Median Maintenance)**: Use a max-heap for the lower half and a min-heap for the upper half; balance sizes to get the median in O(1)
- **K-Way Merge**: Push the first element from each list into a min-heap; pop the minimum and push the next element from that list
- **Lazy Deletion**: Mark elements as invalid instead of removing them; skip invalid elements on pop

## Common Complexity
- Time: O(n log k) for top-k problems; O(n log n) for heap sort; O(log n) per push/pop
- Space: O(k) for top-k; O(n) for a heap of all elements

## Classic Problems
- Kth Largest Element in a Stream (Easy)
- Last Stone Weight (Easy)
- Kth Largest Element in an Array (Medium)
- K Closest Points to Origin (Medium)
- Task Scheduler (Medium)
- Design Twitter (Medium)
- Find Median from Data Stream (Hard)
- Merge k Sorted Lists (Hard)

## Tips for Interviews
- In Python, `heapq` is a min-heap; for a max-heap, negate the values
- Always clarify if you need the kth largest (min-heap of size k) or kth smallest (max-heap of size k)
- For "median" problems, practice the two-heap balancing technique until it is second nature
- When merging k sorted sequences, always push the source index along with the value so you know where to pull the next element from
- A heap is not the same as a sorted array -- you cannot efficiently find arbitrary elements, only the min/max
