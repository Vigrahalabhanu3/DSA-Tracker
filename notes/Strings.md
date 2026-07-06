# Strings - Study Notes

## Overview
String problems test manipulation, pattern matching, and sliding window techniques. 22 problems solved — strong coverage across common patterns.

## Problems Solved (22 total)
1. Longest Substring Without Repeating Characters — Sliding window, O(n) two-pointer (Medium)
2. [Additional problems tracked in daily logs]

## Key Patterns
- **Sliding Window**: Two pointers (left/right), expand right, shrink left when invariant violated
- **Two Pointers**: Palindrome check, reverse, valid palindrome
- **Hash Map / Set**: Character frequency, anagram detection, first unique char
- **Trie**: Prefix matching, autocomplete, word search
- **KMP / Rabin-Karp**: Substring search (advanced)
- **String DP**: Edit distance, LCS, regex matching

## Key Insights
- Longest Substring Without Repeating: Maintain set/array[256] of seen chars. When duplicate found at right, remove s[left] and increment left until it's gone. Track max(right - left + 1).
- Sliding window template: while(condition_violated) { shrink left }. Always expand right unconditionally.
- For anagram problems: fixed-size window + frequency array comparison (O(26) per check).
- Use array[26] or array[256] instead of HashMap for ASCII/lowercase — constant time is smaller constant.

## Progress
22 problems solved. Sliding window is now well-understood. Next targets: Group Anagrams, Minimum Window Substring, Longest Palindromic Substring.

---
*Updated: 2026-07-06*
