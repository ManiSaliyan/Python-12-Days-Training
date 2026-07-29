## Pattern Baxa

<br>
* * *
<br>
* * *
<br>
* * *


```python
m=3
n=3
for i in range(0,m):
    for j in range(0,n):
        print('*',end=" ")
    print()
```



1 * * * <br>
2 3 * * <br>
4 5 6 * <br>
7 8 9 10 

```python
m=int(input("Enter Row: "))
n=int(input("Enter Column: "))
count=0
for i in range(m):
    for j in range(n):
        if i<j:
            print("*", end=" ")
        else:
            count+=1
            print(count,end=" ")
    print()
```

1 * * *  <br>
1 2 * *  <br>
1 2 3 *  <br>
1 2 3 4  <br>

- the diffrence is Re-initialising Count
```python
m=int(input("Enter Row: "))
n=int(input("Enter Column: "))
count=0
for i in range(m):
    for j in range(n):
        if i<j:
            print("*", end=" ")
        else:
            count+=1
            print(count,end=" ")
    count=0
    print()
```

1 2 3 <br>
4   5 <br>
6 7 8 <br>

```python
m=int(input("Enter Row: "))
# n=int(input("Enter Column: "))
count=0
for i in range(m):
    for j in range(m):
        if i ==0 or i == m-1 or j == 0 or j == m-1:
            count+=1
            print(count,end=" ")
        else:
            print(" ",end=" ")
    print()
```

* * * * * <br>
      *   <br>
    *    <br> 
  *      <br> 
* * * * * <br>

```python
m=int(input("Enter Row: "))
for i in range(m):
    for j in range(m):
        if i == 0 or i == m-1 or j==m-i-1:
            print("*",end=" ")
        else:
            print(" ",end=" ")
    print()
```


<br>

```python

```






## Pattern Baxa

<br>

```python

```

