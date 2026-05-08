# 🔹 DFS (Depth First Search)

## 🔹 What is DFS?

DFS stands for:

```text id="3q8pva"
Depth First Search
```

It visits nodes by going as deep as possible first.

👉 Go deep
👉 Backtrack
👉 Explore next path

---

## 🔹 Example Tree

```text id="8m2wfr"
       1
      / \
     2   3
    / \   \
   4   5   6
```

---

## DFS Traversal

Visit order:

```text id="4v7zpk"
1 → 2 → 4 → 5 → 3 → 6
```

---

## Why?

* Start from root
* Go deep into left branch
* Backtrack
* Explore remaining branches

---

# 🔹 Data Structure Used

👉 Stack
or
👉 Recursion (uses call stack internally)

---

# 🔹 DFS Flow

```text id="6n1jkt"
Visit node
Go deeper
Backtrack
Repeat
```

---

# 🔹 Algorithm

1. Visit current node
2. Mark visited
3. Visit all unvisited neighbors recursively

---

# 🔹 Code (Recursive DFS)

```python id="2x6kqp"
def dfs(graph, node, visited):
    if node not in visited:
        print(node)
        visited.add(node)

        for neighbor in graph[node]:
            dfs(graph, neighbor, visited)
```

---

# 🔹 Graph Example

```python id="5w9mrl"
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

```python id="1h7qav"
visited = set()
dfs(graph, 1, visited)
```

---

## Output

```text id="9d4mcu"
1
2
4
5
3
6
```

---

# 🔹 Dry Run

Start:

```text id="0g5kxr"
dfs(1)
```

Visit:

```text id="4t1vjm"
1
```

Go deeper:

```text id="7q2plf"
2
```

Go deeper:

```text id="3z9knd"
4
```

No children → backtrack

Then:

```text id="8v4xow"
5
```

Backtrack again.

Then:

```text id="2n8wyt"
3
6
```

Done ✅

---

# 🔹 Iterative DFS (Using Stack)

```python id="7f3zma"
def dfs_iterative(graph, start):
    stack = [start]
    visited = set()

    while stack:
        node = stack.pop()

        if node not in visited:
            print(node)
            visited.add(node)

            for neighbor in reversed(graph[node]):
                stack.append(neighbor)
```

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

---

# 🔹 Applications of DFS

---

## 1. Cycle Detection

Detect loops in graph.

---

## 2. Path Finding

Maze problems.

---

## 3. Topological Sorting

Directed graph problems.

---

## 4. Connected Components

Graph clusters.

---

## 5. Backtracking

Sudoku, N-Queens.

---

# 🔹 BFS vs DFS

| Feature   | BFS           | DFS              |
| --------- | ------------- | ---------------- |
| Structure | Queue         | Stack            |
| Traversal | Level-wise    | Depth-wise       |
| Best for  | Shortest path | Deep exploration |

---

# 🔹 Common Interview Questions

* Number of islands
* Cycle detection
* Path exists
* Clone graph

---
