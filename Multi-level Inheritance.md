# Exp.No:24  
## Multi-level Inheritance

---

### AIM  
To write a Python program to get the name, age, and ID of a person and display them using multilevel inheritance.

---

### ALGORITHM

1. Define the `Person` class:
   - Inside the `Person` class, define the `__init__` method (constructor) with two parameters: `name` and `age`.
   - Inside the `__init__` method, assign the `name` to `self.name` and `age` to `self.age`.

2. Define the `PersonDetails` class that inherits from the `Person` class:
   - Inside the `PersonDetails` class, define the `__init__` method (constructor) with three parameters: `name`, `age`, and `person_id`.
   - Inside the `__init__` method, call the `__init__` method of the `Person` class using `super()` to initialize `name` and `age`.
   - Assign `person_id` to `self.person_id`.

3. Define the `DisplayDetails` class that inherits from the `PersonDetails` class:
   - Inside the `DisplayDetails` class, define the `__init__` method (constructor) with three parameters: `name`, `age`, and `person_id`.
   - Inside the `__init__` method, call the `__init__` method of the `PersonDetails` class using `super()` to initialize `name`, `age`, and `person_id`.

4. Inside the `DisplayDetails` class, define the `show_details` method:
   - Inside the `show_details` method, return a formatted string with `self.name`, `self.age`, and `self.person_id`.

5. Prompt the user to enter `name` (string), `age` (integer), and `person_id` (integer).

6. Create an instance `person` of the `DisplayDetails` class, passing `name`, `age`, and `person_id` to the constructor.

7. Call the `show_details` method on the `person` object and print the result.

8. Terminate the program.

---

### PROGRAM

```
# Parent Class
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def display_person_details(self):
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")

# Child Class (inherits from Person)
class Employee(Person):
    def __init__(self, name, age, employee_id):
        super().__init__(name, age)  # Call the constructor of Person class
        self.employee_id = employee_id
    
    def display_employee_details(self):
        self.display_person_details()  # Call display_person_details from Person class
        print(f"Employee ID: {self.employee_id}")

# Grandchild Class (inherits from Employee)
class Manager(Employee):
    def __init__(self, name, age, employee_id, department):
        super().__init__(name, age, employee_id)  # Call the constructor of Employee class
        self.department = department
    
    def display_manager_details(self):
        self.display_employee_details()  # Call display_employee_details from Employee class
        print(f"Department: {self.department}")

# Example usage:
name = input("Enter name: ")
age = int(input("Enter age: "))
employee_id = input("Enter employee ID: ")
department = input("Enter department: ")

# Creating an object of the Manager class (which will inherit from Employee and Person)
manager = Manager(name, age, employee_id, department)

# Displaying the details
print("\nManager Details:")
manager.display_manager_details()


```

### OUTPUT
![image](https://github.com/user-attachments/assets/9b3d6f9c-1842-4743-981c-46bfb1a1a92f)

### RESULT
thus the program is executed succcessfully
