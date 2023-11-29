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

##code1

import unittest
from calculator import Calculator

class TestCalculator(unittest.TestCase):
    def setUp(self):
        self.calculator = Calculator()

    def test_add(self):
        self.assertEqual(self.calculator.add(2, 3), 5)

    def test_subtract(self):
        self.assertEqual(self.calculator.subtract(5, 2), 3)

    def test_multiply(self):
        self.assertEqual(self.calculator.multiply(4, 3), 12)

    def test_divide(self):
        self.assertEqual(self.calculator.divide(6, 2), 3)
        with self.assertRaises(ValueError):
            self.calculator.divide(5, 0)

    # Add tests for scientific operations
    def test_square_root(self):
        self.assertEqual(self.calculator.square_root(9), 3)

    def test_logarithm(self):
        self.assertEqual(self.calculator.logarithm(10), 2.302585092994046)

    # Add additional scientific operations here
    def square_root(self, x):
        return x ** 0.5

    def logarithm(self, x):
        import math
        return math.log(x)
