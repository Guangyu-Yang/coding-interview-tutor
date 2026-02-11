# Greedy

## Pattern Overview
Greedy algorithms make the locally optimal choice at each step with the hope of finding the global optimum. They work when the problem has the greedy choice property (a local optimum leads to a global optimum) and optimal substructure. Greedy solutions are typically simpler and faster than DP but harder to prove correct -- the key challenge is recognizing when greedy works.

## Key Signals (When to Use)
- "Find the minimum number of steps/coins/operations" where a greedy strategy clearly dominates
- Scheduling or interval selection problems
- "Can you rearrange to satisfy a condition?" (often involves sorting + greedy assignment)
- The problem asks for a feasible solution and a simple rule always makes progress
- After sorting, processing items in order naturally leads to the optimal result

## Core Techniques
- **Sort and Greedily Assign**: Sort by one criterion (deadline, end time, ratio) and process in that order. Common in scheduling and interval problems.
- **Two-Pass Greedy**: Make a greedy pass left-to-right, then right-to-left, combining results (e.g., Candy problem)
- **Greedy Choice by Extremes**: Always pick the largest/smallest available option (e.g., activity selection by earliest finish time)
- **Exchange Argument**: Prove correctness by showing that swapping any non-greedy choice with the greedy choice does not worsen the solution
- **Jump Game Strategy**: Track the farthest reachable position and check if you can reach the end

## Common Complexity
- Time: O(n log n) typical when sorting is involved; O(n) if no sorting needed
- Space: O(1) to O(n) depending on the problem

## Classic Problems
- Maximum Subarray (Medium) -- Kadane's algorithm
- Jump Game (Medium)
- Jump Game II (Medium)
- Gas Station (Medium)
- Hand of Straights (Medium)
- Merge Triplets to Form Target Triplet (Medium)
- Partition Labels (Medium)
- Valid Parenthesis String (Medium)
- Candy (Hard)

## Tips for Interviews
- If you think greedy works, try to articulate why -- even informally. "Sorting by end time means we leave the most room for future intervals" is often enough.
- If you cannot convince yourself greedy is correct, consider DP instead
- Many greedy problems become obvious after sorting -- always consider what sorting criterion unlocks a greedy strategy
- Test your greedy approach on counterexamples before committing to it
- Greedy and DP are not mutually exclusive: some problems can be solved both ways, but greedy is preferred when it works because it is simpler
