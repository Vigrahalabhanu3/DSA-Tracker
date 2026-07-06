# Backtracking - Study Notes

## Overview
Backtracking systematically explores all candidate solutions by building incrementally and abandoning ("backtracking") paths that can't lead to a valid solution. Think of it as DFS through a decision tree.

## Problems Solved (24 total)
1. Subsets — Include/exclude each element, O(2ⁿ) (Medium)
2. Combination Sum — Build combinations to target sum, unlimited uses, pruning (Medium)
3. [Additional problems tracked in daily logs]

## Key Patterns
- **Subsets pattern**: For each element: include it OR exclude it. Push → recurse → pop.
- **Combination Sum pattern**: For each candidate (from start): push if ≤ target → recurse with same index → pop. Sort for early pruning.
- **Permutations pattern**: Swap or track used[] array, build ordering.
- **N-Queens / Sudoku**: Constraint satisfaction — place, check validity, recurse, remove.
- **Palindrome Partitioning**: Partition string into palindromic substrings.

## Template
```
def backtrack(path, state):
    if goal_reached(state):
        result.append(path.copy())
        return
    for choice in get_candidates(state):
        if is_valid(choice, state):
            path.append(choice)        # choose
            backtrack(path, new_state)  # explore
            path.pop()                  # unchoose (backtrack)
```

## Key Insights
- Subsets vs Combination Sum: Subsets is binary choice per element. Combination Sum is build-to-target with repeats — use `start` index to avoid duplicates.
- Sorting candidates enables early pruning (break when candidate > remaining target).
- Always copy `path` when adding to results — otherwise it mutates.
- The `start` parameter is the key to avoiding duplicate combinations.

## Progress
24 problems solved. Subsets and Combination Sum are the two fundamental backtracking patterns. Next: Permutations II (handling duplicates), N-Queens, Palindrome Partitioning.

---
*Updated: 2026-07-06*
