# 🌳 Binary Search Tree (BST) 

## 🔹 What is BST?

BST is a Binary Tree with special rules:

### Rule:

```text id="3z8kpa"
Left subtree < Root < Right subtree
```

Meaning:

* Left child values are smaller
* Right child values are greater

---

## 🔹 Example

```text id="7m2vqa"
       10
      /  \
     5   15
    / \    \
   2   7   20
```

Check:

* Left of 10 → smaller ✅
* Right of 10 → greater ✅

---

# 🔹 Why BST?

Because searching becomes efficient.

Instead of checking every node:

* go left if smaller
* go right if larger

Just like Binary Search.

---

# 🔹 Node Structure

```python id="8f3krt"
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None
```

---

# 🔹 Searching in BST

---

## Logic

Example search 7:

```text id="6q1vzm"
Start at 10
7 < 10 → go left
At 5
7 > 5 → go right
Found 7
```

---

## Code

```python id="1v7kqa"
def search(root, key):
    if root is None or root.data == key:
        return root

    if key < root.data:
        return search(root.left, key)

    return search(root.right, key)
```

---

# 🔹 Insert in BST

Insert:

```text id="2m8wfa"
8
```

Traversal:

```text id="4p3kxu"
8 < 10 → left
8 > 5 → right
8 > 7 → right
```

Insert there.

---

## Code

```python id="5n4vtr"
def insert(root, key):
    if root is None:
        return Node(key)

    if key < root.data:
        root.left = insert(root.left, key)
    else:
        root.right = insert(root.right, key)

    return root
```

---

# 🔹 Delete in BST

Harder operation 🔥

Cases:

---

## 1. Node has no child

Delete directly.

---

## 2. Node has one child

Replace with child.

---

## 3. Node has two children

Replace with inorder successor.

---

# 🔹 Inorder Traversal in BST

Very important:

```text id="9k6vpd"
Inorder of BST gives sorted order
```

---

Example:

```text id="0f3mza"
2 5 7 10 15 20
```

---

# 🔹 Time Complexity

Balanced BST:

Search:
O(\log n)

Insert:
O(\log n)

Delete:
O(\log n)

---

Worst case (skewed tree):

O(n)

---

Example skewed:

```text id="8v1kpl"
1
 \
  2
   \
    3
```

Behaves like linked list.

---

# 🔹 Advantages

✔ Fast search
✔ Sorted data
✔ Efficient insertion/deletion

---

# 🔹 Disadvantages

❌ Can become unbalanced

---

# 🔹 Applications

* Database indexing
* Searching systems
* Dictionaries

---

# 🔹 BST vs Binary Tree

| Feature  | Binary Tree | BST      |
| -------- | ----------- | -------- |
| Ordering | No rule     | Ordered  |
| Search   | O(n)        | O(log n) |

---
