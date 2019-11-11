## Collatz Conjecture proof.

This script uses a recursive function to count the steps required to implement the collatz sequence on a user input integer. The collatz sequence states that for any positive integer n, there exists a sequence that can reduce that integer to 1. If the integer already equals 1, 0 steps are required. If the integer is even, pass n/2 through the sequence. If the integer is odd, pass 3n+1 through the sequence.

```Python
def collatz(n):
    try:
        if n == 1:
            return 0
        elif n % 2 == 0:
            return 1 + collatz(n / 2)
        elif n % 2 == 1:
            return 1 + collatz(3 * n + 1)
    except ValueError:
        print("This is not a valid input")


i = int(input("Enter a positive number: "))
print(collatz(i))
```

A sample output is provided:

