# 🔥 Union Find (Disjoint Set Union - DSU)

# 🔹 First Understand the Problem

Suppose we have:

```text id="1"
1   2   3   4   5
```

Initially, everyone is separate.

```text id="2"
{1} {2} {3} {4} {5}
```

These are called sets.

---

# 🔹 What is Union Find?

Union Find is a data structure that helps us:

1. Find which set an element belongs to
2. Merge two sets efficiently

---

# 🔹 Real-Life Example

Think of social groups.

Initially:

```text id="3"
A   B   C   D
```

Everyone is alone.

Now:

```text id="4"
Union(A,B)
```

Groups become:

```text id="5"
[A,B]   [C]   [D]
```

Then:

```text id="6"
Union(C,D)
```

Groups become:

```text id="7"
[A,B]   [C,D]
```

---

# 🔹 Two Important Operations

---

## 1. Find(x)

Finds the parent (leader) of x.

Example:

```text id="8"
1 → 2 → 3
```

Leader is:

```text id="9"
3
```

So:

```text id="10"
find(1) = 3
```

---

## 2. Union(x,y)

Merge two groups.

Example:

Before:

```text id="11"
{1,2}
{3,4}
```

After:

```text id="12"
union(2,3)
```

Result:

```text id="13"
{1,2,3,4}
```

---

# 🔹 Basic Representation

Using parent array:

```python id="14"
parent = [0,1,2,3,4]
```

Meaning:

```text id="15"
0 is parent of 0
1 is parent of 1
2 is parent of 2
...
```

Everyone is their own leader.

---

# 🔹 Find Function

```python id="16"
def find(x):
    if parent[x] == x:
        return x

    return find(parent[x])
```

---

# 🔹 Union Function

```python id="17"
def union(x, y):
    px = find(x)
    py = find(y)

    parent[px] = py
```

---

# 🔹 Example

Initial:

```text id="18"
1 2 3 4
```

Parent:

```text id="19"
1 2 3 4
```

---

Union(1,2)

```text id="20"
1 → 2
```

---

Union(2,3)

```text id="21"
1 → 2 → 3
```

---

Find(1)

```text id="22"
1 → 2 → 3
```

Answer:

```text id="23"
3
```

---

# 🔹 Problem with Basic DSU

Suppose:

```text id="24"
1 → 2 → 3 → 4 → 5
```

Finding 1 requires many steps.

Slow ❌

---

# 🔹 Path Compression

Big optimization 🔥

Before:

```text id="25"
1 → 2 → 3 → 4 → 5
```

After find(1):

```text id="26"
1
 \
  5
2/
3/
4/
```

Everyone points directly to root.

Fast ✅

---

# 🔹 Path Compression Code

```python id="27"
def find(x):
    if parent[x] != x:
        parent[x] = find(parent[x])

    return parent[x]
```

---

# 🔹 Union by Rank

Another optimization.

Always attach smaller tree under bigger tree.

This keeps tree short.

---

# 🔹 Time Complexity

Without optimization:

```text id="28"
O(n)
```

---

With Path Compression + Rank:

Almost constant time 🚀

```text id="29"
O(α(n))
```

(alpha)

Practically:

```text id="30"
≈ O(1)
```

---

# 🔹 Applications

---

## 1. Detect Cycle in Graph

Very common.

If two nodes already belong to same set:

```text id="31"
Cycle exists
```

---

## 2. Kruskal Algorithm

Minimum Spanning Tree.

Uses DSU heavily.

---

## 3. Network Connectivity

Check if two computers belong to same network.

---

## 4. Friend Groups

Social network problems.

---

# 🔹 Example Interview Question

Given:

```text id="32"
Edges:
1-2
2-3
3-1
```

Cycle?

Process:

```text id="33"
Union(1,2)
Union(2,3)
```

Now:

```text id="34"
1 and 3 already connected
```

Adding:

```text id="35"
3-1
```

Creates cycle ✅

---

# 🔹 Interview Tip

Remember:

```text id="36"
Find → find parent
Union → merge sets
```

---

# 🔹 Quick Summary

* DSU manages groups
* Find identifies group leader
* Union merges groups
* Path Compression makes it very fast
* Used in graphs and cycle detection

---
