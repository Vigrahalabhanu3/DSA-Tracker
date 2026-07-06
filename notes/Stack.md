# Stack - Study Notes

## Overview
Stack is a LIFO (Last-In-First-Out) data structure. Essential for problems involving nested structures, reversal, monotonic sequences, and backtracking undo operations.

## Problems Solved (15 total)
1. Valid Parentheses — Bracket matching with stack (Easy)
2. Min Stack — Auxiliary stack for O(1) minimum tracking (Easy)
3. [Additional problems tracked in daily logs]

## Key Patterns
- **Bracket/expression matching**: Push opens, pop and match closes — check stack empty at end
- **Monotonic stack**: Maintain increasing/decreasing order — Next Greater Element, Largest Rectangle
- **Two-stack pattern**: One for data, one for auxiliary info (Min Stack, Max Stack)
- **String reversal / undo**: Push chars/actions, pop to reverse or undo
- **Expression evaluation**: Infix → Postfix conversion, calculator problems

## Optimization Tips
- Use array + pointer instead of Stack class for better performance in languages with overhead
- For bracket matching: early exit if closing bracket doesn't match top of stack
- Monotonic stack: push indices, not values, when you need to calculate spans/widths

## Progress
15 problems solved. Comfortable with bracket matching and two-stack patterns. Next: monotonic stack problems (Daily Temperatures, Next Greater Element).

---
*Updated: 2026-07-06*
