# Heap 

## 🔹 What is Heap?

Heap is a special type of binary tree.

Rules:

- It must be a complete binary tree
- It follows heap property

## For Max Heap:

Parent >= Children

For Min Heap:

Parent <= Children

Example:

    50
   /  \
 30   40

Special property:

---

## Max Heap

Parent is always greater than children.

Example:

```text id="6m8qta"
       50
      /  \
    30    40
   / \   /
 10 20 35
```

Rule:

```text id="8w2kpr"
Parent >= Child
```

---

## Min Heap

Parent is always smaller than children.

Example:

```text id="3v7nfa"
       10
      /  \
    20    30
   / \   /
 40 50 60
```

Rule:

```text id="1g4mzc"
Parent <= Child
```

---

# 🔹 Why Heap?

Fast access to:

* maximum element (Max Heap)
* minimum element (Min Heap)

---

# 🔹 Complete Binary Tree

All levels filled except last.

Last level filled left to right.

Valid:

```text id="4x7pql"
    1
   / \
  2   3
 / \
4   5
```

---

Invalid:

```text id="2f9krt"
    1
   / \
  2   3
   \
    5
```

---

# 🔹 Array Representation

Heap stored in array.

Example:

```text id="5h3vna"
[50,30,40,10,20,35]
```

Tree:

```text id="8z1kpm"
       50
      /  \
    30   40
```

---

## Formula

For index `i`:

Left child:

2i+1

Right child:

2i+2

Parent:

\left\lfloor\frac{i-1}{2}\right\rfloor

---

# 🔹 Insertion

Insert at last position.

Then fix heap.

This is called:

```text id="0k8mya"
Heapify Up
```

---

Example:

Insert 60:

```text id="5n7vkp"
50
```

60 > 50

Swap upward.

---

# 🔹 Deletion

Usually delete root.

Steps:

1. Replace root with last element
2. Remove last
3. Fix heap

Called:

```text id="7c3mqt"
Heapify Down
```

---

# 🔹 Python Heap

Python has min heap.

```python id="4d8qvl"
import heapq

heap = []

heapq.heappush(heap, 10)
heapq.heappush(heap, 5)
heapq.heappush(heap, 20)
```

---

Remove min:

```python id="2v9kxp"
heapq.heappop(heap)
```

---

Output:

```text id="1f7mrb"
5
```

---

# 🔹 Time Complexity

Insert:
O(\log n)

Delete:
O(\log n)

Get min/max:
O(1)

---

# 🔹 Applications

---

## 1. Priority Queue

Highest priority first.

---

## 2. CPU Scheduling

Task scheduling.

---

## 3. Dijkstra Algorithm

Shortest path.

---

## 4. Heap Sort

Sorting.

---

## 5. Top K Elements

Top K frequent numbers.

---

# 🔹 Heap Sort

Uses heap for sorting.

Time:

O(n\log n)

---

# 🔹 Advantages

✔ Fast min/max
✔ Efficient priority handling

---

# 🔹 Disadvantages

❌ Searching arbitrary element slow

---

# 🔹 Heap vs BST

| Feature          | Heap | BST      |
| ---------------- | ---- | -------- |
| Access min/max   | Fast | Moderate |
| Sorted traversal | No   | Yes      |


---
