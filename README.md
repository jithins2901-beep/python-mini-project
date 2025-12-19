# python-mini-project 1
import math

# Base class
class Shape:
    def calculate_area(self):
        raise NotImplementedError("Subclasses must implement this method.")

# Subclass: Circle
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def calculate_area(self):
        return math.pi * self.radius ** 2

# Subclass: Rectangle
class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def calculate_area(self):
        return self.width * self.height

# List of shape objects
shapes = [
    Circle(5),
    Rectangle(4, 6),
    Circle(3.5),
    Rectangle(2, 9)
]

# Loop to calculate and print areas
for shape in shapes:
    print(f"Area: {shape.calculate_area():.2f}")
