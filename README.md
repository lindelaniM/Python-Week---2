# Python-Week---2

# Basic functions

    def get_greeting(name):
        return f"Hi {name}"
    message = get_greeting("Mtiza")
    print (message)

    def incr(number, by):
      return number + by
      results = incr(5,9)
    print(results)

    def mult(*numbers):
      total = 1
      for number in numbers:
          total = total * number
      return total
    mult(2,4,6)

    #Get a dictionary as a results

    def calling(**user):
        print(user)
    calling(Id = 12345, name = "Mtiza", address = "n54gf3")

#######

def is_prime(num):
    
    if num <= 1:
        print("Not a prime number")
        return
    
    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            print("Not a prime number")
            return
    
    print("The prime number is:", num)

is_prime(8)

#######

    # Local and Global scope:

    name = "a"

    def g():
        global name
        name = "b"
    g()
    print(name)

######


#Sample factorial:

def factorial_function(n):
    
    if n < 0:
        return None
        
    if n < 2:
        return 1

    product = 1
    for i in range(2, n + 1):
        product *= i
    return product

for n in range(1, 6):  # testing
    print(n, factorial_function(n))

# Recursive implementation of the factorial function.

def factorial(n):
    if n == 1:    # The base case (termination condition.)
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(4)) # 4 * 3 * 2 * 1 = 24

# Some useful exceptions

try:
    value = int(input('Enter a natural number: '))
    print('The reciprocal of', value, 'is', 1/value)        
 except ValueError:
     print('I do not know what to do.')    
 except ZeroDivisionError:
     print('Division by zero is not allowed in our Universe.')    
except: ##takes in and handle all kinds of exception: Default
    print('Something strange has happened here... Sorry!')


#Let’s discuss in more detail some useful (or rather, the most common) exceptions you may experience.

# ZeroDivisionError
#This appears when you try to force Python to perform any operation which provokes division in which the divider is zero, or is indistinguishable from zero.
#Note that there is more than one Python operator which may cause this exception to raise.
#Can you guess them all?

#: /, //, and %.

# ValueError

#Expect this exception when you're dealing with values which may be inappropriately used in some context.
#In general, this exception is raised when a function (like int() or float()) receives an argument of a proper type, but its value is unacceptable.

# TypeError
    
#This exception shows up when you try to apply a data whose type cannot be accepted in the current context.
#Look at the example:

short_list = [1]
one_value = short_list[0.5]

#AttributeError
#This exception arrives – among other occasions –
#when you try to activate a method which doesn't exist in an item you're dealing with.
#For example:

short_list = [1]
short_list.append(2)
short_list.depend(3)

# SyntaxError

#This exception is raised when the control reaches a line of code which violates Python's grammar.
#It may sound strange, but some errors of this kind cannot be identified without first running the code.
#This kind of behavior is typical of interpreted languages – the interpreter always works in a hurry and has no time to scan the whole source code.
#It is content with checking the code which is currently being run. An example of such a category of issues will be presented very soon.

#It's a bad idea to handle this exception in your programs.
#You should produce code that is free of syntax errors, instead of masking the faults you’ve caused.

# Bug vs. debug
The basic measure a developer can use against bugs is – a debugger, while the process during which bugs are removed from the code is called debugging.
According to an old joke, debugging is a complicated mystery game in which you are simultaneously the murderer, the detective, and the victim.
