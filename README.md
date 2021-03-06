# UNIT 1 - Salma Bhar
# An electronic hardware store

## Criteria A: Planning 

### Context of the problem
There is a hardware store in Karuizawa. This store is quite old, Like 1000 years old. The owner, Mr Sakamoto, wants to upgrade his accounting software, which at the moment is kept on paper. He would like to have a software application tha replaces the accounting book. Mr Sakamoto got a new Mac PC from his nephew, and we would like to use it.

### Justification of the solution
***Here we will write the design statement: what we will do, how, by when***
we want to crate a text based application that runs on a computer, which provides the functionality for the hardware store. The app should provide action such as record of purchases, categorization of items, record of inventory, calculation of totals, billing. We will develop this application using Python. We will use Python because it is the software we are using in class at the moment. In comparison to C++ or C, Python has a lean and simple programming syntax. In addition Python has become the most popular programming language over the last years [1]. Similarly, Python has a large repository of libraries and documentation. 

[1] Finley, Klint. “The Python Programming Language Is More Popular Than Ever.” Wired, Conde Nast, 3 Mar. 2020, www.wired.com/story/python-language-more-popular-than-ever/. 

T.E.L.O.S study: 
 
T - Technical - Is the project technically possible?
We dispose of PyCharm software to make Python code and of a computer to code on. In addition, Mr. Sakamoto got a new MAC Portable Computer on which he can run the application successfully. All we need to make this project is a computer, a Python coding software and the disposal of our customer of a computer. All 3 criteria are satisfied, thus, our project is technically possible. 

E - Economic - Can the project be afforded? Will it increase profit?
This project is developed for free by UWC ISAK Japan CS students. Its benifits include time-saving and efficiency which will allow Mr. Sakamoto to manage his store's financial transactions. Moreover, an accounting notebook might cause non-intentional errors and mistakes which result in loss of money. 

L - Legal - Is the project legal?
The project is completely legal as the 1947 Japanese constitution does not criminalize digitalisation and automization. 

O - Operational - How will the current operations support the change?
TBD

S - Scheduling - Can the project be done in time?
TBD

### Criteria for Success
1. Provides clear feedback to the user (Usability)
2. **There are no bugs in the application**
3. The application should allow to calcualte the total and billing
4. Secure application: It allows user login/autenthication 

## Criteria B: Design
### Record of Tasks
| Task No | Planned Action                                                                                           | Planned Outcome                       | Time Estimated | Target Completion date | Criterion |
|---------|----------------------------------------------------------------------------------------------------------|---------------------------------------|----------------|------------------------|-----------|
| 1       | Planning: Discuss the context of the situation. ( Ideally this is the first interview with your client)  | Write the context of the problem      | 15 min         | Sep 11th               | A         |
| 2       | Development: Coded the a text-based menu system for some parts in the hardware store                     | A working program that shows the menu | 80 min         | Sep 18th               | D         |
|         |                                                                                                          |                                       |                |                        |           |

## Criteria C: Development

First test of text based menu:

```.py
welcome_msg = "Welcome to Sakamoto's store"
print(welcome_msg)
print("This is the menu")
print("=" * 20)
items = [("RAM", 10), ("CPU", 15)]
print("=" * 20)
for c, item in enumerate(items):
  print("{}. {} ...... {} USD".format(c+1, item[0], item[1]))

# print("1. RAM ...... 30 USD")
# print("2. CPU ...... 10 USD")
for n in range(3): 
  option = int(input("Enter the number of the product you want"))
  if option<1 or option>2:
    option=int(input('Option not valid. Please enter an existing product number'))
  elif option==1:
    print('Product RAM added to your cart successfully!')
    total+=10
    print('Your Total is ....... {}'.format(total))
  elif option==2:
    print('Product CPU added to your cart successfully!')
    total+=15
    print('Your Total is ....... {} USD'.format(total))
print('Your Final Total is ....... {} USD'.format(total))
print('Thank you for shopping in our store!')

#STILL NEEDS A LOT OF WORK !!!
# Check that the user entered a valid option,
# give at least three trials
# Get the quantity
# show the total 
```

