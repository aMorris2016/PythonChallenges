## Tip Calculator
A simple program that calculates the tip and splits the bill equally based on the given number of people in the party.

![tip_calculator](https://user-images.githubusercontent.com/19298335/213610004-a2e48bef-c967-42ab-86d5-5d43dacad242.gif)

```
print("Welcome to the tip calculator!\n\n")
bill = float(input("What was the total bill? "))
tip_percent = int(input("What percentage tip would you like to give?\n 10, 12, or 15? "))
num_people = int(input("How many people to split the bill? "))
bill_share = bill * (tip_percent/100 + 1)/ num_people
message = ("Each person should pay: ${x:.2f}")
print(message.format(x=bill_share))
```

https://replit.com/@aileenmorris201/tip-calculator?v=1
