# 🚶 Queue

## 🔹 What is Queue?

A Queue is a linear data structure that follows:

```text id="5k3tq1"
FIFO = First In First Out
```

👉 First inserted element is removed first.

---

## 🔹 Real-Life Example

Think of people standing in a queue 🚶

```text id="z8v1ac"
Front → [10, 20, 30] ← Rear
```

* 10 entered first
* 10 leaves first

---

# 🔹 Basic Operations

---

## 1. Enqueue

Add element at rear.

```python id="6d8qph"
queue.append(10)
queue.append(20)
```

Result:

```text id="q5v7ma"
[10, 20]
```

---

## 2. Dequeue

Remove element from front.

```python id="2t8hgn"
queue.pop(0)
```

Result:

```text id="1k7bmr"
[20]
```

---

## 3. Front

Get first element.

```python id="4n2xwy"
queue[0]
```

---

## 4. Rear

Get last element.

```python id="v7c1ed"
queue[-1]
```

---

# 🔹 Queue Implementation Using List

```python id="h4m8zt"
queue = []

queue.append(10)
queue.append(20)
queue.append(30)

print(queue.pop(0))
```

---

## Output

```text id="7r3kfa"
10
```

Because Queue is FIFO.

---

# 🔹 Better Queue in Python

Using `deque`

```python id="k8p2dw"
from collections import deque

queue = deque()

queue.append(10)
queue.append(20)

queue.popleft()
```

👉 Faster than list.

---

# 🔹 Time Complexity

| Operation | Complexity |
| --------- | ---------- |
| Enqueue   | O(1)       |
| Dequeue   | O(1)       |
| Front     | O(1)       |

---

# 🔹 Types of Queue

---

## 1. Simple Queue

Normal FIFO queue.

---

## 2. Circular Queue

Last position connects to first.

---

## 3. Priority Queue

Higher priority element removed first.

---

## 4. Deque

Insertion/deletion from both ends.

---

# 🔹 Applications of Queue

---

## 1. CPU Scheduling

Tasks processed in order.

---

## 2. Printer Queue

Documents printed one by one.

---

## 3. BFS Traversal

Graphs/Trees use queue.

---

## 4. Call Center Systems

First caller handled first.

---

# 🔹 Stack vs Queue

| Feature   | Stack | Queue |
| --------- | ----- | ----- |
| Principle | LIFO  | FIFO  |
| Insert    | Top   | Rear  |
| Remove    | Top   | Front |

---

# 🔹 Circular Queue

After last position:

```text id="6g3tpo"
rear → front
```

Helps reuse empty space.

---

# 🔹 Priority Queue

Example:

```text id="8h9kpl"
VIP customer served first
```

Priority matters more than insertion order.

---

# 🔹 Deque

Double-ended queue.

```python id="t1q4rz"
dq.appendleft(10)
dq.append(20)
```

---

# 🔹 Common Interview Questions

* Implement Queue using Stack
* Implement Stack using Queue
* Circular Queue
* Generate Binary Numbers

---

# 🔹 Advantages

✔ Fast insertion/deletion
✔ Useful for scheduling

---

# 🔹 Disadvantages

❌ No random access
❌ Front-only deletion

---

