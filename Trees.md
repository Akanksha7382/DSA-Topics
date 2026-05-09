# 🌳 Trees

## 🔹 What is Tree?

A Tree is a hierarchical data structure made of nodes.

Example:

```text id="3m7qvf"
       1
      / \
     2   3
    / \
   4   5
```

---

## 🔹 Important Terms

---

### 1. Root

Top node.

```text id="9v2ncr"
1
```

---

### 2. Parent

Node having child.

Example:

```text id="4k1zpa"
2 is parent of 4,5
```

---

### 3. Child

Node below parent.

Example:

```text id="2g8wlr"
4 is child of 2
```

---

### 4. Leaf Node

Node with no children.

Example:

```text id="7j3mqt"
4,5,3
```

---

### 5. Siblings

Nodes with same parent.

Example:

```text id="1d8fva"
2 and 3
```

---

### 6. Height

Longest path root → leaf.

---

### 7. Depth

Distance from root.

---

# 🔹 Binary Tree

Each node has maximum 2 children.

```text id="8x2lpr"
left, right
```

Example:

```text id="5w7gcm"
    1
   / \
  2   3
```

---

# 🔹 Node Structure

```python id="0z6ktm"
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None
```

---

# 🔹 Creating Tree

```python id="4v1pza"
root = Node(1)
root.left = Node(2)
root.right = Node(3)
```

---

# 🔹 Tree Traversals

Very important 🔥

---

## 1. Inorder

```text id="5t4xzr"
Left → Root → Right
```

Example output:

```text id="8q7pln"
4 2 5 1 3
```

Code:

```python id="7k3vmb"
def inorder(root):
    if root:
        inorder(root.left)
        print(root.data)
        inorder(root.right)
```

---

## 2. Preorder

```text id="6p8qwa"
Root → Left → Right
```

Output:

```text id="1w9zmc"
1 2 4 5 3
```

Code:

```python id="2h7xkn"
def preorder(root):
    if root:
        print(root.data)
        preorder(root.left)
        preorder(root.right)
```

---

## 3. Postorder

```text id="9r4kxu"
Left → Right → Root
```

Output:

```text id="3g8vpm"
4 5 2 3 1
```

Code:

```python id="0n2tqj"
def postorder(root):
    if root:
        postorder(root.left)
        postorder(root.right)
        print(root.data)
```

---

# 🔹 Level Order Traversal

Uses BFS.

Output:

```text id="7f1kzr"
1 2 3 4 5
```

---

# 🔹 Time Complexity

Traversal:

O(n)

Visit every node once.

---

# 🔹 Space Complexity

Recursive stack:

O(h)

h = height

---

# 🔹 Types of Trees

* Binary Tree
* Binary Search Tree
* AVL Tree
* Heap
* Trie

---

# 🔹 Applications

---

## 1. File Systems

Folders and subfolders.

---

## 2. Database Indexing

Fast search.

---

## 3. Expression Trees

Math expressions.

---

## 4. Decision Trees

Machine learning.

---
