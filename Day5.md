## Basic Stack
```python
def create_stack():
    stack=[]
    return stack

def push(stack,val):
    stack.append(val)
    print(f"Inserted {val}")
def is_empty(stack):
    return len(stack)==0
def pop(stack):
    if is_empty(stack):
        print("Empty Stack")
    else:
        val=stack.pop()
        print(f"Deleted {val}")
    
stack = create_stack()
push(stack,1)
push(stack,2)
push(stack,3)
push(stack,4)
print("Stack Elements Before Pop: ",str(stack))
pop(stack)
print("Stack Elements After Pop: ",str(stack))

```

## stack using Linked List
```python
class Node:
    def __init__(self,data):
        self.val = data
        self.next = None
class Stack:
    def __init__(self):
        self.head=None
    def push(self,data):
        newNode = Node(data)
        if self.head==None:
            self.head=newNode
        else:
            newNode.next=self.head
            self.head=newNode
        print(f"Inserted {newNode.val}")
    def pop(self):
        if self.head==None:
            print("Empty List")
        else:
            print(f"Deleted {self.head.val}")
            self.head=self.head.next
    def traverse(self):
        cur = self.head
        while cur:
            print(cur.val,end="->")
            cur = cur.next
        print()

stack = Stack()
stack.push(1)
stack.push(2)
stack.push(3)
stack.push(4)
stack.traverse()
stack.pop()
stack.traverse()
```






##
```python

```
