# rock_paper_scissors
The game of rock_paper_scissors
<br>
#Password Generator Project
<br>

<br>
import random
<br>

<br>
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
<br>

<br>
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
<br>
<br>
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']
<br>

<br>
print("Welcome to the PyPassword Generator!")
<br>
nr_letters= int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

#Eazy Level - Order not randomised:
#e.g. 4 letter, 2 symbol, 2 number = JduE&!91
ltr_string = ""
for n in range(0,nr_letters):
  ltr_index = random.randint(0,len(letters)-1)
  ltr_string += letters[ltr_index]

char_string = ""
for n in range(0, nr_symbols):
  char_index = random.randint(0, len(symbols)-1)
  char_string += symbols[char_index]

num_string = ""
for n in range(0, nr_numbers):
  num_index = random.randint(0, len(numbers)-1)
  num_string += numbers[num_index]

N = nr_letters + nr_symbols + nr_numbers
pwd = ltr_string + char_string + num_string

pwd_list = list(pwd)
random.shuffle(pwd_list)

final_password = ""
for n in range(0,N-1):
  char = str(pwd_list[n])
  final_password += char
print(final_password)



#Hard Level - Order of characters randomised:
#e.g. 4 letter, 2 symbol, 2 number = g^2jk8&P
