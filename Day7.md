## binary Search Tree
```python
class Node:
    def __init__(self,d):
        self.left=self.right=None
        self.data=d
class Tree:
    def __init__(self):
        self.root=None
    def insert(self, data, node=None):
        if self.root is None:
            self.root = Node(data)
            return self.root
        if node is None:
            node = self.root
        if data < node.data:
            if node.left is None:
                node.left = Node(data)
            else:
                self.insert(data, node.left)
        else:
            if node.right is None:
                node.right = Node(data)
            else:
                self.insert(data, node.right)
        return node
    
    def inorder(self,node):
        if node:
            self.inorder(node.left)
            print(node.data,end=" ")
            self.inorder(node.right)
    def preorder(self,node):
        if node:
            print(node.data,end=" ")
            self.preorder(node.left)
            self.preorder(node.right)
            
    def postorder(self,node):
        if node:
            self.postorder(node.left)
            self.postorder(node.right)
            print(node.data,end=" ")
    def search(self,node,key):
        if node is None:
            return False
        if node.data == key:
            return True
        if node.data<key:
            return self.search(node.left,key)
        else:
            return self.search(node.right,key)
    def height(self,node):
        if node is None:
            return 0
        left = self.height(node.left)
        right = self.height(node.right)
        return max(left,right)+1
    def inorder_successor(self,node):
        cur = node.right
        while cur.left:
            cur=cur.left
        return cur.data
tree = Tree()
tree.insert(8)
tree.insert(3)
tree.insert(1)
tree.insert(6)
tree.insert(7)
tree.insert(10)
tree.insert(14)
tree.insert(4)

print("Inorder: ",tree.inorder(tree.root))
print("Preorder: ",tree.preorder(tree.root))
print("Postorder: ",tree.postorder(tree.root))

print(tree.search(tree.root,10))

print("Height of the tree: ",tree.height(tree.root))
print("inorder Successive of 3: ",tree.inorder_successor(tree.root))
```


## 
```python
class Node:
    def __init__(self,d):
        self.left=self.right=None
        self.data=d
class Tree:
    def __init__(self):
        self.root=None
    def insert(self,node,data):
        if node is None:
            return Node(data)
        if node.data>data:
            node.left = self.insert(node.left,data)
        else:
            node.right = self.insert(node.right,data)
        return node
    
    def inorder(self,node):
        if node:
            self.inorder(node.left)
            print(node.data,end=" ")
            self.inorder(node.right)
    def preorder(self,node):
        if node:
            print(node.data,end=" ")
            self.preorder(node.left)
            self.preorder(node.right)
            
    def postorder(self,node):
        if node:
            self.postorder(node.left)
            self.postorder(node.right)
            print(node.data,end=" ")
    def search(self,node,key):
        if node is None:
            return False
        if node.data == key:
            return True
        if node.data>key:
            return self.search(node.left,key)
        else:
            return self.search(node.right,key)
    def height(self,node):
        if node is None:
            return 0
        left = self.height(node.left)
        right = self.height(node.right)
        return max(left,right)+1
    def inorder_successor(self,node):
        cur = node.right
        while cur.left:
            cur=cur.left
        return cur.data
tree = Tree()
root=None
root=tree.insert(root,8)
root=tree.insert(root,3)
root=tree.insert(root,1)
root=tree.insert(root,6)
root=tree.insert(root,7)
root=tree.insert(root,10)
root=tree.insert(root,14)
root=tree.insert(root,4)
print("Inorder: ",tree.inorder(root))
print("Preorder: ",tree.preorder(root))
print("Postorder: ",tree.postorder(root))
print("Key is Present or Not: ",tree.search(root,10))
print("Height of the tree: ",tree.height(root))
print("inorder Successor: ",tree.inorder_successor(root))
```


## 
```python

```
