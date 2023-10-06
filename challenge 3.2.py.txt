"""Implement a function called sort_students that takes a list of student objects as input and sorts the list based on their CGPA(Cumulative Grade point Average) in descending order.Each student object has the following attributes:name(string),roll_number(sting),and cgpa(float).Test the function with different input List of students."""
class Student:

       def __init__(self, name, roll_number, cgpa):
              self.name = name
              self.roll_number = roll_number
              self.cgpa = cgpa

def sort_students(student_list):
       # print the list of students in descending order of CGPA
       sorted_students = sorted(student_list, key=lambda student: student.cgpa, reverse=True)
       # Syntax - lambda arg:exp
       return sorted_students

# Example usage
students = [ Student("jaiakash", "A123", 7.8),
          Student("Poovarasan", "A124", 8.9),
          Student("Madhuramutthu", "A125", 9.1),
          Student("Gokul", "A126", 9.9) ]

sorted_students = sort_students(students)
# Print the sorted list of students
for student in sorted_students:

   print("Name: {}, Roll Number: {}, CGPA: {}".format(student.name, student.roll_number,
student.cgpa))
