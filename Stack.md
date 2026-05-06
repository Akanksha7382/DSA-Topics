# 📚 Stack 

## 🔹 What is Stack?

A Stack is a linear data structure that follows:

```text id="8nz4q1"
LIFO = Last In First Out
```

👉 Last inserted element comes out first.

---

## 🔹 Real-Life Example

Think of a stack of plates 🍽️

```text id="1bc6zr"
Top
---
Plate 3
Plate 2
Plate 1
---
Bottom
```

👉 Remove from top only.

---

## 🔹 Basic Operations

---

## 1. Push

Add element to top.

```python id="8m6xhv"
stack.append(10)
stack.append(20)
```

Result:

```text id="3vj2qy"
[10, 20]
```

---

## 2. Pop

Remove top element.

```python id="wq2g91"
stack.pop()
```

Result:

```text id="5t6nkp"
[10]
```

---

## 3. Peek / Top

See top element.

```python id="v0hy8u"
stack[-1]
```

---

## 4. Check Empty

```python id="3m8czx"
len(stack) == 0
```

---

## 🔹 Stack Implementation Using List

```python id="e5r7xl"
stack = []

stack.append(10)
stack.append(20)
stack.append(30)

print(stack.pop())
```

---

## Output

```text id="9gw5n2"
30
```

Because stack is LIFO.

---

# 🔹 Time Complexity

| Operation | Complexity |
| --------- | ---------- |
| Push      | O(1)       |
| Pop       | O(1)       |
| Peek      | O(1)       |

---

# 🔹 Applications of Stack

---

## 1. Function Calls / Recursion

Functions are stored in call stack.

---

## 2. Undo / Redo

Text editors use stack.

---

## 3. Parentheses Matching

Example:

```text id="c3v6kb"
() {} []
```

---

## 4. Browser History

Back button uses stack.

---

# 🔹 Parentheses Problem

Example:

```text id="y6t4hp"
( )
```

Push opening bracket:

```python id="9j7nka"
stack.append("(")
```

Pop when closing found.

---

## Example Code

```python id="0fdk8s"
def is_valid(s):
    stack = []

    for ch in s:
        if ch == '(':
            stack.append(ch)
        else:
            if not stack:
                return False
            stack.pop()

    return len(stack) == 0
```

---

# 🔹 Stack Using Linked List

Each node acts like stack element.

Push/Pop at head.

---

# 🔹 Advantages

✔ Fast operations
✔ Simple implementation

---

# 🔹 Disadvantages

❌ Limited access
❌ Only top accessible

---

# 🔹 Common Interview Questions

* Valid Parentheses
* Min Stack
* Next Greater Element
* Reverse string using stack

---

# 🔹 Array vs Stack

| Feature | Array     | Stack    |
| ------- | --------- | -------- |
| Access  | Any index | Top only |
| Order   | Flexible  | LIFO     |

---
