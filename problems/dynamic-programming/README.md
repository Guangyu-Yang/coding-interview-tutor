# Dynamic Programming

## Pattern Overview
Dynamic programming (DP) solves problems by breaking them into overlapping subproblems and caching their results to avoid redundant computation. It applies when a problem has optimal substructure (the optimal solution is built from optimal solutions to subproblems) and overlapping subproblems (the same subproblems recur many times). The two approaches are top-down (memoized recursion) and bottom-up (iterative tabulation).

## Key Signals (When to Use)
- "Find the minimum/maximum cost/profit/count"
- "How many ways to reach a target?"
- "Can you partition/split into parts satisfying a constraint?"
- The problem has optimal substructure and the brute-force involves repeated work
- The problem can be framed as "make a sequence of decisions, each depending on previous decisions"
- String comparison problems (edit distance, longest common subsequence)

## Core Techniques
- **1D DP**: State depends on one variable (e.g., `dp[i]` = answer for first i items). Examples: climbing stairs, house robber.
- **2D DP**: State depends on two variables (e.g., `dp[i][j]` for substrings or two sequences). Examples: longest common subsequence, edit distance.
- **Knapsack Variants**: 0/1 knapsack (take or skip each item), unbounded knapsack (unlimited copies), bounded knapsack. Core to many "target sum" and "partition" problems.
- **Interval DP**: `dp[i][j]` represents the answer for the subarray/substring from i to j. Expand by trying all split points.
- **State Machine DP**: Model the problem as transitions between states (e.g., buy/sell stock with cooldown).
- **Space Optimization**: When `dp[i]` only depends on `dp[i-1]`, use two variables or a rolling array instead of a full table.

## Common Complexity
- Time: O(n^2) or O(n * target) typical; varies widely by problem
- Space: O(n) to O(n^2) typical; often reducible with rolling arrays

## Classic Problems
- Climbing Stairs (Easy)
- House Robber (Medium)
- Coin Change (Medium)
- Longest Increasing Subsequence (Medium)
- Longest Common Subsequence (Medium)
- Word Break (Medium)
- Partition Equal Subset Sum (Medium)
- Unique Paths (Medium)
- Edit Distance (Medium)
- Decode Ways (Medium)
- Best Time to Buy and Sell Stock with Cooldown (Medium)
- Regular Expression Matching (Hard)
- Burst Balloons (Hard)

## Tips for Interviews
- Start with the brute-force recursive solution, then add memoization -- this is easier than jumping straight to bottom-up
- Clearly define what `dp[i]` (or `dp[i][j]`) represents in one English sentence before writing the recurrence
- Identify the base cases and the transition (recurrence relation) -- these are the two critical pieces
- If you cannot figure out the recurrence, try working through a small example and see how the answer for a larger input depends on smaller inputs
- Look for opportunities to reduce space: if you only need the previous row, do not store the entire table
- Practice recognizing which DP pattern (1D, 2D, knapsack, interval) a problem maps to -- this is the hardest skill and comes with practice
