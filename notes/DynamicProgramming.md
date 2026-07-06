# Dynamic Programming - Study Notes

## Overview
DP solves problems by breaking them into overlapping subproblems and storing results (memoization or tabulation). Key characteristics: optimal substructure + overlapping subproblems. Currently a flagged weak area — building from easy → medium.

## Problems Solved (19 total)
1. Climbing Stairs — Bottom-up DP, Fibonacci pattern (Easy)
2. [Additional problems tracked in daily logs]

## Key Patterns
- **Bottom-up (Tabulation)**: Build dp array iteratively — dp[i] depends on previous states
- **Top-down (Memoization)**: Recursive with cache — solve(i) = memo.get(i) or compute
- **1D DP**: Fibonacci, Climbing Stairs, House Robber, Coin Change
- **2D DP**: Grid paths, Edit Distance, LCS
- **Knapsack variants**: 0/1 Knapsack, Unbounded Knapsack, Subset Sum
- **LIS (Longest Increasing Subsequence)**: O(n²) DP → O(n log n) with patience sorting

## Key Insights
- Climbing Stairs = Fibonacci in disguise: dp[i] = dp[i−1] + dp[i−2]
- Start with recursion → identify overlapping subproblems → add memoization → convert to bottom-up
- Space optimization: if only last 1-2 states needed, use variables instead of full array

## Progress
19 problems solved. Building fundamentals — started with easy Fibonacci-pattern problems. Next targets: House Robber, Coin Change, Longest Increasing Subsequence.

---
*Updated: 2026-07-06*
