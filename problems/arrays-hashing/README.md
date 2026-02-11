# Arrays & Hashing

## Pattern Overview
Arrays and hashing problems form the foundation of most coding interviews. Use hash maps to trade space for time when you need fast lookups, frequency counting, or duplicate detection. Many problems that appear to require O(n^2) brute force can be solved in O(n) with a well-chosen hash map.

## Key Signals (When to Use)
- "Find if a pair/group satisfies a condition" (hash map for complement lookup)
- "Count frequencies" or "find duplicates" (hash map or hash set)
- "Group elements by some property" (hash map with lists as values)
- The problem involves checking membership or existence quickly
- You need to map one value to another for constant-time retrieval

## Core Techniques
- **Hash Map for Complement Lookup**: Store seen values and check if the complement exists (e.g., Two Sum)
- **Frequency Counter**: Count occurrences with a hash map, then reason about the counts
- **Hash Set for Deduplication**: Use a set to track seen elements or enforce uniqueness
- **Index Mapping**: Map values to indices or vice versa for O(1) positional lookups
- **Encoding/Grouping**: Use a canonical form as a hash key to group related items (e.g., sorted string for anagrams)

## Common Complexity
- Time: O(n) typical with hash map; O(n log n) if sorting is involved
- Space: O(n) typical for storing elements in a hash map/set

## Classic Problems
- Two Sum (Easy)
- Contains Duplicate (Easy)
- Valid Anagram (Easy)
- Group Anagrams (Medium)
- Top K Frequent Elements (Medium)
- Product of Array Except Self (Medium)
- Longest Consecutive Sequence (Medium)
- Encode and Decode Strings (Medium)

## Tips for Interviews
- Always consider whether a hash map can reduce a nested loop to a single pass
- Clarify what to return when there are ties or multiple valid answers
- When using arrays as keys in a hash map, convert them to tuples or strings first
- Watch for off-by-one errors when mapping indices
- If the value range is small and known, an array can replace a hash map for better constant factors
