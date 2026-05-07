# 🔹 BFS (Breadth First Search) 

## 🔹 What is BFS?

BFS stands for:

```text id="7w2jkc"
Breadth First Search
```

It visits nodes **level by level**.

👉 First visit all neighbors
👉 Then move to next level

---

## 🔹 Example Tree

```text id="9q5mxt"
       1
      / \
     2   3
    / \   \
   4   5   6
```

---

## BFS Traversal

Visit order:

```text id="6k8pza"
1 → 2 → 3 → 4 → 5 → 6
```

---

## Why?

* Start at root
* Visit all nodes at current level
* Move deeper gradually

---

# 🔹 Data Structure Used

👉 Queue

Because queue follows FIFO.

---

## BFS Flow

```text id="u3t7bd"
Push root
Pop node
Push neighbors
Repeat
```

---

# 🔹 Algorithm

1. Insert starting node into queue
2. Mark visited
3. While queue not empty:

   * Remove front node
   * Visit it
   * Add unvisited neighbors

---

# 🔹 Code (Tree BFS)

```python id="e5m4qa"
from collections import deque

def bfs(graph, start):
    visited = set()
    queue = deque([start])

    visited.add(start)

    while queue:
        node = queue.popleft()
        print(node)

        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)
```

---

# 🔹 Graph Example

```python id="6h1kyo"
graph = {
    1: [2, 3],
    2: [4, 5],
    3: [6],
    4: [],
    5: [],
    6: []
}
```

Call:

```python id="s8w2dn"
bfs(graph, 1)
```

Output:

```text id="9v4gtr"
1
2
3
4
5
6
```

---

# 🔹 Dry Run

Initial:

```text id="7n1dlu"
queue = [1]
```

Pop 1:

```text id="3y8kfe"
visit 1
add 2,3
queue = [2,3]
```

Pop 2:

```text id="0j4vkh"
visit 2
add 4,5
queue = [3,4,5]
```

Continue similarly.

---

# 🔹 Time Complexity

For graph:

O(V+E)

Where:

* V = vertices
* E = edges

---

# 🔹 Space Complexity

O(V)

Queue + visited set.

---

# 🔹 Applications of BFS

---

## 1. Shortest Path (Unweighted Graph)

Find shortest distance.

---

## 2. Level Order Traversal

Binary trees.

---

## 3. Grid Problems

Examples:

* Rotten oranges
* Flood fill
* Number of islands

---

## 4. Social Network

Friend suggestions.

---

# 🔹 BFS vs DFS

| Feature        | BFS        | DFS             |
| -------------- | ---------- | --------------- |
| Data Structure | Queue      | Stack/Recursion |
| Traversal      | Level wise | Depth wise      |

---
