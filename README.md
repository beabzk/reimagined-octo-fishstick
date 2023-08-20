### Question 1
```python
num = int(input("Enter a 5-digit number: "))
a = num // 10000 
b = (num % 10000) // 1000
c = (num % 1000) // 100
d = (num % 100) // 10
e = num % 10
print(a, "   ", b, "   ", c, "   ", d, "   ", e)

# Use integer division and modulo to extract each digit.
```
### Question 2
```python 
num = int(input("Enter a number: "))
factorial = 1
for i in range(1, num+1):
  factorial = factorial * i
print("The factorial of", num, "is", factorial) 

# Use a for loop to multiply numbers from 1 to num 
```
### Question 3
```python
import math
x = float(input("Enter x: "))
n = int(input("Enter n: "))
cosx = 1
sign = 1
for i in range(2, n+1, 2):
  sign = -sign
  cosx += sign * (x ** i) / math.factorial(i)
print("cos(", x, ") = ", cosx)

# Use a for loop and alternate signs to calculate terms
```
### Question 4
#### A)
```python
# Pattern iv
for i in range(1, 6):
    for j in range(5-i):
        print(' ', end=' ')
    for k in range(i):
        print('*', end=' ')
    for l in range(i-1):
        print('*', end=' ')
    print() 
```
```python
# Pattern v
for i in range(1, 6):
    for j in range(5-i):
        print(' ', end=' ')
    for k in range(i):
        print(i, end=' ')
    for l in range(i-1):
        print(i, end=' ')
    print()
```
```python
# Pattern vi
for i in range(1, 6):
    for j in range(5-i):
        print(' ', end=' ')
    for k in range(i, 0, -1):
        print(k, end=' ')
    for l in range(2, i+1):
        print(l, end=' ')
    print()
```
#### B)
```python
for i in range(65, 70):
  for j in range(65, i+1):
    print(chr(j), end=' ')
  print()
  
# Use nested loops and chr() to print letters
```
### Question 5
```python
import math

a = float(input("Enter the value of a: "))
b = float(input("Enter the value of b: "))
c = float(input("Enter the value of c: "))

discriminant = b**2 - 4*a*c

if discriminant > 0:
    x1 = (-b + math.sqrt(discriminant)) / (2*a)
    x2 = (-b - math.sqrt(discriminant)) / (2*a)
    print(f"The solutions are x1 = {x1} and x2 = {x2}")
elif discriminant == 0:
    x = -b / (2*a)
    print(f"The solution is x = {x}")
else:
    real_part = -b / (2*a)
    imaginary_part = math.sqrt(-discriminant) / (2*a)
    print(f"The solutions are x1 = {real_part} + {imaginary_part}i and x2 = {real_part} - {imaginary_part}i")

```


### Question 6
```python 
num = int(input("Enter a number: "))

if num > 1:
    for i in range(2, int(num/2)+1):
        if (num % i) == 0:
            print(num, "is not prime")
            break
    else:
        print(num, "is prime")
else:
    print(num, "is not prime")

```

### Question 7
```python
import math

def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

x = float(input("Enter the value of x: "))
n = int(input("Enter a positive integer n: "))

sin_x = 0
for i in range(n+1):
    coefficient = (-1)**i
    numerator = x**(2*i + 1)
    denominator = factorial(2*i + 1)
    sin_x += (coefficient) * (numerator / denominator)

print(f"The sine of {x} computed using {n} terms in the series expansion is {sin_x}")
```

### Question 10
```python
numbers = []
while True:
    num = input("Enter a number (or 'done' to finish): ")
    if num == 'done':
        break
    else:
        numbers.append(float(num))

print(f"The maximum number entered is {max(numbers)}")
print(f"The minimum number entered is {min(numbers)}")
```
### Question 11
```python
n = int(input("Enter a positive integer n: "))

a, b = 0, 1
for i in range(n):
    print(a, end=' ')
    a, b = b, a + b
```
### Question 12
```python
for num in range(1, 501):
    sum_of_cubes = 0
    temp = num
    while temp > 0:
        digit = temp % 10
        sum_of_cubes += digit ** 3
        temp //= 10

    if num == sum_of_cubes:
        print(num)
```
### Question 13
```python
import math

num = int(input("Enter your favorite positive integer: "))
sqrt_num = math.sqrt(num)
print(f"The square root of {num} is {sqrt_num}")
```
### Question 14
```python
count = 1
for i in range(1, 5):
    for j in range(i):
        print(count, end=' ')
        count += 1
    print()
```
### Question 15
```python
num = int(input("Enter an integer number: "))
reversed_num = 0

while num != 0:
    digit = num % 10
    reversed_num = reversed_num * 10 + digit
    num //= 10

print(f"The reversed number is {reversed_num}")
```

### Question 16
```python
n = int(input("Enter a positive integer n: "))

sum_of_series = 0
for i in range(1, n+1):
    sum_of_series += 1/i

print(f"The sum of the series is {sum_of_series}")
```
### Question 17
```python
base = float(input("Enter the base number: "))
exponent = float(input("Enter the exponent: "))

result = base ** exponent

print(f"{base} raised to the power of {exponent} is {result}")

```
### Question 18
```python
n = int(input("Enter a positive integer n: "))

ln_2 = 0
for i in range(1, n+1):
    ln_2 += (-1)**(i+1) * (1/i)

print(f"The natural logarithm of 2 computed using {n} terms in the series is {ln_2}")

```
