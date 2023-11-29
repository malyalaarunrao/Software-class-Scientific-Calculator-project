# Software-class-Scientific-Calculator-project
Git Usage and Calculator Implementation
##code

class Calculator:
    def add(self, x, y):
        return x + y

    def subtract(self, x, y):
        return x - y

    def multiply(self, x, y):
        return x * y

    def divide(self, x, y):
        if y == 0:
            raise ValueError("Cannot divide by zero")
        return x / y

    # Add additional scientific operations here
    def square_root(self, x):
        return x ** 0.5

    def logarithm(self, x):
        import math
        return math.log(x)
