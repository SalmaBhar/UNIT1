Remark: these are just my digital class notes, the rest of my notes are in my physical notebook.  

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
    print('Option not valid. Please enter an existing product number')
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

# Dice Simulation
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
# Personal Notes on Norman Doors Video

Def: A Norman Door is a door where the design tells you to do the opposite of what you are supposed to do.

### Human-Centered Design Basics:
1. Dicoverability: The ability to discover what operations one can do.
2. Feedback: A signal of what happened.

Observation --> Idea Generation --> Prototyping --> Testing (Repeat)

### Comment
This small issue of bad doors highlights a wider issue on the global scale. Just like there are bad doors in this world, there also bad houses, bad drainage-systems, bad airplanes and so on. I think it is genius to consider this small issue that we usually ignore in our everyday life. That is why products have to be well-designed so it makes tasks easier and more efficient, rather than complicate them.
 
# Taxes Program 
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

#This program calculates Taxes

#Step 1 Enter and validate input which is a total amount
while True:
    total=int(input("Please enter the Total amount (BTC):"))
    if total<0:
        print("The total cannot be negative, try again.")
    else:
        break

#Step 2: without using pattern recognition
if 0<total<=250:
    tax=0.05
if 250<total<=500:
    tax=0.10
if 500<total<=750:
    tax=0.15
if 750<total<=1000:
    tax=0.20
if total>1000:
    tax=0.25

#With pattern recognition
for n in [0,1,2,3,4]:
    if 250*n<total<=250*n+250:
        tax=0.25-0.05*n
    if total>1000:
        tax=0.05
        
# Step 3 show the result in a frame
print("#"*50)
print("#"," "*46,"#")
print("#",tax) # I CANNOT GET THE # AFTER THE TAX TOTAL IN THE FRAME IN THE RIGHT PLACE!
print("#"," "*46,"#")
print("#"*50)

```
## I CANNOT GET THE # AFTER THE TAX TOTAL IN THE FRAME IN THE RIGHT PLACE!

# A program that verifies perfect numbers
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
    
#Edit so it shows us the 1st 100 perfect number
n=1000001
my_sum=0
my_list=[]
first_hundred=0

if first_hundred<101:
    for num in range (1, n):
        for div in range (1,num):
            if num%div==0:
                my_sum+=div
        if my_sum==num:
            first_hundred+=1
            my_list.append(num)
else:
    print(my_list)
```
# Quick Exercice 
input: 3578195
output: true/false
sum of the 1st 3 digits and sum of last 4 digits are the same.
```.py
num=3578195
num_str=str(num)
print(num_str)
f=num_str[0:3]
l=num_str[3:]
print(f, l)
sumf=0
suml=0
for n in f:
    sumf+=int(n)
for i in l:
    suml+=int(i)
print(sumf==suml)
```
! I copied some parts from Dr. Ruben's repository which indicate the task done in class :) ! 
