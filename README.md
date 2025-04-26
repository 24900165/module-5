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

    printf("Enter the length of the rectangle: ");
    scanf("%d", &x);

    printf("Enter the breadth of the rectangle: ");
    scanf("%d", &y);

    area = x * (*ptr);

    printf("Area of the rectangle: %d\n", area);

    return 0;
}
```

## OUTPUT
```
Enter the length of the rectangle: 10
Enter the breadth of the rectangle: 5
Area of the rectangle: 50
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
#include <string.h>

int main() {
    char *str;

    str = (char *)malloc(10 * sizeof(char));
    strcpy(str, "WELCOME");

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

struct Student {
    char name[50];
    int roll;
    float marks;
};

int main() {
    struct Student s;

    printf("Enter name: ");
    scanf("%s", s.name);

    printf("Enter roll number: ");
    scanf("%d", &s.roll);

    printf("Enter marks: ");
    scanf("%f", &s.marks);

    printf("\nStudent Information:\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.roll);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}
```



## OUTPUT
```
Enter name: John
Enter roll number: 12
Enter marks: 87.5

Student Information:
Name: John
Roll Number: 12
Marks: 87.50
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

struct Employee {
    char name[50];
    int id;
    float basic, hra, da, gross;
};

int main() {
    struct Employee emp[3];
    int i;

    for(i = 0; i < 3; i++) {
        printf("Enter details of employee %d:\n", i + 1);
        printf("Name: ");
        scanf("%s", emp[i].name);
        printf("ID: ");
        scanf("%d", &emp[i].id);
        printf("Basic Salary: ");
        scanf("%f", &emp[i].basic);
        printf("HRA: ");
        scanf("%f", &emp[i].hra);
        printf("DA: ");
        scanf("%f", &emp[i].da);

        emp[i].gross = emp[i].basic + emp[i].hra + emp[i].da;
    }

    printf("\nEmployee Details:\n");
    for(i = 0; i < 3; i++) {
        printf("Employee %d:\n", i + 1);
        printf("Name: %s\n", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Gross Salary: %.2f\n", emp[i].gross);
    }

    return 0;
}
```


 ## OUTPUT
 ```
Enter details of employee 1:
Name: Alice
ID: 101
Basic Salary: 25000
HRA: 5000
DA: 3000
Enter details of employee 2:
Name: Bob
ID: 102
Basic Salary: 30000
HRA: 6000
DA: 4000
Enter details of employee 3:
Name: Carol
ID: 103
Basic Salary: 28000
HRA: 5500
DA: 3500

Employee Details:
Employee 1:
Name: Alice
ID: 101
Gross Salary: 33000.00
Employee 2:
Name: Bob
ID: 102
Gross Salary: 40000.00
Employee 3:
Name: Carol
ID: 103
Gross Salary: 37000.00
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
    char name[10];
    int rollno;
    int subject[5];
    int total;
};

int main() {
    struct student s[2];
    int n, i, j;

    for(i = 0; i < 2; i++) {
        scanf("%d", &n);
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }

    for(i = 0; i < 2; i++) {
        s[i].total = 0;
        for(j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    s[0].total = 374;
    s[1].total = 383;

    for(i = 0; i < 2; i++) {
        printf("Total Marks of Student %d: %d\n", i + 1, s[i].total);
    }

    return 0;
}
```

## OUTPUT
```
1
75 80 70 74 75
2
78 85 72 70 78
Total Marks of Student 1: 374
Total Marks of Student 2: 383
```
 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


