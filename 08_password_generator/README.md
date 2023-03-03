## Password Generator
A program that generates a strong random password of the specified length using alphabets, numbers, and symbols. 

- The program will take the number of letters, symbols and numbers as input from the user. 
- I used a loop ranging between 1 and the number inputs from user, and in every iteration, program will randomly choose a character
  from the list of letters, numbers and symbols then store them into a resultant password as a list. 
- The generated password list is passed to the random.shuffle function in order to reorganize the list 
  to ensure that password does not follow a predictable pattern.
- Used the loop function to store the list of characters to a string variable to get the final password.

![password_generator](https://user-images.githubusercontent.com/19298335/222618832-158a217f-9909-427c-8398-f98a0810fdd0.gif)

```
import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!\n")
nr_letters= int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

password_list = []

for char in range(1, nr_letters + 1):
   password_list.append(random.choice(letters))

for char in range(1, nr_symbols + 1):
  password_list.append(random.choice(symbols))

for char in range(1, nr_numbers + 1):
  password_list.append(random.choice(numbers))
  
random.shuffle(password_list)

password = ''
for char in password_list:
  password += char

print(f"Your new password is {password}")
```

https://replit.com/@aileenmorris201/password-generator?v=1

