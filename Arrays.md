# ✅ What is an Array?

- 👉 An array is a collection of elements stored in continuous memory locations

arr = [10, 20, 30, 40]
Index starts from 0
arr[0] = 10, arr[1] = 20 


##  Key Properties
- Same data type (usually)
- Fixed order 
- Fast access using index

## Basic Operations
1. Access Element → O(1)
```print(arr[2]) ``` # 30

2. Traverse Array → O(n)
```
for i in arr:
    print(i)
```

3. Insert Element → O(n)
```arr.insert(1, 15)```

4. Delete Element → O(n)
```arr.remove(20)```
