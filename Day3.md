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
