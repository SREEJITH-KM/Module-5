# Exp.No:22  
## Destructor

---

### AIM  
To create a Python class `Student` with a destructor.

---

### ALGORITHM

1. Begin the program.  
2. Define the `student` class.  
3. Inside the `student` class, define the `__init__` method (constructor) and the `__del__` method (destructor).  
4. Create an object `s2` of the `student` class. When the object `s2` is created, the `__init__` method is called, and its print statements are executed.  
5. Use the `del` statement to delete the object `s2`. This triggers the `__del__` method (destructor), and the respective print statements are executed.  
6. Terminate the program.

---

### PROGRAM

```
class Student:
    def __init__(self, name, roll_number):
        self.name = name
        self.roll_number = roll_number
        print(f"Student {self.name} with roll number {self.roll_number} has been created.")
    
    def __del__(self):
        print(f"Student {self.name} with roll number {self.roll_number} is being deleted.")
        
# Example usage:
student1 = Student("Alice", 101)
del student1  # This explicitly calls the destructor

```

### OUTPUT
![image](https://github.com/user-attachments/assets/8b5867e4-4c4b-4807-a760-605258581c62)



### RESULT
Thus the program is executed successfully
