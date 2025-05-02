# Exp.No:23  
## Multiple Inheritance

---

### AIM  
To write a Python program to get the name, attendance, and ID of a student and check if they are eligible for the next module using multiple inheritance. If attendance > 80, the student is eligible; otherwise, not eligible.

---

### ALGORITHM

1. Define the `Student` class.
2. Inside the `Student` class, define the `__init__` method (constructor). The `__init__` method accepts two parameters: `name` and `student_id`.
    - Inside the `__init__` method: Assign the value of `name` to `self.name` and `student_id` to `self.student_id`.
3. Define the `get_student_info` method inside the `Student` class:
    - This method should return a string formatted with `self.name` and `self.student_id`.
4. Define the `Attendance` class, which inherits from the `Student` class.
5. Inside the `Attendance` class, define the `__init__` method (constructor).
    - The `__init__` method accepts three parameters: `name`, `student_id`, and `attendance`.
    - Inside the `__init__` method: Call the parent class constructor `super().__init__(name, student_id)` to initialize `name` and `student_id`. Assign the value of `attendance` to `self.attendance`.
6. Define the `check_eligibility` method inside the `Attendance` class:
    - If `self.attendance` is greater than 80, return a formatted string indicating the student is eligible for the module exam.
    - Otherwise, return a formatted string indicating the student is not eligible for the module exam.
7. Prompt the user to enter the `name` (as a string), `student_id` (as an integer), and `attendance` (as an integer).
8. Create an instance `student` of the `Attendance` class, passing the entered `name`, `student_id`, and `attendance` to the constructor.
9. Call the `check_eligibility` method on the `student` object and print the result.
10. Terminate the program.

---

### PROGRAM

# Parent Class 1: PersonalDetails
class PersonalDetails:
    def __init__(self, name, student_id):
        self.name = name
        self.student_id = student_id
    
    def display_personal_details(self):
        print(f"Name: {self.name}")
        print(f"Student ID: {self.student_id}")

# Parent Class 2: Attendance
class Attendance:
    def __init__(self, attendance):
        self.attendance = attendance
    
    def check_attendance(self):
        if self.attendance > 80:
            return True
        else:
            return False

# Child Class: Student (Multiple Inheritance from PersonalDetails and Attendance)
class Student(PersonalDetails, Attendance):
    def __init__(self, name, student_id, attendance):
        PersonalDetails.__init__(self, name, student_id)  # Initialize PersonalDetails
        Attendance.__init__(self, attendance)  # Initialize Attendance
    
    def display_eligibility(self):
        self.display_personal_details()  # Display personal details
        if self.check_attendance():  # Check if the student is eligible based on attendance
            print("Eligibility: Eligible for the next module.")
        else:
            print("Eligibility: Not eligible for the next module.")

# Example usage:
# Get student details
name = input("Enter student's name: ")
student_id = input("Enter student's ID: ")
attendance = float(input("Enter attendance percentage: "))

# Create a Student object
student = Student(name, student_id, attendance)

# Display eligibility
student.display_eligibility()
```

```

### OUTPUT
![image](https://github.com/user-attachments/assets/20c4ebb3-746f-40c5-845f-3e6bd8408604)



### RESULT
thus the program is executed successfully




