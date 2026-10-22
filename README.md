# Student Grade Calculator

A command-line Python program that takes a student's name and marks (0-100), validates the input, assigns a letter grade, and prints an encouraging message.

## Features

- Input validation: rejects non-numeric input and marks outside 0-100
- Letter grades: A, B, C, D, F
- An encouraging message for each grade
- Accepts decimal marks (e.g. 89.5)

## Requirements

- Python 3.8 or newer
- No external libraries

## Setup and Run

1. Clone the repository:
   
   git clone https://github.com/medha-mishra/<repo-name>.git
   
2. Enter the project folder:
   
   grade_calculator.py
   
3. Run the program:
   
   python grade_calculator.py
   

## Grading Logic

| Marks   | Grade | Message                                          |
|---------|-------|--------------------------------------------------|
| 90-100  | A     | Outstanding! Keep up the excellent work!         |
| 80-89   | B     | Very Good! Keep it up!                           |
| 70-79   | C     | Good job! Push a little harder next time.        |
| 60-69   | D     | Passed, but there's room to grow.                |
| 0-59    | F     | Don't give up. Review the topics and retry.      |

The program checks each band with >= against the lower bound, so a mark of 89.9 falls into B.

## Functions

- get_grade(marks): Uses if-elif-else to return the letter grade and message for a mark.
- get_valid_marks(): Repeatedly asks for input inside a while True loop until the user enters a number from 0 to 100. Invalid input is rejected and the user is asked again.
- main(): Asks for the student's name, calls get_valid_marks() and get_grade(), then prints the result.

## Sample Run


Enter student name: Priya
Enter marks (0-100): 92

RESULT FOR PRIYA:
Marks: 92/100
Grade: A
Message: Outstanding! Keep up the excellent work!


## Testing

Test cases are in [test_cases.txt](test_cases.txt).

| Input  | Expected result        | Actual result |
|--------|------------------------|---------------|
| 85     | B                      |               |
| 90     | A                      |               |
| 89.9   | B                      |               |
| 70     | C                      |               |
| 60     | D                      |               |
| 59.9   | F                      |               |
| 0      | F                      |               |
| 100    | A                      |               |
| 101    | Rejected, asks again   |               |
| abc    | Rejected, asks again   |               |

