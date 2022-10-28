# Password_creator
This program can create password which contains random not ordered variables

# Given a list of letters, numbers, and symbols 
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

# Greetings to the program
print("Welcome to the Python Password generator!")

# Input how many variables do you want to create password
nr_letters= int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

# Don't forget to import random in the beginning
import random

# Create a list of password
password_list = []

#By using for loop and range() function, let the computer choose letters, numbers, and symbols by inputting how many of them you want
for letter in range(1, nr_letters + 1):
  password_list.append(random.choice(letters))

for number in range(1, nr_numbers + 1):
  password_list += random.choice(numbers)

for symbol in range(1, nr_symbols + 1):
  password_list += random.choice(symbols)

# Then, shuffle the variables randomly
random.shuffle(password_list)

# Convert the list of passwords in strings
password = ""

for variables in password_list:
  password += variables

# Print the result
print(password)
