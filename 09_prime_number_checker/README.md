## Prime Number Checker
Prime numbers are numbers that can only be cleanly divided by themselves and 1. 
This program checks whether a given number is a prime number or not.

![prime_number_checker](https://user-images.githubusercontent.com/19298335/233259005-f8cc340e-4479-46a8-b526-58aad0ae54d6.gif)

```
import math

def prime_checker(number):
    is_prime = True
    last_divisor = math.ceil(math.sqrt(number))

    for x in range(2, last_divisor):
        if number % x == 0:
            is_prime = False
    if is_prime:
        print("It's a prime number.")
    else:
        print("It's not a prime number")
        
n = int(input("Check this number: "))

prime_checker(number=n)
```

Try it out for yourself: https://replit.com/@aileenmorris201/primenumberchecker?v=1
