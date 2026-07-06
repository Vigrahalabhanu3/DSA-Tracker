# Heap - Study Notes

## Overview
A heap is a specialized tree-based data structure that satisfies the heap property — min-heap (parent ≤ children) or max-heap (parent ≥ children). Perfect for priority queues and k-way merging.

## Problems Solved (23 total)
1. Min Heap Implementation — Array-based, bubble up/down, O(log n) insert/extract (Medium)
2. Merge k Sorted Lists — k-way merge with min-heap, O(N log k) (Hard)
3. [Additional problems tracked in daily logs]

## Key Patterns
- **Min/Max Heap Implementation**: Array representation — parent = (i-1)//2, left = 2i+1, right = 2i+2. Bubble up on insert, bubble down on extract.
- **Top-K**: Use min-heap of size k — push all, pop when size > k
- **K-way merge**: Push all heads, pop smallest, push next from that list
- **Median maintenance**: Two heaps (max-heap for lower half, min-heap for upper)
- **Scheduling**: Min-heap by end time / priority
- **Dijkstra's**: Min-heap for shortest path frontier

## Key Insights
- Array-based heap: complete binary tree stored in array — no pointers needed
- Merge k Sorted Lists: Dummy head + tail pointer. Push all non-null heads. While heap: pop, append to result, push next from popped node's list. O(N log k).
- For k-way merge, heap stores (value, list_index) or (value, node).
- Python: `heapq` module — heapify, heappush, heappop. For custom objects, store tuple (priority, counter, obj).

## Progress
23 problems solved. Built heap fundamentals with Min Heap implementation, then applied it to k-way merge (first Hard!). Next targets: Top K Frequent Elements, Find Median from Data Stream, Task Scheduler.

---
*Updated: 2026-07-06*
