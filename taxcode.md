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
print("#",tax," "*41,"#")
print("#"," "*46,"#")
print("#"*50)

```
