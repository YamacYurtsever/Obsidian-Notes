- A **class** is a blueprint or a template for creating objects
- **Objects** are instances of classes
- Classes define the **data structure** by specifying **properties** that describe the state of an object
- Classes also define **methods**, which are functions or behaviors that an object can perform
- Allows for the creation of organized, reusable, and modular code by encapsulating related data and functionality within classes and creating instances from those classes when needed

#### Implementation
Python
```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def display_info(self):
        print(f"{self.year} {self.make} {self.model}")

def main():
	my_car = Car("Toyota", "Camry", 2022)
	my_car.display_info()  
```
! /__/init/__/ is a special method (constructor) that initializes the object's attributes