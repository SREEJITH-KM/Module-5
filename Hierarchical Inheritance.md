# Exp.No:25  
## Hierarchical Inheritance

---

### AIM  
To write a Python program to get the employee and doctor details and display them using hierarchical inheritance. Create a parent (base) class named `Details` and two child (derived) classes named `Employee` and `Doctor`.

---

### ALGORITHM

1. **Begin the program.**
2. **Create a class Details** with an `__init__` method to initialize three attributes: `id`, `name`, and `gender`.
3. **Define a method display_details()** to print the values of `id`, `name`, and `gender`.
4. **Create a class Employee** that inherits from the `Details` class. 
   - Add two additional attributes: `company` and `department`.
   - Override the `display_details()` method to print the employee-specific attributes (`company` and `department`) along with the inherited details.
5. **Create a class Doctor** that also inherits from the `Details` class. 
   - Add two additional attributes: `hospital` and `department`.
   - Override the `display_details()` method to print the doctor-specific attributes (`hospital` and `department`) along with the inherited details.
6. **Accept input** for employee and doctor details.
7. **Create objects of Employee and Doctor** using the input.
8. **Call the `display_details()` method** for both objects to print the details.
9. **Terminate the program.**

---

### PROGRAM
```
# Parent (Base) Class: Details
class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def display_details(self):
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")

# Child Class 1: Employee
class Employee(Details):
    def __init__(self, name, age, employee_id, department):
        # Calling the constructor of the base class (Details)
        super().__init__(name, age)
        self.employee_id = employee_id
        self.department = department
    
    def display_employee_details(self):
        self.display_details()  # Display common details
        print(f"Employee ID: {self.employee_id}")
        print(f"Department: {self.department}")

# Child Class 2: Doctor
class Doctor(Details):
    def __init__(self, name, age, specialization, hospital_name):
        # Calling the constructor of the base class (Details)
        super().__init__(name, age)
        self.specialization = specialization
        self.hospital_name = hospital_name
    
    def display_doctor_details(self):
        self.display_details()  # Display common details
        print(f"Specialization: {self.specialization}")
        print(f"Hospital: {self.hospital_name}")

# Example usage:
# Getting employee details
employee_name = input("Enter employee name: ")
employee_age = int(input("Enter employee age: "))
employee_id = input("Enter employee ID: ")
employee_department = input("Enter employee department: ")

# Getting doctor details
doctor_name = input("Enter doctor name: ")
doctor_age = int(input("Enter doctor age: "))
doctor_specialization = input("Enter doctor's specialization: ")
doctor_hospital = input("Enter doctor's hospital name: ")

# Creating objects
employee = Employee(employee_name, employee_age, employee_id, employee_department)
doctor = Doctor(doctor_name, doctor_age, doctor_specialization, doctor_hospital)

# Displaying employee and doctor details
print("\nEmployee Details:")
employee.display_employee_details()

print("\nDoctor Details:")
doctor.display_doctor_details()


```

### OUTPUT  
![image](https://github.com/user-attachments/assets/55682528-587a-4ccb-927c-b1a21a8c9208)





### RESULT
Thus the program is executed successfully
