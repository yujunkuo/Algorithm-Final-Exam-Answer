# Code 

## Q1. Divide and Conquer: Missing Number
    - Time Complexity: O(logN)

```python
def search_missing(arr, size): 
    i = 0
    j = size - 1
    mid = 0
    while j > i + 1: 
        mid = (i + j) // 2
        if (arr[i] - i) != (arr[mid] - mid): 
            j = mid 
        else:
            i = mid
    return arr[mid] + 1

```

## Q2. Graph: Topological Sort

```python


```

## Q3. Backtracking: Derangement

```python


```

## Q4. Dynamic Programming: Cutting String

```python


```
