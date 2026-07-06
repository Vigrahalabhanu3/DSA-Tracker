# Dynamic Programming - Study Notes

## Overview
DP solves problems by breaking them into overlapping subproblems and storing results (memoization or tabulation). Key characteristics: optimal substructure + overlapping subproblems. Currently a flagged weak area — now at 21 problems and gaining momentum.

## Problems Solved (21 total)
1. Climbing Stairs — Bottom-up DP, Fibonacci pattern (Easy)
2. House Robber — 1D DP: skip-or-take decision, O(n) time / O(1) space (Medium)
3. Coin Change — Unbounded knapsack: dp[amount] = min coins, O(amount × coins) (Medium)
4. [Additional problems tracked in daily logs]

## Key Patterns
- **Bottom-up (Tabulation)**: Build dp array iteratively — dp[i] depends on previous states
- **Top-down (Memoization)**: Recursive with cache — solve(i) = memo.get(i) or compute
- **1D DP**: Fibonacci, Climbing Stairs, House Robber, Coin Change
- **2D DP**: Grid paths, Edit Distance, LCS
- **Knapsack variants**: 0/1 Knapsack (House Robber), Unbounded Knapsack (Coin Change), Subset Sum
- **LIS (Longest Increasing Subsequence)**: O(n²) DP → O(n log n) with patience sorting

## Key Insights
- **House Robber**: dp[i] = max(dp[i-1], dp[i-2] + nums[i]). Not about alternating — each house: skip or take+skip adjacent.
- **Coin Change**: Initialize dp[0]=0, rest=INF. dp[i] = min(dp[i], 1 + dp[i - coin]). Return -1 if dp[amount]=INF.
- Climbing Stairs = Fibonacci in disguise: dp[i] = dp[i−1] + dp[i−2]
- Start with recursion → identify overlapping subproblems → add memoization → convert to bottom-up
- Space optimization: if only last 1-2 states needed, use variables instead of full array

## Progress
21 problems solved. Broke into mediums — House Robber and Coin Change established the core DP intuition. Next targets: Longest Increasing Subsequence, Edit Distance, 0/1 Knapsack.

---
*Updated: 2026-07-06*
