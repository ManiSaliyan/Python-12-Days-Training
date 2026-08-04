## Tree
- it is a non linear Data structure .collection of nodes connected with edges in a hierchial manner

## graph
- it is a non linear Data structure .collection of vertices connected with edges.
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
## Invert Binary Tree
```python

# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def invertTree(self, root: Optional[TreeNode]) -> Optional[TreeNode]:
        if root is None:
            return root
        root.left,root.right = root.right,root.left
        self.invertTree(root.left)
        self.invertTree(root.right)
        return root
```
