# Bit Manipulation

## Pattern Overview
Bit manipulation problems require operating directly on the binary representation of numbers using bitwise operators (AND, OR, XOR, NOT, shifts). These techniques can solve certain problems in O(1) space and O(n) time that would otherwise require extra data structures. XOR is especially powerful for "find the unique element" problems since `a ^ a = 0` and `a ^ 0 = a`.

## Key Signals (When to Use)
- "Find the single number" that appears once while others appear twice
- "Count the number of 1 bits" or "reverse bits"
- The problem explicitly involves binary representation or powers of 2
- You need O(1) space and cannot use extra data structures
- Problems involving subsets (each subset maps to a bitmask)

## Core Techniques
- **XOR for Cancellation**: XOR all elements; duplicates cancel out, leaving the unique one. `a ^ a = 0`, `a ^ 0 = a`, and XOR is commutative and associative.
- **Bit Masking**: Use `n & (1 << i)` to check if bit i is set; `n | (1 << i)` to set it; `n & ~(1 << i)` to clear it
- **Brian Kernighan's Algorithm**: `n & (n - 1)` removes the lowest set bit; repeat to count set bits in O(k) where k is the number of set bits
- **Shift Operations**: Left shift (`<<`) multiplies by 2; right shift (`>>`) divides by 2. Useful for building numbers bit by bit.
- **Bitmask DP**: Represent subsets as bitmasks; iterate over all 2^n subsets. Used for small n (typically n <= 20).

## Common Complexity
- Time: O(n) for scanning; O(1) or O(32) for single-number bit operations
- Space: O(1) typical -- no extra data structures needed

## Classic Problems
- Single Number (Easy)
- Number of 1 Bits (Easy)
- Counting Bits (Easy)
- Reverse Bits (Easy)
- Missing Number (Easy)
- Sum of Two Integers (Medium)
- Reverse Integer (Medium)

## Tips for Interviews
- XOR is the go-to tool for "find the element that appears once" problems
- Remember: `n & (n - 1)` clears the lowest set bit -- this is used surprisingly often
- Power of 2 check: `n > 0 and n & (n - 1) == 0`
- Practice converting small numbers to binary by hand to build intuition
- Bit manipulation can replace hash sets for certain problems, saving space
- Be careful with signed vs unsigned integers and language-specific behavior of right shift
