## Operators
  - Logical
  - Comparison

## Loops


## 3 Reverse a number 
```python
n = int (input())
rev = 0
while(n!=0):
    rem = n%10
    rev = (rev*10) + rem
    n = n//10
print(rev)
```


## 4 Prime Number
```python
def isPrime(n):
    flag = True
    for i in range(2,n):
        if(n%i==0):
            flag = False
    return flag
    # if flag==0:
    #     print(n," is a Prime Number")
    # else:
    #     print(n," is not a Prime Number")
lis = []

sr = int (input("Enter Starting Range: "))
er = int (input("Enter Starting Range: "))
for i in range(sr,er+1):
    if isPrime(i):
        lis.append(i)
for i in lis:
    print(i)

```


## 5 Palindrome
```python
def isPalindrome(n):
    tempn=n
    rev = 0
    while(tempn!=0):
        rem = tempn%10
        rev = (rev*10) + rem
        tempn = tempn//10
    if n==rev:
        print("Palindrome")
    else:
        print("Not Palindrome")
n = int(input("Enter a Number: "))
isPalindrome(n)
```
