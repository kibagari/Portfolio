## Fibonacci sequence generator.

This is a sample script that accepts user input as an integer and outputs a sequence of fibonacci numbers. The function takes the input, and through a series of if/elif/else statements, generates a list of numbers in the sequence, then prints the list in the console.

```Python
"""
Generate a fibonacci sequence at length designated by a user input.
"""

def gen_fib():
    count = int(input("How many fibonacci numbers would you like to generate? "))
    i = 1
    try:
        if count <= 0:
            fib = []
        elif count == 1:
            fib = [1]
        elif count == 2:
            fib = [1,1]
        elif count > 2:
            fib = [1,1]
            while i < (count - 1):
                fib.append(fib[i] + fib[i-1])
                i += 1
    except ValueError:
        print("Ooops this is not a valid number.")
        fib = []
    return fib


print(gen_fib())
```

A sample output is provided below:

![Image of Fib](https://kibagari.github.io/Portfolio/images/fib.png)
