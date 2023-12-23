- **Classes** are blueprints (templates) for creating objects
- **Objects** are instances of classes
- Classes define the **data structure** by specifying **attributes** that describe the state of an object
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

- **\__init\__ (Constructor)**: 
	- A special [[Functions | method]] that is automatically called when a new object is created and initializes it's attributes
- **self [[Parameters | parameter]]:**
	- Allows methods to access and manipulate the attributes of the specific instance belong to
- **Instance attributes**:
	- [[Variables]] declared with the "self." prefix inside methods become instance attributes, meaning they are connected to the specific instance of the class and can be accessed from any other method inside the object