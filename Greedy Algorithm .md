# 🔥 Greedy Algorithm 

## 🔹 What is Greedy Algorithm?

Greedy algorithm makes the best choice at each step.

```text id="8m2kpa"
Take best option now
```

without worrying too much about future.

---

## Main Idea

```text id="3v7qzt"
Local optimum → Global optimum
```

---

## Real Life Example

Coin selection:

Need:

```text id="7k1mpr"
₹27
```

Coins:

```text id="5n8vxa"
10, 5, 2, 1
```

Greedy picks:

```text id="1p4klt"
10 + 10 + 5 + 2
```

Fast answer.

---

# 🔹 When Greedy Works?

Problem should have:

---

## 1. Greedy Choice Property

Best local choice leads to best solution.

---

## 2. Optimal Substructure

Optimal solution built from smaller solutions.

---

# 🔹 Example 1: Activity Selection

Choose max non-overlapping activities.

Activities:

```text id="2m9qwr"
(1,3), (2,4), (3,5)
```

Rule:

👉 Choose activity with earliest finish time.

---

## Code

```python id="4x7kpm"
activities.sort(key=lambda x: x[1])

count = 1
end = activities[0][1]

for i in range(1, len(activities)):
    if activities[i][0] >= end:
        count += 1
        end = activities[i][1]
```

---

# 🔹 Example 2: Minimum Coins

Coins:

```python id="1v8qza"
coins = [10,5,2,1]
amount = 27
```

Pick largest possible first.

---

Code:

```python id="9t2mkr"
count = 0

for coin in coins:
    while amount >= coin:
        amount -= coin
        count += 1
```

---

# 🔹 Example 3: Fractional Knapsack

Take item with highest:

```text id="8p5vlt"
value / weight
```

first.

---

# 🔹 Why Called Greedy?

Because algorithm is “greedy” 😄

```text id="7g3kpa"
Take best available immediately
```

---

# 🔹 Time Complexity

Usually depends on sorting.

Common:

O(n\log n)

---

# 🔹 Advantages

✔ Fast
✔ Simple
✔ Efficient

---

# 🔹 Disadvantages

❌ Doesn’t always work
❌ Can miss optimal solution

---

# 🔹 Where Greedy Fails

Example:

Coins:

```text id="4w9mqt"
4,3,1
```

Need:

```text id="6f1xpa"
6
```

Greedy:

```text id="0z8krl"
4+1+1 = 3 coins
```

Optimal:

```text id="7h2vzc"
3+3 = 2 coins
```
Greedy fails ❌

---

# 🔹 Common Greedy Problems

* Activity selection
* Fractional knapsack
* Huffman coding
* Job scheduling
* Minimum platforms

---

# 🔹 Greedy vs DP

| Feature  | Greedy    | DP           |
| -------- | --------- | ------------ |
| Decision | Immediate | Future-aware |
| Speed    | Faster    | Slower       |

---
