num_students=int(input("Enter number of students"))
grades=[]

for i in range(num_students):
    name=input("Enter student name: ")


    grade=float(input("Enter student grade: "))
    if 0 <= grade <= 100:
        break
    else:
        print("Invalid grade! Enter a grade between 0 and 100.")

    num_students += 1

    grades.append(grade)

    print("Student Name: ", name)
    print("Student Grade: ", grade)

total=sum(grades)
average=total/num_students
print("Total Grade: ", total)
print("Average Grade: ", average)
print("Student Name: ", name,"Student Grade: ", grade,"Average Grade: ", average)
num_students=int(input("Enter number of students"))
subjects=['Maths','English','Science']
students=[]




for i in range(num_students):
    print("\nStudent", i + 1)
    name=input("Enter student name: ")
    grades = []
    for subject in subjects:
        grade = float(input("Enter " + subject + " grade: "))
        grades.append(grade)

    print("Student Name: ", name)
    print("Student Grade: ", grade)
student=(grades,name)
students.append(student)
print(students)
print('Student averages')
for name, grades in students:
    average = sum(grades) / len(grades)

    print(name, "Average:", round(average, 2))
for i in range(len(subjects)):
    subject_grades = []

    for name, grades in students:
        subject_grades.append(grades[i])

    highest = max(subject_grades)
    lowest = min(subject_grades)

    print(subjects[i], "- Highest:", highest, "Lowest:", lowest)
students={}
num_students=int(input('Enter number of students:'))

for i in range(num_students):
    name=input("Enter student name: ")
    math=float(input("Enter math grade: "))
    english=float(input("Enter english grade: "))
    science=float(input("Enter science grade: "))

    students[name]={
        "math":math,
        "english":english,
        "science":science
}
#Adding new students
print('Add New Students:')
name=input("Enter student name: ")
math=float(input("Enter math grade: "))
english=float(input("Enter english grade: "))
science=float(input("Enter science grade: "))

students[name]={
        "math":math,
        "english":english,
        "science":science
}
print(students)

#Updating existing student records
print('Update Students:')
name=input("Enter student name: ")

if name in students:
    math = float(input("Enter math grade: "))
    english = float(input("Enter english grade: "))
    science = float(input("Enter science grade: "))

    students[name] = {
        "math": math,
        "english": english,
        "science": science
    }
    print('Update Successful')
else:
        print("Student not found.")

#Deleting Students
print('Delete Students:')
name=input("Enter student name: ")

if name in students:
    del students[name]
    print('Delete Successful')
else:
    print("Student not found.")
#Subject as a key
subject_grades={}
subjects=['math', 'english', 'science']

for subject in subjects:
    subject_grades[subject]=[]
for name in students:
    for subject in subjects:
        subject_grades[subject].append(students[name][subject])

#View all grades for subject
print('View all grades for subject')
subject=input("Enter subject name: ")
if subject in subject_grades:
    print(subject,'Grades:')
    for name in students:
        print(name, ":", students[name][subject])
else: print("Student not found.")
