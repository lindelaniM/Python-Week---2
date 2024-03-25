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
