# Dynamic Programming (DP) — Comprehensive Notes

## Core Concepts

### 1. Definition
DP is an optimization technique that breaks a problem into overlapping subproblems and stores results to avoid redundant calculations.

### 2. When to Use DP
- Optimal substructure (solution built from subproblem solutions)
- Overlapping subproblems (same sub-problems recalculated)
- Examples: Fibonacci, coin change, longest subsequence, knapsack

### 3. DP Approaches

#### Top-Down (Memoization)
```python
memo = {}
def fib(n):
    if n in memo: return memo[n]
    if n <= 1: return n
    memo[n] = fib(n-1) + fib(n-2)
    return memo[n]
```

#### Bottom-Up (Tabulation)
```python
def fib(n):
    dp = [0] * (n+1)
    dp[1] = 1
    for i in range(2, n+1):
        dp[i] = dp[i-1] + dp[i-2]
    return dp[n]
```

## Common Patterns

### Pattern 1: Sequence DP
**Problem**: Maximum sum of non-adjacent elements
```
dp[i] = max(dp[i-1], arr[i] + dp[i-2])
```

### Pattern 2: 2D DP (Knapsack)
```
dp[i][w] = max(dp[i-1][w], arr[i] + dp[i-1][w-weight[i]])
```

### Pattern 3: String DP (LCS, Edit Distance)
```
dp[i][j] = match ? dp[i-1][j-1] : 1 + min(dp[i-1][j], dp[i][j-1])
```

## Time Complexity Guide

| Problem | Approach | Time | Space |
|---------|----------|------|-------|
| Fibonacci | Memoization | O(n) | O(n) |
| Knapsack | Tabulation | O(n*W) | O(n*W) |
| LCS | 2D DP | O(m*n) | O(m*n) |
| Coin Change | BFS/DP | O(n*m) | O(n) |

## Last Updated: 2026-05-26
**Reviewed by**: Night Review Session
**Confidence Level**: 🟡 Medium (weak areas identified)
