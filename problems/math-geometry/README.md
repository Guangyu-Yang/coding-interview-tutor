# Math & Geometry

## Pattern Overview
Math and geometry problems test your ability to identify mathematical patterns, properties, and formulas rather than relying on standard data structures. These problems often have elegant O(1) or O(n) solutions once you spot the mathematical insight. Common themes include modular arithmetic, number theory, matrix operations, and geometric reasoning.

## Key Signals (When to Use)
- The problem involves mathematical operations (power, factorial, GCD, primes)
- Matrix rotation, spiral traversal, or coordinate geometry
- "Find a pattern" in a sequence of numbers
- Problems involving digits, remainders, or number properties
- Geometric relationships (distance, area, overlap of shapes)
- The brute force is simple but the interviewer expects a mathematical shortcut

## Core Techniques
- **Modular Arithmetic**: Use properties like `(a + b) % m = ((a % m) + (b % m)) % m` to prevent overflow and simplify calculations
- **Matrix Manipulation**: Rotate by transposing then reversing rows; spiral order uses boundary pointers
- **Math Properties/Formulas**: Sum of 1..n = n*(n+1)/2; Gauss's formula; pigeonhole principle
- **GCD / LCM**: Euclidean algorithm for GCD; LCM = (a * b) / GCD(a, b)
- **Geometry Basics**: Distance formula, cross product for orientation, checking collinearity

## Common Complexity
- Time: O(1) to O(n) for number theory; O(n^2) for matrix operations on n x n matrix
- Space: O(1) typical for math; O(n^2) for matrix storage

## Classic Problems
- Rotate Image (Medium)
- Spiral Matrix (Medium)
- Set Matrix Zeroes (Medium)
- Happy Number (Easy)
- Plus One (Easy)
- Pow(x, n) (Medium)
- Multiply Strings (Medium)
- Detect Squares (Medium)

## Tips for Interviews
- For matrix rotation: rotate 90 degrees clockwise = transpose + reverse each row
- Look for patterns by computing the first few values by hand
- Watch for integer overflow -- use modular arithmetic or language-specific big integers
- Many "clever" math problems are just about recognizing a formula or invariant
- If the brute force is obvious but slow, ask yourself: "Is there a mathematical relationship that eliminates the loop?"
- For geometry, draw diagrams and label coordinates before coding
