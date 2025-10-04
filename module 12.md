## NAME :- PRABHAKARAN P
## REGISTER NUMBER :- 212224040236

EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.

Aim:
To write a C program to display stack elements using linked list.

Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node* next;
};

struct Node* head = NULL;

void display() {
    struct Node* p = head;
    if (p == NULL) {
        printf("Linked list is empty.\n");
        return;
    }
    printf("Linked list elements are:\n");
    while (p != NULL) {
        printf("%d ", p->data);
        p = p->next;
    }
    printf("\n");
}

int main() {
    struct Node* first = (struct Node*)malloc(sizeof(struct Node));
    struct Node* second = (struct Node*)malloc(sizeof(struct Node));
    struct Node* third = (struct Node*)malloc(sizeof(struct Node));

    first->data = 10;
    second->data = 20;
    third->data = 30;

    first->next = second;
    second->next = third;
    third->next = NULL;

    head = first;

    display();

    return 0;
}
```
Output:

<img width="817" height="307" alt="image" src="https://github.com/user-attachments/assets/51af9a80-e006-40b3-a6cb-3774f56d2c74" />



Result:
Thus, the program to display stack elements using linked list is verified successfully. 

-----------------------------------------------------------------------------------------------

EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.

Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node *next;
};

struct Node* pop(struct Node *head) {
    if(head == NULL) {
        printf("Stack is empty.\n");
        return NULL;
    }
    struct Node *temp = head;
    printf("Popped element: %d\n", head->data);
    head = head->next;
    free(temp);
    return head;
}

void display(struct Node *head) {
    if(head == NULL) {
        printf("Stack is empty.\n");
        return;
    }
    printf("Stack elements: ");
    while(head != NULL) {
        printf("%d ", head->data);
        head = head->next;
    }
    printf("\n");
}

struct Node* push(struct Node *head, int value) {
    struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = head;
    head = newNode;
    return head;
}

int main() {
    struct Node *head = NULL;
    head = push(head, 10);
    head = push(head, 20);
    head = push(head, 30);
    display(head);
    head = pop(head);
    display(head);
    return 0;
}

```

Output:

<img width="801" height="467" alt="image" src="https://github.com/user-attachments/assets/52c76bc8-50ef-4fe1-86bd-b8f325500168" />



Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

-------------------------------------------------------------------------
 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

Aim:
To write a C program to display queue elements using linked list.
Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node *next;
};

void display(struct Node *front) {
    if(front == NULL) {
        printf("Queue is empty.\n");
        return;
    }
    printf("Queue elements: ");
    while(front != NULL) {
        printf("%d ", front->data);
        front = front->next;
    }
    printf("\n");
}

struct Node* enqueue(struct Node *rear, int value, struct Node **front) {
    struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;
    if(*front == NULL) {
        *front = newNode;
        return newNode;
    }
    rear->next = newNode;
    return newNode;
}

int main() {
    struct Node *front = NULL, *rear = NULL;
    rear = enqueue(rear, 10, &front);
    rear = enqueue(rear, 20, &front);
    rear = enqueue(rear, 30, &front);
    display(front);
    return 0;
}

```
Output:

<img width="803" height="279" alt="image" src="https://github.com/user-attachments/assets/353930f2-d43a-4053-ae83-7eb9ee1f2720" />


Result:
Thus, the program to display queue elements using linked list is verified successfully.

--------------------------------------------------------------------------------------------------
 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:
To write a C program to insert elements in queue using linked list

Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node *next;
};

struct Node* enqueue(struct Node *rear, int value, struct Node **front) {
    struct Node *p = (struct Node*)malloc(sizeof(struct Node));
    p->data = value;
    p->next = NULL;
    if(*front == NULL) {
        *front = p;
        return p;
    }
    rear->next = p;
    return p;
}

void display(struct Node *front) {
    if(front == NULL) {
        printf("Queue is empty.\n");
        return;
    }
    printf("Queue elements: ");
    while(front != NULL) {
        printf("%d ", front->data);
        front = front->next;
    }
    printf("\n");
}

int main() {
    struct Node *front = NULL, *rear = NULL;
    rear = enqueue(rear, 10, &front);
    rear = enqueue(rear, 20, &front);
    rear = enqueue(rear, 30, &front);
    display(front);
    return 0;
}

```
Output:

<img width="793" height="267" alt="image" src="https://github.com/user-attachments/assets/6e74e6bf-1a6f-43fa-901e-cc4e03c488b0" />

Result:
Thus, the program to insert elements in queue using linked list is verified successfully.

------------------------------------------------------------------------------------

EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:
```
#include <stdio.h>
#include <stdlib.h>

struct Node {
    int data;
    struct Node *next;
};

int peek(struct Node *front) {
    if(front == NULL) {
        printf("Queue is empty.\n");
        return -1; // indicate error
    }
    return front->data;
}

struct Node* enqueue(struct Node *rear, int value, struct Node **front) {
    struct Node *p = (struct Node*)malloc(sizeof(struct Node));
    p->data = value;
    p->next = NULL;
    if(*front == NULL) {
        *front = p;
        return p;
    }
    rear->next = p;
    return p;
}

int main() {
    struct Node *front = NULL, *rear = NULL;
    rear = enqueue(rear, 10, &front);
    rear = enqueue(rear, 20, &front);
    rear = enqueue(rear, 30, &front);

    printf("Front element (peek) = %d\n", peek(front));
    return 0;
}

```



Output:

<img width="807" height="231" alt="image" src="https://github.com/user-attachments/assets/15949e0a-ca6c-4f17-9560-58eb370b718b" />



Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


