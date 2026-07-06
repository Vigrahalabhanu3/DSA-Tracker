# Hashing - Study Notes

## Overview
Hash-based data structures (HashMap, HashSet) provide O(1) average-time operations for insertion, deletion, and lookup. Core to solving pair-finding, frequency counting, and duplicate detection problems efficiently.

## Problems Solved (16 total)
1. Two Sum — Hash map complement lookup, O(n)
2. Contains Duplicate — Hash set, O(n)
3. Top K Frequent Elements — Hash map + heap, O(n log k)
4. [Additional problems tracked in daily logs]

## Key Patterns
- **Complement lookup**: Store target − current and check existence (Two Sum pattern)
- **Frequency counting**: Hash map → sort by frequency or use bucket sort
- **Duplicate detection**: HashSet for seen elements
- **Caching/memoization**: Store computed results for O(1) lookup
- **Character/word counts**: Array[26] or hash map for string problems

## Optimization Tips
- Use array instead of hash map when keys are known and small (e.g., lowercase letters → int[26])
- Pre-size HashMap to avoid rehashing overhead
- Python: `collections.Counter`, `defaultdict` for cleaner code

## Progress
16 problems solved. Comfortable with complement-lookup and frequency-counting patterns. Next: hash-based caching for DP optimization.

---
*Updated: 2026-07-06*
