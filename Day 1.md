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

## 5 Strong Number
 - a no is said to be strong number if its each digits factorial sum is equal to the number itself
 -  145
 -  1! + 4! + 5! = 145
 -  1 + 24 + 120 = 145
 -  hence 145 is a strong number
```python
def fact(n):
    if n==1:
        return 1
    return n * fact(n-1)

def isStrong(n):
    tempn=n
    strong = 0
    while(tempn!=0):
        rem = tempn%10
        strong += fact(rem)
        tempn = tempn//10
    if n==strong:
        print("Strong Number")
    else:
        print("Not Strong Number")
n = int(input("Enter a Number: "))
isStrong(n)
```


## 6 Perfect Number
 - a no is said to be strong number if its sum of its positive proper divisors, excluding the number itself
 - 6 divisors  1,2,3
 - 1+2+3 = 6
 - where as 12 divisors 1,2,3,4,6
 - 1+2+3+4+6 = 16  it is not the same no hence it is not a perfect number
```python
def isPerfect(n):
    sum = 0
    for i in range(1,n):
        if(n%i==0):
            sum+=i
    if sum==n:
        print("Perfect Number")
    else:
        print("Not aPerfect Number")
        
n = int(input("Enter a Number: "))
isPerfect(n)
```

## 7 Happy Number

```python
def isHappy(n):
    seen = set()
    tempn = n
    val = 0
    x=0
    while(x<10):
        while(tempn!=0):
            rem = tempn%10
            val += rem**2
            tempn = tempn//10
        tempn=val
        val=0
        x+=1
    if tempn==1:
        print("Happy")
    else:
        print("Not happy")

isHappy(94)
```
