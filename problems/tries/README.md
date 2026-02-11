# Tries

## Pattern Overview
A trie (prefix tree) is a tree-like data structure for efficiently storing and searching strings by their prefixes. It enables O(m) lookup, insertion, and prefix-matching where m is the word length, regardless of how many words are stored. Tries are the go-to structure when problems involve prefix queries, word dictionaries, or character-by-character search.

## Key Signals (When to Use)
- "Search for words with a given prefix"
- "Implement autocomplete or typeahead"
- "Find if any word in the dictionary is a prefix of another"
- Word search in a grid combined with a dictionary
- The problem involves matching, building, or validating words character by character

## Core Techniques
- **Standard Trie**: Each node has a map of children (character -> node) and an `is_end` flag. Insert by walking down and creating nodes; search by walking down and checking flags.
- **Wildcard Search**: For patterns with wildcards (like `.`), use DFS/backtracking at wildcard positions to explore all children
- **Trie + DFS/Backtracking**: Combine a trie with grid search (e.g., Word Search II) -- prune branches early when no prefix matches

## Common Complexity
- Time: O(m) per insert/search where m is word length; O(n * m) to build trie for n words
- Space: O(n * m) worst case for n words of average length m (though prefix sharing reduces this in practice)

## Classic Problems
- Implement Trie (Prefix Tree) (Medium)
- Design Add and Search Words Data Structure (Medium)
- Word Search II (Hard)
- Replace Words (Medium)
- Longest Word in Dictionary (Medium)

## Tips for Interviews
- Implement the TrieNode class first with `children` (dict or array of size 26) and `is_end` boolean
- Using a dictionary for children is simpler to code and handles any character set; a fixed-size array is faster but limited to lowercase letters
- For Word Search II, building a trie of all words and doing one DFS from each cell is far more efficient than searching for each word separately
- Remember to mark the end of words -- a common bug is matching prefixes that are not complete words
- Tries can be combined with other patterns (backtracking, BFS) for complex problems
