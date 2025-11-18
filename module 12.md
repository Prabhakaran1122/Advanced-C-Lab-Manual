## NAME :- PRABHAKARAN P
## REGISTER NUMBER :- 212224040236

## EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.

## Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
## Program:
```
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void display()  
{ 
    struct Node *current=head;
    while(current!=NULL)
    {
        printf("%.2f\n",current->data);
        current=current->next;
    }
}
```
## Output:

<img width="400" height="447" alt="437718622-4affefe0-601f-4667-93d1-24fef0d562a0" src="https://github.com/user-attachments/assets/850c7ed0-8d7b-4879-b003-05563fa121cf" />




## Result:
Thus, the program to display stack elements using linked list is verified successfully. 

-----------------------------------------------------------------------------------------------

## EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.

## Aim:
To write a C program to pop an element from the given stack using liked list.

## Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
## Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void pop()  
{ 
    if(head!=0)
    {
        head=head->next;
    }
    else
    {
        printf("stack is empty");
    }
}
```

## Output:

<img width="1062" height="596" alt="437719012-484e2315-997c-47d8-8d91-22b357b358ff" src="https://github.com/user-attachments/assets/f5d17912-e0fb-4249-bf58-53fabcb157d8" />



## Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

-------------------------------------------------------------------------
 
## EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

## Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
 struct Node *current=front;
 if(current==NULL)
 {
     printf("queue is empty");
 }
 else
 {
 printf("queue elements:\n");
 while(current!=NULL)
{
    
   printf("%c\n",current->data);
   current=current->next;
}
}
}

```
## Output:
<img width="528" height="506" alt="437719415-80b38f3e-e811-4373-b32e-c6de48dcc2ea" src="https://github.com/user-attachments/assets/3bd6b98a-c14a-4118-af46-88101de48921" />



## Result:
Thus, the program to display queue elements using linked list is verified successfully.

--------------------------------------------------------------------------------------------------
 
## EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

## Aim:
To write a C program to insert elements in queue using linked list

## Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
```
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *current = (struct Node*)malloc(sizeof(struct Node));
    current->data = data;
    current->next = NULL;

    if (front == NULL)
    {
        front = rear = current;
    }
    else
    {
        rear->next = current;
        rear = current;
    }
}

```
## Output:

<img width="542" height="505" alt="437719745-43a754e0-5287-4f95-8200-43543b44c720" src="https://github.com/user-attachments/assets/99531afc-8cf1-449c-9f58-4fde5213141b" />

## Result:
Thus, the program to insert elements in queue using linked list is verified successfully.

------------------------------------------------------------------------------------

## EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


## Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

## Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

## Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    if(front==NULL)
    {
        printf("queue is empty");
    }
    else
    {
        printf("%.2f",front->data);
    }
}
```



## Output:

<img width="431" height="527" alt="437720169-4d5fed2a-fbf5-4eaf-b8f6-efa6f78c308d" src="https://github.com/user-attachments/assets/2d543fab-ae16-4c3d-b030-cb9d65761e58" />



## Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


