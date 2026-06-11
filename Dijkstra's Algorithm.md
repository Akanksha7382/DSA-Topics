# 🚗 Dijkstra's Algorithm 
# 🔹 First Understand the Problem

Suppose we have cities:

```text id="1"
A ----5---- B
|           |
2           1
|           |
C ----3---- D
```

Numbers represent distance.

Question:

```text id="2"
Shortest distance from A to D?
```

Possible paths:

```text id="3"
A → B → D = 5 + 1 = 6

A → C → D = 2 + 3 = 5
```

Answer:

```text id="4"
A → C → D
Distance = 5
```

---

# 🔹 What is Dijkstra?

Dijkstra finds:

```text id="5"
Shortest path from one source node
to all other nodes
```

---

# 🔹 Main Idea

Always choose the node with:

```text id="6"
Smallest known distance
```

and expand from there.

---

# 🔹 Real-Life Example

Google Maps:


---

# 🔹 Data Structure Used

👉 Priority Queue (Min Heap)

Why?

Need the node with minimum distance quickly.

---

# 🔹 Example Graph

```text id="10"
      A
     / \
    4   1
   /     \
  B---2---C
       \
        5
         \
          D
```

---

# 🔹 Step 1

Source:

```text id="11"
A
```

Distance table:

```text id="12"
A = 0
B = ∞
C = ∞
D = ∞
```

---

# 🔹 Step 2

Visit A.

Neighbors:

```text id="13"
B = 4
C = 1
```

Update:

```text id="14"
A = 0
B = 4
C = 1
D = ∞
```

---

# 🔹 Step 3

Choose smallest distance.

```text id="15"
C = 1
```

Visit C.

Path to D:

```text id="16"
1 + 5 = 6
```

Update:

```text id="17"
D = 6
```

Path to B:

```text id="18"
1 + 2 = 3
```

Better than 4.

Update:

```text id="19"
B = 3
```

---

# 🔹 Final Distances

```text id="20"
A = 0
B = 3
C = 1
D = 6
```

---

# 🔹 Algorithm

1. Set source distance = 0
2. Others = infinity
3. Put source into min heap
4. Take smallest distance node
5. Update neighbors
6. Repeat

---

# 🔹 Python Code

```python id="21"
import heapq

def dijkstra(graph, start):
    dist = {node: float('inf') for node in graph}
    dist[start] = 0

    pq = [(0, start)]

    while pq:
        current_dist, node = heapq.heappop(pq)

        for neighbor, weight in graph[node]:
            new_dist = current_dist + weight

            if new_dist < dist[neighbor]:
                dist[neighbor] = new_dist
                heapq.heappush(
                    pq,
                    (new_dist, neighbor)
                )

    return dist
```

---

# 🔹 Graph Input

```python id="22"
graph = {
 'A':[('B',4),('C',1)],
 'B':[('D',1)],
 'C':[('B',2),('D',5)],
 'D':[]
}
```

---

# 🔹 Time Complexity

Using Min Heap:

O((V+E)\log V)

Where:

* V = Vertices
* E = Edges

---

# 🔹 Space Complexity

O(V)

---

# 🔹 Important Limitation

Dijkstra does NOT work correctly with:

```text id="23"
Negative edge weights
```

Example:

```text id="24"
A → B = -5
```

For negative weights use:

```text id="25"
Bellman-Ford Algorithm
```

---

# 🔹 Applications

## Google Maps

Shortest routes.

---

## Network Routing

Internet packets.

---

## Flight Planning

Lowest travel cost.

---

## Delivery Apps

Fastest route.

---

# 🔹 Dijkstra vs BFS

| Feature       | BFS        | Dijkstra |
| ------------- | ---------- | -------- |
| Graph Type    | Unweighted | Weighted |
| Structure     | Queue      | Min Heap |
| Shortest Path | Yes        | Yes      |

---
