## Inventory

This is a block of Python script that I am working on to create an inventory tracker for a RPG game. The snippet shows the currency tracking function. It is a function that, when called, asks the user to select a coin type and amount, then stores the amount as the index value for the coin type's key.  The script then calls the function and prints the currency dictionary.

```Python
import sys

currency = {"PP": 0,
            "GP": 0,
            "EP": 0,
            "SP": 0,
            "CP": 0}


def addCurrency(coin, amount):
    coin = input("What type of currency? ")
    amount = int(input("How much " + coin + " did you receive? "))
    if coin in currency.keys():
        currency[coin] += amount


addCurrency("", 0)
addCurrency("", 0)
addCurrency("", 0)
addCurrency("", 0)
addCurrency("", 0)

for x, y in currency.items():
    print(x, y)
```

