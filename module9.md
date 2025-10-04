## NAME :- PRABHAKARAN P
## REGISTER NUMBER :- 212224040236

EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:

To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents

Program:
```
float stack[100];
int top;

void display()
{
    if (top == -1)
{
        printf("Stack is empty\n");
    } else {
        for (int i = top; i >= 0; i--) {
            printf("%.1f\n", stack[i]);
        }
    }
}

```

Output:

<img width="725" height="535" alt="image" src="https://github.com/user-attachments/assets/ec3618bb-1f1c-4a4f-8ec4-19e1a4df12ab" />

Result:
Thus, the program to display stack elements using an array is verified successfully.

 -----------------------------------------------------------------------------------


EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.

Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```
float stack[100];
int top;

void display()
{
    if (top == -1)
{
        printf("Stack is empty\n");
    } else {
        for (int i = top; i >= 0; i--) {
            printf("%.1f\n", stack[i]);
        }
    }
}

```

Output:

<img width="725" height="535" alt="image" src="https://github.com/user-attachments/assets/ec3618bb-1f1c-4a4f-8ec4-19e1a4df12ab" />

Result:
Thus, the program to push the given element in to a stack using array is verified successfully

-----------------------------------------------------------------------------------

 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.

Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
#include <stdio.h>

float queue[50];  
int rear = -1, front = -1, i;

void display()
{
    if (front == -1 || front > rear)
    {
        printf("No elements to display\n");
    }
    else
    {
        for (i = front; i <= rear; i++)
        {
            printf("%.1f\n", queue[i]); 
        }
    }
}

```

Output:

<img width="896" height="531" alt="image" src="https://github.com/user-attachments/assets/f519aea7-c479-4128-b8e1-1fbeb37536a8" />

Result:
Thus, the program to display queue elements using array is verified successfully.

-----------------------------------------------------------------------------------

 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.

Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

```
int rear,front,size=3;
int queue[50];
void enqueue(int data) 
{
    if (rear<size)
    {
        if(front==-1)
        front++;
        rear++;
        queue[rear]=data;
    }
 
}
```

Output:

<img width="1089" height="666" alt="image" src="https://github.com/user-attachments/assets/23698d08-c7c1-4b3d-9b06-7874c073e006" />

Result:
Thus, the program to insert elements in queue using array is verified successfully.


-----------------------------------------------------------------------------------

 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.

Program:

```
int front, rear;
void dequeue()
{
    if(front==-1||front>rear){
        printf("No elements to display");
    }
    else{
        front++;
    }
}
```


Output:

<img width="1082" height="858" alt="image" src="https://github.com/user-attachments/assets/ca964caa-37d8-45ab-a68d-351d623d0e57" />

Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.

---------------------------------------------------------------------------------

