#Main gradebook which stores names and grades as key and value
gradebook = {}

#Function that adds student to gradebook
def add_student(name):
    #Checks if student key already exists
    if name not in gradebook:
        gradebook[name] = []
    else:
        print(f"Student {name} already exists, try another name!")

#Adds a student and grade to the gradebook
def add_grade (name, grade):
    if name in gradebook and grade <= 100:
        gradebook[name].append(grade)
    else:
        print(f"Student {name} doesn't exist")

#Calculates average of the list of grades for a student
def calc_average(name):
    #If name exists in gradebook and has grades paired to it,
    #calculates average and returns it
    if name in gradebook and len(gradebook[name]) > 0:
        return sum(gradebook[name]) / len(gradebook[name])
    else:
        print(f"No grades available for {name}")

#Checks if student is passing or failing
def check_pass(name):
    average = calc_average(name)
    if average >= 60:
        return True
    else: 
        return False

#Displays each student's grades, average, and pass status
def display_gradebook():
    for student, grades, in gradebook.items():
        average = calc_average(student)
        #Creates bool variable and stores pass status
        if check_pass(student):
            status = "Pass"
        else:
            status = "Fail"
        
        #Prints student name, their grades, the average,
        #and their pass status
        print(f"Student: {student}, Grades: {grades}, Average: {average:.2f}, Status: {status}")

#Adding students
add_student("Tony Tonoyan")
add_student("Faris")
add_student ("Thanos")

#Adding grades
add_grade("Tony Tonoyan", 76)
add_grade("Thanos", 94)
add_grade("Thanos", 63)
add_grade("Faris", 96)

display_gradebook()
