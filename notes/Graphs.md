# Graphs — Comprehensive Notes

## Representations

### 1. Adjacency List (Most Common for DSA)
```python
graph = {
    0: [1, 2],
    1: [0, 3],
    2: [0],
    3: [1]
}
```

### 2. Adjacency Matrix
```python
graph = [
    [0, 1, 1, 0],
    [1, 0, 0, 1],
    [1, 0, 0, 0],
    [0, 1, 0, 0]
]
```

## Core Algorithms

### DFS (Depth-First Search)
```python
def dfs(node, visited, graph):
    visited.add(node)
    for neighbor in graph[node]:
        if neighbor not in visited:
            dfs(neighbor, visited, graph)
```
- Time: O(V + E)
- Space: O(V) for recursion stack

### BFS (Breadth-First Search)
```python
from collections import deque
def bfs(start, graph):
    queue = deque([start])
    visited = {start}
    while queue:
        node = queue.popleft()
        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)
```
- Time: O(V + E)
- Space: O(V) for queue

## Common Patterns

### Connected Components
Use DFS/BFS to count islands or components

### Cycle Detection
- **Undirected**: If revisit non-parent node, cycle exists
- **Directed**: Use color marking (white/gray/black)

### Topological Sort
DFS + stack for DAG ordering

## Last Updated: 2026-05-26
**Reviewed by**: Night Review Session
**Confidence Level**: 🟡 Medium
