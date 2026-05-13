# 🕸️ Graph

## 🔹 What is Graph?

A Graph is a collection of:

* Vertices (nodes)
* Edges (connections)

---

## Example

```text id="7k2vpr"
A ---- B
|      |
C ---- D
```

---

## Terms:

* A, B, C, D = vertices
* lines = edges

---

# 🔹 Why Graph?

Used to represent relationships.

Examples:

* Cities connected by roads
* Friends in social media

---

# 🔹 Types of Graph

---

## 1. Undirected Graph

Connection both ways.

```text id="4z8mqt"
A -- B
```

Means:

* A connected to B
* B connected to A

---

## 2. Directed Graph

Connection one way.

```text id="5x1kpa"
A → B
```

Only A to B.

---

## 3. Weighted Graph

Edges have weights.

Example:

```text id="9m3vzc"
A --5-- B
```

Weight = 5

---

## 4. Unweighted Graph

No weights.

---

## 5. Cyclic Graph

Contains cycle.

```text id="3t7qpl"
A → B → C → A
```

---

## 6. Acyclic Graph

No cycle.

---

# 🔹 Graph Representation

Very important 🔥

---

## 1. Adjacency Matrix

2D array.

Example:

```python id="7n2xwr"
graph = [
 [0,1,1],
 [1,0,1],
 [1,1,0]
]
```

---

## 2. Adjacency List

Most common.

```python id="1m8kqa"
graph = {
    1: [2,3],
    2: [1,4],
    3: [1],
    4: [2]
}
```

---

# 🔹 BFS in Graph

Uses queue.

Traversal:

* level by level


---

# 🔹 DFS in Graph

Uses recursion/stack.

Traversal:

* go deep first


---

# 🔹 Degree

Number of edges connected.

Example:

```text id="2g9mvl"
A connected to 2 nodes
degree = 2
```

---

# 🔹 Path

Sequence of vertices.

Example:

```text id="6v3qta"
A → B → D
```

---

# 🔹 Cycle

Loop exists.

Example:

```text id="8k5xpr"
A → B → C → A
```

---

# 🔹 Connected Graph

All nodes reachable.

---

# 🔹 Disconnected Graph

Some nodes isolated.

---

# 🔹 Time Complexity

Adjacency list traversal:

O(V+E)

Where:

* V = vertices
* E = edges

---

# 🔹 Applications

---

## 1. Google Maps

Shortest route.

---

## 2. Social Media

Friend suggestions.

---

## 3. Computer Networks

Routing.

---

## 4. Recommendation Systems

Netflix, YouTube.

---

## 5. Web Crawlers

Internet page links.

---

# 🔹 Common Graph Algorithms

* BFS
* DFS
* Dijkstra
* Bellman Ford
* Floyd Warshall
* Kruskal
* Prim

---

# 🔹 Common Interview Questions

* Number of islands
* Detect cycle
* Clone graph
* Course schedule

---

# 🔹 Graph vs Tree

| Feature | Tree | Graph         |
| ------- | ---- | ------------- |
| Cycle   | No   | Can exist     |
| Root    | Yes  | Not necessary |

---
