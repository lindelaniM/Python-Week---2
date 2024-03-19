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

    # Local and Global scope:

    name = "a"

    def g():
        global name
        name = "b"
    g()
    print(name)
