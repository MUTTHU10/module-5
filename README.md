# EX-26-AREA-AND-CIRCLE-USING- POINTER
## AIM
write a C program to find area of a circle and perimeter of the circle for the radius 100 using pointer.

## ALGORITHM
1.	Start the program.
2.	Read the numbers.
3.	Calculate the area of circle using the formula area=(3.14)*(r)*(r) and perimeter=(2)*(3.14)*(r)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
int main()
{
    float rad;
    float *ptr=&rad;
    scanf("%f",ptr);
    float Area=3.14*(*ptr)*(*ptr);
    float Perimeter=2*3.14*(*ptr);
    printf("Area of Circle = %.2f\n",Area);
    printf("Perimeter of Circle = %.2f",Perimeter);
}
```

## OUTPUT
<img width="950" height="345" alt="Screenshot 2025-10-22 083930" src="https://github.com/user-attachments/assets/23cf3dd9-a8c9-4e5e-a31b-f6c8eb5aa173" />
       	


## RESULT
Thus the program to find area and perimeter of circle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
Write a C program to add value 20.21,32.67 to list which already have 12.33,67.44,89.55  in that  using malloc() and print that value.

## ALGORITHM
1.	Start the program.
2.	Read a float variable.
3.	Allocate memory using malloc().
4.	Display the float values.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h>

#include<stdlib.h>

int main()

{

     float* ptr;
    

     ptr = (float*)malloc( sizeof(float));

     ptr[0]=12.330000;
     ptr[1]=67.440000;
     ptr[2]=89.550000;
     ptr[3]= 20.210000;
     ptr[4]=32.670000;
     for(int i=0;i<5;i++)

     printf("%.2f ",ptr[i]);

}

```
## OUTPUT

<img width="922" height="252" alt="Screenshot 2025-10-22 084311" src="https://github.com/user-attachments/assets/f8a6cd30-59a6-4e16-8ec3-5115a80fd0aa" />


## RESULT
Thus the program to add value 20.21,32.67 to list which already have 12.33,67.44,89.55  in that  using malloc() has been executed successfully.


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
struct students
{
    char name[100];
    int roll;
    float marks;
};
int main()
{
    printf("Displaying Information:\n");
    struct students student;
    scanf("%s %d %f",student.name,&student.roll,&student.marks);
    printf("Name: %s\nRoll number: %d\nMarks: %.1f",student.name,student.roll,student.marks);
}
```

## OUTPUT
<img width="894" height="326" alt="Screenshot 2025-10-22 084511" src="https://github.com/user-attachments/assets/74e8a5e9-c1b5-4770-9015-4d4ccc2bc5db" />


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EB-CALCULATION-BILL-USING-STRUCTURES

## AIM

Create a structure for eb calculation bill for 3 Customers(use customer no,prev reading & curre reading as input) using nested structure ( first 100 unit 2 Rs per unit ,101 to 200 rs.3 per unit and above 200 rs 5 per unit).



## ALGORITHM

1.	Start the program.
2.	Create an e_bill structure with prev_read, curr_read and units details as members.
3.	Using structure variable read the structure members.
4.	print the details of the employee.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdio.h>
struct e_bill
{
    int prev_read;
    int curr_read;
    int units;
};

struct electricity
{
    int cust_no;
    struct e_bill bill;
    float amount;
};

int main()
{
    struct electricity e[3];
for(int i=0; i<3; i++)
    {
scanf("%d %d %d", &e[i].cust_no, &e[i].bill.prev_read, &e[i].bill.curr_read);
    }
for(int i=0; i<3; i++)
    {
        e[i].bill.units = e[i].bill.curr_read - e[i].bill.prev_read;
        if(e[i].bill.units<= 100)
        {
            e[i].amount = e[i].bill.units * 2;
        }
        else if(e[i].bill.units> 100 && e[i].bill.units <=200)
        {
            e[i].amount = (100 * 2) + ((e[i].bill.units - 100) * 3);
        }
        else
        {
            e[i].amount = (100 * 2) + (100 * 3) + ((e[i].bill.units - 200) * 5);
        }
    }
printf("Details of the EB Customer\n");
for(int i=0; i<3; i++)
    {
printf("%d      %.2f\n", e[i].cust_no, e[i].amount);
    }
    return 0;
}

```

 ## OUTPUT
<img width="1229" height="600" alt="Screenshot 2025-10-22 084940" src="https://github.com/user-attachments/assets/5b3ed30c-96b5-49b3-a8dd-4a47ab479256" />

 

## RESULT

Thus the C program Create a structure for eb calculation bill for 3 Customers(use customer no,prev reading & curre reading as input) using nested structure ( first 100 unit 2 Rs per unit ,101 to 200 rs.3 per unit and above 200 rs 5 per unit)



# EX – 30 - POINTERS

## AIM
Write a C program to find character 'E' is vowel or consonant using pointer.

## ALGORITHM 

Step 1: Strat the program.
Step 2: Declare the character variable.
Step 3: Use pointer to point the address of the character variable.
Step 4: check whether the given character is vowel or not using if condition.
Step 5: If the given condition is true, then print the given character is vowel.
Step 6: Otherwise, print the given character is not vowel.
Step 7: End the program.

## PROGRAM
```
#include <stdio.h>
int main()
{
    char ch;
    char *ptr=&ch;
    scanf("%c",ptr);
    if (*ptr=='A'||*ptr=='E'||*ptr=='I'||*ptr=='O'||*ptr=='U'||*ptr=='a'||*ptr=='e'||*ptr=='i'||*ptr=='o'||*ptr=='u')
    {
        printf("%c is Vowel.",*ptr);
    }
    else
    {
        printf("%c is consonant.",*ptr);
    }
}
```

## OUTPUT
<img width="817" height="291" alt="Screenshot 2025-10-22 090121" src="https://github.com/user-attachments/assets/8dcb729a-4e22-46fd-9b07-9491a15a6339" />

 

## RESULT

Thus the C program to check whether the given character is vowel using pointer has been executed successfully.
	


