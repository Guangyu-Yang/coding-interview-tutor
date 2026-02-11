# Intervals

## Pattern Overview
Interval problems involve ranges defined by a start and end point. The core strategy is almost always to sort intervals by start (or end) time and then process them sequentially, merging overlapping ones, finding gaps, or counting conflicts. Once sorted, interval relationships (overlap, contain, disjoint) become easy to check with simple comparisons.

## Key Signals (When to Use)
- The input is a list of intervals [start, end]
- "Merge overlapping intervals" or "insert a new interval"
- "Find the minimum number of rooms/resources" (interval scheduling)
- "Check if intervals overlap" or "find free time"
- Meeting rooms, job scheduling, or time-range problems

## Core Techniques
- **Sort by Start Time**: Sort intervals by their start point; then scan linearly to merge overlaps or detect conflicts
- **Merge Overlapping**: After sorting, merge interval `i` with interval `i+1` if they overlap (start of next <= end of current); extend the end to `max(end_current, end_next)`
- **Sweep Line / Event Points**: Convert intervals into +1 (start) and -1 (end) events; sort events and sweep to find peak overlap count
- **Min-Heap for Scheduling**: Use a min-heap of end times to track active intervals; the heap size at any point gives the number of concurrent intervals

## Common Complexity
- Time: O(n log n) for sorting; O(n) for the linear scan
- Space: O(n) for the output or event list; O(1) extra if merging in place

## Classic Problems
- Meeting Rooms (Easy)
- Meeting Rooms II (Medium)
- Merge Intervals (Medium)
- Insert Interval (Medium)
- Non-overlapping Intervals (Medium)
- Minimum Interval to Include Each Query (Hard)
- Interval List Intersections (Medium)

## Tips for Interviews
- Always sort first -- almost every interval problem starts with sorting by start or end time
- Decide whether to sort by start or end: merge problems use start; greedy selection problems (like minimum removals) often use end
- Draw intervals on a number line for a small example to visualize overlaps
- Two intervals `[a, b]` and `[c, d]` overlap if and only if `a < d and c < b` (assuming a <= b, c <= d)
- The sweep line technique is powerful for "maximum concurrent" or "point of maximum overlap" problems
