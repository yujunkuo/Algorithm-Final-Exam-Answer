# Code 

## Q1. Divide and Conquer: Missing Number

```python
def search(ar, size): 
    i = 0
    j = size - 1
    mid = 0
    while j > i + 1: 
        mid = (i + j) // 2
        if (ar[i] - i) != (ar[mid] - mid): 
            j = mid 
        # elif (ar[j] - j) != (ar[mid] - mid): 
        #     i = mid 
        else:
            i = mid
    return ar[mid] + 1

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
