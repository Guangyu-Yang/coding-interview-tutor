# Stack

## Pattern Overview
Stack problems exploit the last-in-first-out (LIFO) property to process nested structures, match pairs, or maintain a monotonic ordering. A stack is the natural choice whenever you need to "remember" previous elements and process them in reverse order, such as matching parentheses, evaluating expressions, or finding the next greater element.

## Key Signals (When to Use)
- "Valid parentheses" or any bracket/nesting matching problem
- "Next greater/smaller element" for each position in an array
- Evaluating or parsing arithmetic expressions (postfix, infix)
- Problems that involve undoing or backtracking to a previous state
- Maintaining a monotonically increasing or decreasing sequence

## Core Techniques
- **Matching Pairs**: Push opening symbols; pop and compare when you see a closing symbol
- **Monotonic Stack**: Maintain a stack where elements are in sorted order; pop elements that violate the order to answer "next greater/smaller" queries in O(n)
- **Expression Evaluation**: Use one stack for operands and one for operators, or convert to postfix notation
- **State Stack**: Push state onto the stack before entering a nested context; pop to restore it when leaving

## Common Complexity
- Time: O(n) typical -- each element is pushed and popped at most once
- Space: O(n) worst case for the stack

## Classic Problems
- Valid Parentheses (Easy)
- Min Stack (Medium)
- Evaluate Reverse Polish Notation (Medium)
- Daily Temperatures (Medium)
- Car Fleet (Medium)
- Largest Rectangle in Histogram (Hard)
- Generate Parentheses (Medium) -- uses stack-like recursion

## Tips for Interviews
- For monotonic stack problems, decide upfront whether the stack should be increasing or decreasing
- When the stack is not empty and the current element triggers a pop, that pop usually produces part of the answer
- Draw out the stack state for a small example before coding to verify your logic
- Consider what to do when the stack is empty at the end -- some problems need a sentinel value
- Stacks and recursion are closely related; any recursive solution can be converted to an iterative one using an explicit stack
