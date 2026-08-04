## Tree
- it is a non linear Data structure

## graph

```pythpn
import collections
def dfs(graph,start,visited=None):
    if visited is None:
        visited = set()
    if start not in visited:
        print(str(start)+" ",end="")
    visited.add(start)
    for next in graph[start] - visited:
        dfs(graph,next,visited)
    return visited

def bfs(graph,root):
    visited = set()
    queue = collections.deque([root])
    visited.add(root)
    
    while queue:
        vertex = queue.popleft()
        print(str(vertex)+" ",end="")
        for neighbour in graph[vertex]:
            if neighbour not in visited:
                visited.add(neighbour)
                queue.append(neighbour)
    
graph = {0:set([1,2]),
        1:set([0,3,4]),
        2:set([0]),
        3:set([1]),
        4:set([2,3]),
    }
print("Depth First Search:")
dfs(graph,0)
print()
print("Breadth First Search:")
bfs(graph,0)
```
