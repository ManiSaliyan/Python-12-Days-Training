## Linked List
 - class = blueprint of object
 - object - an Entity or instance of class
 - def __init__(self,var...):   constructor
 - for Train Concept
 - Train is linked List
 - Train Engine is Head
 - if head is None train has no compartments
 - Node
```python
class Node:
    def __init__(self,d):
        self.d = d
        self.next=None
```
 - linked List
```python
class LinkedList:
    def __init__(self):
        self.head=None
```
 - insert at begining
   - if head is none update head with address of newNode
   - else assign head value to the newNode next and
   ```python
    def insertBeg(self,d):
        node = Node(d)
        if self.head==None:
            self.head = node
        else:
            node.next=self.head
            self.head = node
   ```