The following code is a simulation of a dice. It uses the Random Library.
```.py
#3- Repeat process 1000 times and record the counts for each face
import random
counts = [0, 0, 0, 0, 0, 0]
num_trial = 20000
for trial in range(num_trial):
    number = random.randint(0,60)
    if number < 10:
        counts[0] += 1
    elif 9 < number < 20:
        counts[1] += 1
    elif 19 < number < 30:
        counts[2] += 1
    elif 29 < number < 40:
        counts[3] += 1
    elif 39 < number < 50:
        counts[4] += 1
    elif 49 < number < 60:
        counts[5] += 1
for index, c in enumerate(counts):
    error = c - num_trial/6
    print("Number of {}s: {}, expected {}, error {}".format(index+1,c, num_trial/6, error))
```  
Personal Notes on Norman Doors Video

Def: A Norman Door is a door where the design tells you to do the opposite of what you are supposed to do.

Human-Centered Design Basics:
1. Dicoverability: The ability to discover what operations one can do.
2. Feedback: A signal of what happened.

Observation --> Idea Generation --> Prototyping --> Testing (Repeat)

Comment: This small issue of bad doors highlights a wider issue on the global scale. Just like there are bad doors in this world, there also bad houses, bad drainage-systems, bad airplanes and so on. I think it is genius to consider this small issue that we usually ignore in our everyday life. That is why products have to be well-designed so it makes tasks easier and more efficient, rather than complicate them.
 
Taxes Program: 
Program to calculate the taxes: The program below uses pattern recognition to simplify the calculation of the taxes according to the table below

Table 1. Calculation of taxes based on the total
| Rate | Bill total          |
|------|---------------------|
| 5%   | >1000 BTC           |
| 10%  | 750 < total <= 1000 |
| 15%  | 500 < total <= 750  |
| 20%  | 250 < total <= 500  |
| 25%  | 0 < total <= 250    |

```.py
#This program calculates Taxes with pattern recognition
for n in [0,1,2,3,4]:
    if 250*n<total<=250*n+250:
        tax=0.25-0.05*n
    if total>1000:
        tax=0.05
```

A program that verifies perfect numbers
```.py
#This program checks if the number provided is perfect
n=int(input("enter a number "))
#Get the factors
sum=0
for div in range (1,n):
    if n%div==0:
        sum+=div
if sum==n:
    print("{} is a perfect number".format(n))
else:
    print("{} is not a perfect number".format(n))
```

The Caesar Cipher
```.py
#Encrypting
msg=input("enter your message ")
n=int(input("enter a shift value "))
encrypted_msg=""
for i in msg:
    i=chr(ord(i)+n)
    encrypted_msg+=i #concatenate text
    print(i, end="") #the end is to make the letters next to each other and not in a seperate line each!
print(" ")

#Decrypting
msg=input("enter your encrypted message ")
n=int(input("enter a shift value "))
decrypted_msg=""
for d in msg:
    d=chr(ord(d)-n)
    decrypted_msg+=d 
    print(d, end="")
```
### Securing the database
To secure the database, we will be using a Caesar Cipher. This cipher encodes messages by assigning a new letter to each existing letter using a constant shift in their ASCII code. We will proceed by the following steps: <br />
1. Open and read the database text file
2. Split the file into letters
3. Apply the shift to each letter of the file 
4. Save the new encrypted database

![alt text](generaldiagram.png) <br>
**Fig.1.** General Diagram for the Encryption process 

<br>

![alt text](cipherflowdiagram.png) <br>
**Fig.2.** Flow Diagram for the Encryption process 

```.py
# This program encryptes a database using the Caesar Cipher
# Step 1
all_db_lines = open("db", "r").readlines()
# Step 2
for line in all_db_lines:
    encrypt_line=""
    len_line = len(line)
#Step 3
    for l in range(len_line):
        print("Line number: {} out of {} {} completion {}%".format(l + 1, len_line, "."* 30, (l + 1) / len_line * 100))
        new_line=chr(ord(line[l])+2)
        encrypt_line+=new_line
    print(encrypt_line)
#Step 4
    with open("encrypted_file", "a") as wfile:
        wfile.write(encrypt_line + "\n")
```
Database
```.py
Product,price,quantity
RAM,34,56
ROM,76,98
CPU,4,57
HDD,24,98
```
## Criteria D: Functionality
In the form of a video.

## Criteria E: Evaluation


