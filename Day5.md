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
## Queue Using Linked List
```python
class Node:
    def __init__(self,data):
        self.data = data
        self.next = None

class Queue:
    def __init__(self):
        self.front=self.rear=None
    def enqueue(self,data):
        nn = Node(data)
        if self.front == self.rear == None:
            self.front=self.rear=nn
        else:
            self.rear.next = nn
            self.rear=nn
        print(f"Inserted {nn.data}")
    def dequeue(self):
        if self.front == self.rear == None:
            print("Empty Queue")
        else:
            temp = self.front
            self.front=self.front.next
            print(f"Deleted {temp.data}")
    def display(self):
        if self.front == self.rear == None:
            print("Empty Queue")
        else:
            cur = self.front
            while cur:
                print(cur.data,end="->")
                cur= cur.next

q = Queue()
q.enqueue(1)
q.enqueue(2)
q.enqueue(3)
q.enqueue(4)
q.display()
q.dequeue()
q.display()


```







##
```python

```
