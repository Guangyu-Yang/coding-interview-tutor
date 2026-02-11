# Coding Interview Tutor

An interactive coding interview preparation environment powered by Claude Code. Uses Socratic, guided learning to help you deeply understand algorithm patterns - not just memorize solutions.

## How It Works

This repo is designed to be used with [Claude Code](https://claude.com/claude-code). Open the repo in Claude Code and start a conversation. The tutor will guide you through problems using a structured 6-phase workflow.

### The 6-Phase Workflow

For every problem, the tutor walks you through:

1. **Understand the Problem** - Analogies, examples, and edge cases until you truly get it
2. **Brute Force Solution** - Identify the simplest approach (conceptually, no code)
3. **Complexity Analysis** - Analyze time/space complexity and identify bottlenecks
4. **Optimal Solution** - Discover the key insight and optimal approach together
5. **Implementation** - Build the solution block by block in your preferred language
6. **Review & Connect** - Reinforce patterns and connect to related problems

### What You Can Do

- **Random practice**: Say "give me a problem" and pick a category/difficulty
- **Company prep**: Say "practice Google problems" to filter by company
- **Import problems**: Share a link, paste text, or upload a PDF
- **Track progress**: Your progress is automatically tracked across sessions

## Getting Started

1. Clone this repo
2. Open it in Claude Code
3. Say "let's practice" or "give me a problem"

## Problem Categories

| Category | Description |
|----------|-------------|
| Arrays & Hashing | Hash maps, frequency counting, prefix sums |
| Two Pointers | Left/right pointers, fast/slow pointers |
| Sliding Window | Fixed and variable window techniques |
| Stack | Monotonic stack, parentheses, next greater element |
| Binary Search | Search on arrays and answer spaces |
| Linked List | Pointer manipulation, reversal, cycle detection |
| Trees | DFS, BFS, BST operations, path problems |
| Tries | Prefix matching, word search |
| Heap / Priority Queue | Top-K, merge K sorted, median |
| Backtracking | Permutations, combinations, constraint satisfaction |
| Graphs | BFS/DFS, topological sort, shortest path, union-find |
| Dynamic Programming | 1D/2D DP, knapsack, string DP |
| Greedy | Interval scheduling, activity selection |
| Intervals | Merge, insert, meeting rooms |
| Math & Geometry | Modular arithmetic, GCD, geometry |
| Bit Manipulation | XOR tricks, bit counting |
| Sorting & Searching | Custom sorts, counting sort, quick select |

## Problem Bank

The repo includes 150+ curated problems from popular interview lists including Blind 75, NeetCode 150, and frequently asked questions at top tech companies (Google, Meta, Amazon, Apple, Microsoft, and more).

## Teaching Philosophy

- **Socratic Method**: Guides you to discover solutions through questions, not lecturing
- **No Skipping**: Every phase matters - understanding WHY is more important than WHAT
- **Pattern Recognition**: Teaches you to recognize and apply algorithmic patterns
- **Active Verification**: Checks your understanding before moving forward
- **No Guessing**: All complexity analysis and technical details are verified

## Privacy

Your personal data stays private:
- `profile/` - Your preferences and settings
- `progress/` - Your study tracker
- `sessions/` - Your session notes
- `private-problems/` - Problems you import

These directories are gitignored and never pushed to the remote repo.

## License

MIT
