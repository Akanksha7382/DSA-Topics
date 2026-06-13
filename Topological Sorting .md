# 🔥 Topological Sorting 

# 🔹 First Understand the Problem

Suppose you have tasks:

```text
Learn HTML
   ↓
Learn CSS
   ↓
Learn JavaScript
```

Can you learn JavaScript first?

❌ No

Because:

```text
HTML → CSS → JavaScript
```

There is an order.

This is where Topological Sorting is used.

---

# 🔹 What is Topological Sort?

Topological Sort is:

```text
An ordering of nodes
such that every dependency
comes before the dependent node.
```

---

# 🔹 Example

Graph:

```text
A → B → D
↓
C
```

Valid Topological Order:

```text
A B C D
```

or

```text
A C B D
```

Both are correct.

---

# 🔹 Important Condition

Topological Sort works only on:

```text
DAG
```

DAG means:

```text
Directed Acyclic Graph
```

---

## Directed

```text
A → B
```

Direction exists.

---

## Acyclic

No cycle.

Valid:

```text
A → B → C
```

Invalid:

```text
A → B → C → A
```

Cycle ❌

---

# 🔹 Why?

If cycle exists:

```text
A depends on B
B depends on C
C depends on A
```

Impossible to decide order.

---

# 🔹 Real-Life Example

Courses:

```text
DSA → Graphs
```

Need DSA first.

---

# 🔹 Method 1: Kahn's Algorithm (BFS)

Most important 🔥

Uses:

```text
Queue
```

---

# 🔹 Key Concept

Indegree = Number of incoming edges.

Example:

```text
A → B
C → B
```

For B:

```text
indegree = 2
```

---

# 🔹 Rule

Start with nodes having:

```text
indegree = 0
```

Because they have no dependencies.

---

# 🔹 Example

Graph:

```text
A → B
A → C
B → D
C → D
```

---

## Step 1

Indegree:

```text
A = 0
B = 1
C = 1
D = 2
```

Queue:

```text
[A]
```

---

## Step 2

Remove A.

Result:

```text
A
```

Reduce indegree:

```text
B = 0
C = 0
```

Queue:

```text
[B,C]
```

---

## Step 3

Remove B.

Result:

```text
A B
```

Reduce:

```text
D = 1
```

---

## Step 4

Remove C.

Result:

```text
A B C
```

Reduce:

```text
D = 0
```

Queue:

```text
[D]
```

---

## Step 5

Remove D.

Result:

```text
A B C D
```

Done ✅

---

# 🔹 Detect Cycle

Very important interview trick 🔥

After Topological Sort:

If:

```text
processed nodes < total nodes
```

Then:

```text
Cycle exists
```

---

# 🔹 Applications

## Course Schedule

Prerequisites.

---

## Build Systems

Compile dependencies.

---

## Task Scheduling

Order of tasks.

---

## Software Packages

Install dependencies first.

---

# 🔹 Topological Sort vs BFS

| Feature | BFS       | Topological Sort |
| ------- | --------- | ---------------- |
| Graph   | Any       | DAG only         |
| Purpose | Traversal | Ordering         |

---

