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


try:
    value = int(input('Enter a natural number: '))
    print('The reciprocal of', value, 'is', 1/value)        
# except ValueError:
#     print('I do not know what to do.')    
# except ZeroDivisionError:
#     print('Division by zero is not allowed in our Universe.')    
except: ## takes in and handle all kinds of exception: Default
    print('Something strange has happened here... Sorry!')

# Some useful exceptions
# Let’s discuss in more detail some useful (or rather, the most common) exceptions you may experience.

# ## ZeroDivisionError
# This appears when you try to force Python to perform any operation which provokes division in which the divider is zero, or is indistinguishable from zero.
# Note that there is more than one Python operator which may cause this exception to raise.
# Can you guess them all?

# : /, //, and %.

# ## ValueError

# Expect this exception when you're dealing with values which may be inappropriately used in some context.
# In general, this exception is raised when a function (like int() or float()) receives an argument of a proper type, but its value is unacceptable.

# ## TypeError
    
# This exception shows up when you try to apply a data whose type cannot be accepted in the current context.
# Look at the example:

