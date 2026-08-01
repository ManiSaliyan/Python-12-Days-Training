##
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
            self.rear.next= nn
        else:
            self.rear.next = nn
            self.rear=nn
            self.rear.next= self.front
        print(f"Inserted {nn.data}")
    def dequeue(self):
        if self.front == self.rear == None:
            print("Empty Queue")
        else:
            temp = self.front
            self.front=self.front.next
            self.rear.next = self.front
            print(f"Deleted {temp.data}")
    def display(self):
        if self.front == self.rear == None:
            print("Empty Queue")
        else:
            prev=None
            cur = self.front
            while prev!=self.front:
                prev=cur
                print(prev.data,end="->")
                cur= cur.next
                prev=prev.next
            print()

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
class Queue:
    def __init__(self,k):
        self.k = k
        self.queue = [None]*k
        self.front=self.rear=-1
    def enqueue(self,data):
        if (self.rear+1)% self.k==self.front:
            print("Circular Queue is Full")
        elif self.front ==-1:
            self.front=self.rear=0
            self.queue[self.rear] = data
        else:
            self.rear = (self.rear+1)%self.k
            self.queue[self.rear] = data
        print(f"Inserted {self.queue[self.rear]}")
    def dequeue(self):
        if self.rear==-1:
            print("The Circular Queue is Empty")
        elif self.front==self.rear:
            temp=self.queue[self.front]
            self.queue[self.front]=None
            self.front= self.rear=-1
            print(f"Deleted {temp}")
        else:
            temp=self.queue[self.front]
            self.queue[self.front]=None
            self.front = (self.front+1)%self.k
            print(f"Deleted {temp}")
    def traverse(self):
        if self.rear==-1:
            print("The Circular Queue is Empty")
        else:
            for i in range(self.front,self.k):
                if self.queue[i]:
                    print(self.queue[i],end="->")
            for i in range(0,self.rear+1):
                if self.queue[i]:
                    print(self.queue[i],end="->")
            print()

queue = Queue(4)
queue.enqueue(1)
queue.enqueue(2)
queue.enqueue(3)
queue.traverse()
queue.dequeue()
queue.traverse()
queue.dequeue()
queue.dequeue()
queue.dequeue()
queue.traverse()
```

## Linear Search
```python
lis = [1,2,3,6,5,4]
key =5
def linear(lis,key):
    for i in lis:
        if i==key:
            return True
    return False
if linear(lis,key):
    print("Key Found")
else:
    print("Key Not Found")
```
## Binary Search
```python
def binary(lis,key):
    left = 0
    right = len(lis)-1
    while(left<=right):
        mid=(left+right)//2
        if lis[mid] == key:
            return True
        elif lis[mid]<key:
            left=mid+1
        else:
            right=mid-1
    return False
lis = [1,2,3,4,5,6]
key =5
if binary(lis,key):
    print("Key Found")
else:
    print("Key Not Found")
```

## Bubble Sort
```python
def bubble(lis):
    length = len(arr)
    for i in range(length):
        for j in range(i+1,length):
            if arr[i]>arr[j]:
                arr[i],arr[j]=arr[j],arr[i]
    return lis

arr = [1,3,6,2,5]
print(bubble(arr))

```

## Insertion Sort
```python
arr= [1,4,5,3,2]

def selection(lis):
    length = len(arr)
    for i in range(length):
        for j in range(1,length-1):
            if arr[j]>arr[j+1]:
                arr[j],arr[j+1]=arr[j+1],arr[j]
    return lis

arr = [1,3,6,2,5]
print(selection(arr))
```

##
```python

```

##
```python

```




##
```python

```
