# 🔥 Dynamic Programming (DP)

## 🔹 What is Dynamic Programming?

Dynamic Programming is an optimization technique.

It solves problems by:

1. Breaking problem into smaller subproblems
2. Solving once
3. Storing results for reuse

---

## Main Idea

```text id="8q3mzt"
Don't solve same problem again and again
```

Store answer and reuse it.

---

# 🔹 Why DP?

Without DP:

Recursive problems repeat work.

Example:

Fibonacci:

```python id="4v8kpa"
fib(5)
```

Calls:

```text id="1m7qwr"
fib(4), fib(3)
```

Then:

```text id="7k2xpl"
fib(3) again
fib(2) again
```

Repeated work ❌

---

# 🔹 Example Without DP

```python id="3z6mqt"
def fib(n):
    if n <= 1:
        return n
    return fib(n-1) + fib(n-2)
```

---

## Problem

Too many repeated calls.

Time:

O(2^n)

Very slow.

---

# 🔹 Solution: DP

Store computed values.

---

## Memoization (Top Down)

Recursion + memory.

```python id="2k9vra"
def fib(n, dp={}):
    if n in dp:
        return dp[n]

    if n <= 1:
        return n

    dp[n] = fib(n-1, dp) + fib(n-2, dp)
    return dp[n]
```

---

## Time Complexity

O(n)

Huge improvement 🚀

---

# 🔹 Tabulation (Bottom Up)

Build from smaller values.

```python id="6t4xkp"
def fib(n):
    dp = [0,1]

    for i in range(2, n+1):
        dp.append(dp[i-1] + dp[i-2])

    return dp[n]
```

---

## Build Like:

```text id="5p8mqa"
fib(0)=0
fib(1)=1
fib(2)=1
fib(3)=2
fib(4)=3
```

---

# 🔹 Two Types of DP

---

## 1. Memoization

```text id="9v3kpl"
Top Down
```

* recursion
* cache results

---

## 2. Tabulation

```text id="7n1qwr"
Bottom Up
```

* iterative
* table building

---

# 🔹 When to Use DP?

Problem has:

---

## 1. Overlapping Subproblems

Same subproblem repeats.

Example:

```text id="1k4xpa"
fib(3) called multiple times
```

---

## 2. Optimal Substructure

Optimal solution built from smaller solutions.

---

# 🔹 Common DP Problems

Very famous 🔥

* Fibonacci
* Climbing stairs
* Knapsack
* Coin change
* Longest common subsequence
* House robber

---

# 🔹 Climbing Stairs Example

Can climb:

* 1 step
* 2 steps

Question:
Ways to reach n stairs.

Formula:

```text id="6m9qzt"
dp[n] = dp[n-1] + dp[n-2]
```

---

# 🔹 Space Optimization

Instead of array:

```python id="4g2vkl"
a, b = 0, 1

for _ in range(n):
    a, b = b, a+b
```

---

## Space:

O(1)

---

# 🔹 Time Complexity

Usually:

O(n)

Depends on problem.

---

# 🔹 Advantages

✔ Faster than recursion
✔ Avoid repeated work

---

# 🔹 Disadvantages

❌ Hard to identify at first

---


