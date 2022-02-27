# Problem 1
I decided to solve this in python3
I first tried this solution:
```#!/bin/python3


import sys


t = int(input().strip())
for a0 in range(t):
    n = int(input().strip())
    sum = 0
    for i in range(n):
      if (i%3 == 0 or i%5==0):
          sum += i
    print('The sum is: ' + str(sum))
```
It seemed to work but it failed test cases 2 and 3
by looking into it i found out that using % operator will cause this problem for higher values of numbers.
So i used this:
```#!/bin/python3

import sys


t = int(input().strip())
for a0 in range(t):
    n = int(input().strip())
    a = ((n-1)//3) 
    b = ((n-1)//5) 
    c = ((n-1)//15) 
    sum = (((3 * a * (a+1))//2) + ((5 * b * (b+1))//2) - ((15 * c * (c+1))//2)) 
    print(int(sum))
```

# Problem 2
```
#!/bin/python3

import sys


t = int(input().strip())
for a0 in range(t):
    n = int(input().strip())
    total = 0
    a = 0
    b = 1
    while b < n:
        if b%2==0:   
            total += b
        a,b = b,a+b
    print(total)
```
