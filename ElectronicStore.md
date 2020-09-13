# An electronic hardware store

## Criteria A: Planning 

### Context of the problem
There is a hardware store in Karuizawa. This store is quite old, Like 1000 years old. The owner, Mr Sakamoto, wants to upgrade his accounting software, which at the moment is kept on paper. He would like to have a software application tha replaces the accounting book. Mr Sakamoto got a new Mac PC from his nephew, and we would like to use it.

### Justification of the solution
***Here we will write the design statement: what we will do, how, by when***
we want to crate a text based application that runs on a computer, which provides the functionality for the hardware store. The app should provide action such as record of purchases, categorization of items, record of inventory, calculation of totals, billing. We will develop this application using Python. We will use Python because it is the software we are using in class at the moment. In comparison to C++ or C, Python has a lean and simple programming syntax. In addition Python has become the most popular programming language over the last years [1]. Similarly, Python has a large repository of libraries and documentation. 

T.E.L.O.S study: 

[1] MLA citation for the data supporting that Python is the most popular programming language

## Criteria for Success
1. Provides clear feedback to the user (Usability)
1. **There are no bugs in the application**
1. The application should allow to calcualte the total and billing
1. Secure application: It allows user login/autenthication 


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

# Check that the user entered a valid option,
# give at least three trials
# Get the quantity
# show the total 
```
