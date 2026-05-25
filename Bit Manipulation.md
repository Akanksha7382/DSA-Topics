# ⚡ Bit Manipulation 

# 🔹 First Understand Binary Numbers

Computers store everything in binary.

Binary uses only:

```text id="7m2xqa"
0 and 1
```

---

# 🔹 Decimal to Binary

Example:

```text id="5p8mvr"
5
```

Binary:

```text id="1k4xzt"
101
```

Meaning:

```text id="8v3qpa"
1×2² + 0×2¹ + 1×2⁰
= 4 + 0 + 1
= 5
```

---

# 🔹 Another Example

```text id="6n1mqa"
10
```

Binary:

```text id="9q7xpl"
1010
```

---

# 🔹 Why Bit Manipulation?

Operations on bits are VERY fast ⚡

Instead of complicated calculations:

* directly manipulate bits

---

# 🔹 Main Bit Operators

| Operator | Name        |    |
| -------- | ----------- | -- |
| `&`      | AND         |    |
| `        | `           | OR |
| `^`      | XOR         |    |
| `~`      | NOT         |    |
| `<<`     | Left Shift  |    |
| `>>`     | Right Shift |    |

---

# 🔹 1. AND Operator (&)

Rule:

```text id="4t8mvr"
1 & 1 = 1
Otherwise 0
```

---

## Example

```text id="5v2kpa"
5 & 3
```

Binary:

```text id="8m1qzr"
5 = 101
3 = 011
```

Result:

```text id="0p7xma"
001
```

Answer:

```text id="2k4vlt"
1
```

---

# 🔹 Use of AND

Check even/odd.

---

## Trick

```python id="7n3qkr"
n & 1
```

If result:

* 0 → even
* 1 → odd

---

## Example

```text id="4m9xpa"
6 = 110
```

```text id="1v8kzt"
110 & 001 = 0
```

Even ✅

---

# 🔹 2. OR Operator (|)

Rule:

```text id="6p2mvr"
Any 1 gives 1
```

---

## Example

```text id="5q7xka"
5 | 3
```

Binary:

```text id="9m1vpa"
101
011
---
111
```

Answer:

```text id="2t8qzl"
7
```

---

# 🔹 3. XOR Operator (^)

Very important 🔥

Rule:

```text id="7v3mkt"
Same bits → 0
Different bits → 1
```

---

## Example

```text id="4n1xqa"
5 ^ 3
```

Binary:

```text id="6k8mvr"
101
011
---
110
```

Answer:

```text id="1q4xzt"
6
```

---

# 🔹 Amazing XOR Properties

---

## Property 1

```text id="8m2qpa"
a ^ a = 0
```

---

## Property 2

```text id="5v7xkr"
a ^ 0 = a
```

---

# 🔹 Famous XOR Question

Find single number.

Array:

```text id="0n8mzt"
[2,2,1]
```

All duplicates cancel.

```text id="2p4xva"
2 ^ 2 ^ 1
= 0 ^ 1
= 1
```

---

# 🔹 4. Left Shift (<<)

Moves bits left.

Example:

```text id="9m3qkt"
5 << 1
```

Binary:

```text id="4v7xpa"
101 → 1010
```

Answer:

```text id="7k1mzr"
10
```

---

## Important Rule

n<<1 = n\times2

---

# 🔹 5. Right Shift (>>)

Moves bits right.

Example:

```text id="3t8qvl"
10 >> 1
```

Binary:

```text id="6m2xpa"
1010 → 0101
```

Answer:

```text id="1p9kzr"
5
```

---

## Important Rule

n>>1 = \lfloor n/2 \rfloor

---

# 🔹 Check Power of 2

Very famous interview trick 🔥

Condition:

```python id="5x7mqa"
n & (n-1) == 0
```

---

## Example

```text id="8v2qkt"
8 = 1000
7 = 0111
```

AND:

```text id="2k5xpa"
0000
```

Power of 2 ✅

---

# 🔹 Set Bit

Turn bit ON.

```python id="7m4qzr"
n | (1 << i)
```

---

# 🔹 Clear Bit

Turn bit OFF.

```python id="1v8mkt"
n & ~(1 << i)
```

---

# 🔹 Toggle Bit

Reverse bit.

```python id="4q2xpa"
n ^ (1 << i)
```

---

# 🔹 Applications

* Competitive programming
* Cryptography
* Memory optimization
* Graphics systems

---

# 🔹 Time Complexity

Most bit operations:

O(1)

Very fast ⚡

---

# 🔹 Interview Tip

Say:

* “XOR cancels duplicates”

---

# 🔹 Final Quick Summary

* Binary operations
* Very fast
* XOR most important

---
