# 🔥 Backtracking 

## 🔹 What is Backtracking?

Backtracking is:

```text id="8p2vma"
Try → Check → Undo
```

Try all possible choices.

If choice is wrong:

* undo it
* try another path

---

## Main Idea

```text id="5k7qtr"
Explore all possibilities
```

---

## Real-Life Example

Maze 🧩

You choose one path.

If dead end:

* go back
* try another path

That is backtracking.

---

# 🔹 Core Steps

1. Choose
2. Explore
3. Undo

---

## Formula

```text id="7v1kpa"
Make choice
Recurse
Backtrack
```

---

# 🔹 Generic Code Template

```python id="2m8qzt"
def backtrack(path, choices):
    if goal_reached:
        result.append(path[:])
        return

    for choice in choices:
        path.append(choice)      # choose
        backtrack(path, choices) # explore
        path.pop()               # undo
```

---

# 🔹 Example 1: Generate Subsets

Input:

```python id="9k4vpr"
nums = [1,2]
```

Output:

```text id="4g7xma"
[]
[1]
[2]
[1,2]
```

---

## Code

```python id="3t8kql"
result = []

def subsets(nums, path, index):
    result.append(path[:])

    for i in range(index, len(nums)):
        path.append(nums[i])
        subsets(nums, path, i+1)
        path.pop()
```

Call:

```python id="6p1mza"
subsets([1,2], [], 0)
```

---

# 🔹 Dry Run

Start:

```text id="0x7kpr"
[]
```

Choose 1:

```text id="8w2mqa"
[1]
```

Choose 2:

```text id="1n5vlt"
[1,2]
```

Undo:

```text id="7m9qwr"
[1]
```

Undo again:

```text id="4k3xpa"
[]
```

Choose 2:

```text id="2v8mzc"
[2]
```

Done.

---

# 🔹 Example 2: Permutations

Input:

```text id="9f1krt"
[1,2,3]
```

Output:

```text id="6q4vpa"
[1,2,3]
[1,3,2]
[2,1,3]
...
```

Try all arrangements.

---

# 🔹 Example 3: N-Queens

Place queens safely.

Rules:

* no same row
* no same column
* no diagonal

Classic backtracking problem 🔥

---

# 🔹 Example 4: Sudoku Solver

Try number.

If invalid:

* remove
* try next number

---

# 🔹 Time Complexity

Usually exponential.

Common:

O(2^n)

or worse depending on problem.

---

# 🔹 Space Complexity

Depends on recursion depth.

Usually:

O(n)

---

# 🔹 Why Important?

Useful when:

* brute force needed
* constraints checking required

---

# 🔹 Common Backtracking Problems

* Subsets
* Permutations
* Combination sum
* Sudoku
* N Queens
* Word search

---

# 🔹 Backtracking vs Recursion

| Feature | Recursion  | Backtracking   |
| ------- | ---------- | -------------- |
| Purpose | Repetition | Explore + undo |

---

# 🔹 Key Operation

Most important line:

```python id="8r2mxt"
path.pop()
```

Undo choice.

This is the heart of backtracking.

---

# 🔹 Interview Tip

Say:

* “Backtracking = try and undo”

---

# 🔹 Quick Summary

* Choose
* Explore
* Undo

---
