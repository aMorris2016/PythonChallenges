## Love Score Calculator

A program that tests the compatibility between two people.

To work out the love score between two people:
- Take both people's names and check for the number of times the letters in the word TRUE occurs. 
- Then check for the number of times the letters in the word LOVE occurs. 
- Then combine these numbers to make a 2 digit number.
- For Love Scores less than 10 or greater than 90, the message should be:
  "Your score is **x**, you go together like coke and mentos."
- For Love Scores between 40 and 50, the message should be:
  "Your score is **y**, you are alright together."
- Otherwise, the message will just be their score. e.g.:
  "Your score is **z**."
  
  ![love_calculator](https://user-images.githubusercontent.com/19298335/214213835-9f042588-888c-4dd6-8431-e638103a6597.gif)

```
print("Welcome to the Love Score Calculator!")
name1 = input("What is your name? \n")
name2 = input("What is their name? \n")

name1_lowercase = name1.lower()
name2_lowercase = name2.lower()
combined_names = name1_lowercase + name2_lowercase

t_count = combined_names.count("t")
r_count = combined_names.count("r")
u_count = combined_names.count("u")
e_count = combined_names.count("e")
true = t_count + r_count + u_count + e_count
first_digit = str(true)

l_count = combined_names.count("l")
o_count = combined_names.count("o")
v_count = combined_names.count("v")
love = l_count + o_count + v_count + e_count
second_digit = str(love)

score = int(first_digit + second_digit)

if score < 10 or score > 90:
    print(f"Your score is {score}, you go together like coke and mentos.")
elif score >=40 and score <=50:
    print(f"Your score is {score}, you are alright together.")
else:
    print(f"Your score is {score}.")
```
https://replit.com/@aileenmorris201/lovecalculator?v=1
