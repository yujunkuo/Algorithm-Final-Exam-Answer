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

class GraphVertex:
    def __init__(self, label):
        self.label = label
        self.d = 0  # Distance to start vertex
        self.discovered = False
        self.processed = False
        self.parent = None  # The vertex discovers me 
        self.edges = []  # Edges in Adjacency List
    def __str__(self):
        output = "{0}(d={1}): ".format(self.label, self.d)
        for e in self.edges:
            output += "{0}->{1} ".format(self.label, e.label)
        return output

def DFS(v:GraphVertex): 
    v.discovered = True 
    process_vertex_early(v.label)
    for t in v.edges:
        if not t.discovered:
            t.parent = v
            t.d = v.d + 1 
            process_edge(v.label, t.label)
            DFS(t)
        elif v.parent != t:
            process_edge(v.label, t.label)
    process_vertex_late(v.label)
    v.processed = True

order = []
def process_vertex_late(label:int):
    order.insert(0, label)
    
def process_edge(i:GraphVertex, j:GraphVertex):
    if edge_classification(i, j) == EdgeType.BACK:
        raise Exception("Cycle from %d to %d" % (i.label, j.label))

```

## Q3. Backtracking: Derangement

```python

def construct_candidate(a:list, inputs:list, c:list):
    curr_index = len(a) + 1
    for i in inputs:
        if (i not in a) and (i != curr_index) :
            c.append(i)

```

## Q4. Dynamic Programming: Cutting String

```python


```
