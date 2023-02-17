## Treasure Map
A program that marks a square on a map grid using a two-digit system
The first digit in the input specifies the column (the position on the horizontal axis).
The second digit in the input will specify the row number (the position on the vertical axis).

![treasure_map](https://user-images.githubusercontent.com/19298335/219567829-bab669be-b688-4ae1-bbd7-7720a37065a6.gif)

```
row1 = ["⬜️","️⬜️","️⬜️"]
row2 = ["⬜️","⬜️","️⬜️"]
row3 = ["⬜️️","⬜️️","⬜️️"]
grid = [row1, row2, row3]
print(f"{row1}\n{row2}\n{row3}")
position = input("Where do you want to put the treasure? ")

#Convert position into a string
digits = str(position)

#Extract each digit and convert back to an integer. Subtract 1 to get index of column and row
column = int(digits[1]) - 1
row = int(digits[0]) - 1

#Assign 'X' to the selected position on the grid
grid[column][row]= 'X'

print(f"{row1}\n{row2}\n{row3}")
```

https://replit.com/@aileenmorris201/Treasure-Map?v=1
