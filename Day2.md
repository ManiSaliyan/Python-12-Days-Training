## Methods in List
- to insert an element
- append(value)  inserts value at the end
- insert(index,value)  inserts value at specific index
- extend([values seperated by comma])   inserts multiple elements

- to remove elements
- pop()   removes last element
- remove(value)   remove specific value
- list.clear()   remove entire elements

- Sort an list
- list.sort()   to sort an array
- list.sort(reverse=True)   to reverse sort

- x = len(list) length of an array
- x = list.count(value)   gives frequency of a value in the list

- Display element
- list.index(index_no)  display element at specific index
- list[index]

- 5 point Summary
- max(list)
- min(list)
- 
```python
append(value)
insert(index,value)
extend([values seperated by comma])

pop()
remove(value)
list.clear()

list.sort()
list.sort(reverse=True)

x = len(list)
x = list.count(value)

list.index(index_no)  display element at specific index
list[index]

max(list)
min(list)
```

## 1 Find Max and Min value in a list
```python
print("Enter the elements: ")
list1 = list(map(int,input().split()))
mini = list1[0]
maxi = list1[0]
for i in range(len(list1)):
    if (maxi<list1[i]):
        maxi=list1[i]
    if (mini>list1[i]):
        mini=list1[i]
print("Maximum Value: ",maxi)
print("Maximum Value: ",mini)
```

## 2 Sum of an Array

```python
print("Enter the elements: ")
list1 = list(map(int,input().split()))
print("Sum of array using Built in function: ",sum(list1))
summ = 0
for i in range(len(list1)):
    summ+=list1[i]
print("Sum of array without using Built in function: ",summ)
```

## 3 Reverse an Array

```python
print("Enter the elements: ")
list1 = list(map(int,input().split()))
print("Reverse array using Built in function: ",list1.reverse())
list2 = []
for i in range(len(list1),0,-1):
    list2.append(list1[i])
print("Sum of array without using Built in function: ",list2)
```
 - another method using left and right variable

```python
print("Enter the elements: ")
list1 = list(map(int,input().split()))
print("Reverse array using Built in function: ",list1.reverse())
left = list1[0]
right = len(list1)-1
while(left<right):
    list1[left],list1[right]=list1[right],list1[left]

    left+=1;right-=1;
print("Reverse array using Custom function: ",list1)
```

## 4 Sort an Array
- Bubble sort
```python
print("Enter the elements: ")
list1 = list(map(int,input().split()))
# print("sort array using Built in function: ",sorted(list1))
for i in range(len(list1)):
    for j in range(i+1,len(list1)):
        if (list1[i]>list1[j]):
            list1[i],list1[j] = list1[j],list1[i]
print("Sort array using Custom function: ",list1)
```
## Sort first half Ascending next half Descending
```python
print("Enter the elements: ")
list1 = list(map(int,input().split()))
mid = len(list1)//2
for i in range(mid):
    for j in range(i+1,mid):
        if (list1[i]>list1[j]):
            list1[i],list1[j] = list1[j],list1[i]
for i in range(mid,len(list1)):
    for j in range(i+1,len(list1)):
        if (list1[i]<list1[j]):
            list1[i],list1[j] = list1[j],list1[i]
print("Sort array using Custom function: ",list1)
```
## 
```python

```








## 
```python

```
