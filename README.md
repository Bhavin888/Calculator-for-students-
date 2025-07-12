# Calculator-for-students-def calculate_grade(marks):
    if marks >= 90:
        return 'A+'
    elif marks >= 80:
        return 'A'
    elif marks >= 70:
        return 'B'
    elif marks >= 60:
        return 'C'
    elif marks >= 50:
        return 'D'
    else:
        return 'F'

def main():
    print("---- Student Grade Calculator ----")
    name = input("Enter student name: ")
    try:
        marks = float(input("Enter marks (out of 100): "))
        if marks < 0 or marks > 100:
            print("Invalid marks! Please enter a value between 0 and 100.")
        else:
            grade = calculate_grade(marks)
            print(f"Student: {name}")
            print(f"Marks: {marks}")
            print(f"Grade: {grade}")
    except ValueError:
        print("Invalid input! Please enter numeric marks.")

if __name__ == "__main__":
    main()