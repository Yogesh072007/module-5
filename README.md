# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int x, y, area;
    int *ptr = &y;
    scanf("%d %d", &x, &y);
    area = x * (*ptr);
    printf("Area of Rectangle = %d\n", area);
    return 0;
}
```

## OUTPUT
```
Area of Rectangle = 20
```
		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    char *str = (char *)malloc(10 * sizeof(char));
    str = "WELCOME";
    printf("%s\n", str);
    free(str);
    return 0;
}
```

## OUTPUT
```
WELCOME
```


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct student {
    char name[20];
    int roll;
    float marks;
};

int main() {
    struct student s;
    scanf("%s %d %f", s.name, &s.roll, &s.marks);
    printf("Name: %s\n", s.name);
    printf("Roll: %d\n", s.roll);
    printf("Marks: %.2f\n", s.marks);
    return 0;
}
```


## OUTPUT
```
John 101 85.5
```


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct employee {
    char name[20];
    int id;
    float basic, hra, da, gross;
};

int main() {
    struct employee e[3];
    for (int i = 0; i < 3; i++) {
        scanf("%s %d %f %f %f", e[i].name, &e[i].id, &e[i].basic, &e[i].hra, &e[i].da);
        e[i].gross = e[i].basic + e[i].hra + e[i].da;
    }
    for (int i = 0; i < 3; i++) {
        printf("Employee %d:\n", i + 1);
        printf("Name: %s\nID: %d\nGross Salary: %.2f\n", e[i].name, e[i].id, e[i].gross);
    }
    return 0;
}
```


 ## OUTPUT
```
Employee 1:  
Name: Ram  
ID: 101  
Gross Salary: 13500.00

Employee 2:  
Name: Sam  
ID: 102  
Gross Salary: 16500.00

Employee 3:  
Name: Raj  
ID: 103  
Gross Salary: 14900.00
```
 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

struct student {
    int subject[5];
    int total;
};

int main() {
    struct student s[2];
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }

    for (int i = 0; i < 2; i++) {
        s[i].total = 0;
        for (int j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    for (int i = 0; i < 2; i++) `{
        float avg = s[i].total / 5.0;
        printf("Student %d Total: %d, Average: %.2f\n", i + 1, s[i].total, avg);
    }
    return 0;
}
```


## OUTPUT
```
Student 1 Total: 400, Average: 80.00  
Student 2 Total: 360, Average: 72.00
```

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


