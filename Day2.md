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
## Count of Each element
```python
print("Enter the elements: ")
list1 = list(map(int,input().split()))
length = len(list1)
visited=[]
# print("sort array using Built in function: ",sorted(list1))
print("\nCount of Each elements: ")
for i in range(length):
    if list1[i] in visited:
        continue
    visited.append(list1[i])
    count=0
    for j in range(length):
        if list1[i] == list1[j]:
            count+=1
    print(list1[i]," : ",count)
        
```
 - To print count in an Descending order
```python
def count(list1):
    length = len(list1)
    visited=[]
    freq=[]
    print("\nCount of Each elements: ")
    for i in range(length):
        if list1[i] in visited:
            continue
        visited.append(list1[i])
        count=0
        for j in range(length):
            if list1[i] == list1[j]:
                count+=1
        freq.append(count)
    for i in range(len(visited)):
        for j in range(i+1,len(visited)):
            if (freq[i]<freq[j]):
                freq[i],freq[j] = freq[j],freq[i]
                visited[i],visited[j] = visited[j],visited[i]
    for i in range(len(visited)):
        print(visited[i]," : ",freq[i])

print("Enter the elements: ")
list1 = list(map(int,input().split()))
count(list1)
```

## Count of unique elements in an Array
```python
def uniqueCount(list1):
    length = len(list1)
    count=0
    visited = []
    for i in range(length):
        if list1[i] in visited:
            continue
        visited.append(list1[i])
        count+=1
    print("Total no of unique elements",len(visited))
print("Enter the elements: ")
list1 = list(map(int,input().split()))
uniqueCount(list1)
```
# String
 - string.capitalize()   to capitalize first letter
 - string.casefold()  convert Uppercase to Lowercase
 - string.upper()  to capitalize all word
 - string.lower()  to lowercase all letters
 - string.center(space_value_in_int)    the value will be half and the amount of space added at both sides
 - string.count("letter")   return count of a letter in a string
 - string.endswith("word or letter")  returns True or False
 - string.expandtabs()   if string stored as "A\tB"  o/p=>  A     B
 - string.find("letter or word")   return index of first occurence
 - str="hi {}".format("Mani")    o/p=>   hi Mani
 - string.isalnum()   Return True if string contain only letter and number not if contains special characters
 - string.isdecimal()   
 - string.isdigit()
 - string.islower()
 - string.isnumeric()
 - string.isupper()
 - string.isspace()   to check whether a string is space

 - Join Method
 - " ".join(list)
 - 
```python
string.capitalize()
string.casefold()
string.upper()
string.lower()
string.center(space_value_in_int)
string.count("letter")
string.endswith("word or letter")
string.expandtabs()
string.find("letter or word")
str="hi {}".format("Mani")
string.isalnum()
string.isdecimal()
string.isdigit()
string.islower()
string.isnumeric(
string.isupper()
string.isspace()
ord("letter")   gives ASCII number
```
## Check String is alphabet without Built in Function
```python
strs = input("Enter a String: ")
count=0
for i in strs:
    count+=1
print("Length of String is: ",count)
```

## Length of String without Built in Function
```python
strs = input("Enter a String: ")
count=0
for i in strs:
    count+=1
print("Length of String is: ",count)
```

## Convert all lowercase to uppercase in a string and viceversa
```python
strs = input("Enter a String: ")
str2 = str()
for i in strs:
    if i.isupper():
        i = i.lower()
        str2 = str2+i
    else:
        i = i.upper()
        str2 = str2+i
print(str2)
```

## Count no of vovels
```python
strs = input("Enter a String: ")
cv = 0
cc = 0
for i in strs:
    i = i.lower()
    if i=="a" or i=="e" or i=="i" or i=="o" or i=="u":
        cv+=1
    elif ord(i)>=65 and ord(i)<=122:
        cc+=1
    else:
        continue
print("Vowel Count: ",cv)
print("Consonants Count: ",cc)
```
## Remove vowels in a string
```python
strs = input("Enter a String: ")
str2 = str()
vovels = ["a","e","i","o","u","A","E","I","O","U"]
for i in strs:
    if i in vovels:
        continue
    else:
        str2 = str2+i
print(str2)
```
## Reverse a String and check whether it is Palindrome
```python
str1 = input("Enter a String: ")
str2= str()
length = 0
for i in str1:
    length+=1
for i in range(length-1,-1,-1):
    str2 = str2+str1[i]
if str1==str2:
    print("Palinrome")
else:
    print("Not Palinrome")

```
## Remove all digits in a string
```python
str1 = input("Enter a String: ")
str2= str()
length = 0
for i in str1:
    if i.isdigit():
        continue
    else:
        str2 = str2+i
print(str2)
```
## Remove all the Space in a given String
```python
str1 = input("Enter a String: ")
str2= str()
for i in str1:
    if i!=" ":
        str2 = str2+i
print(str2)
```
## 
```python
def freqChar(stri,char):
    count=0
    for i in stri:
        if i == char:
            count+=1
    return count
str1 = input("Enter a String: ")
visited = []
for i in str1:
    if i not in visited:
        visited.append(i)
        print(i," : ",freqChar(str1,i))
```
## Anagram problem  eat,ate,tea  just character reframed 
```python

str1 = sorted(input("Enter First String: ").lower())
str2 = sorted(input("Enter Second String: ").lower())
if str1==str2:
    print("Anagram")
else:
    print("Not Anagram")

```








## 
```python

```
