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
## Queue
```python
class Queue:
    def __init__(self,k):
        self.k = k
        self.queue = [None]*k
        self.front=self.rear=-1
    def enqueue(self,data):
        if self.front==self.k-1:
            print("Queue is Full")
            return
        elif self.front ==-1:
            self.front=self.rear=0
            self.queue[self.rear] = data
        else:
            self.rear+=1
            self.queue[self.rear] = data
        print(f"Inserted {self.queue[self.rear]}")
    def dequeue(self):
        if self.rear==-1:
            print("Empty List")
        elif self.front==self.rear:
            temp=self.queue[self.front]
            self.front+=1
            print(f"Deleted {temp}")
        else:
            temp=self.queue[self.front]
            self.front+=1
            print(f"Deleted {temp}")
    def traverse(self):
        if self.rear==-1:
            print("Empty List")
        else:
            for i in range(self.front,self.rear+1):
                print(self.queue[i])

queue = Queue(4)
queue.enqueue(1)
queue.enqueue(2)
queue.enqueue(3)
queue.enqueue(4)
queue.traverse()
queue.dequeue()
queue.traverse()
        
```
##
```python

```







##
```python

```
