## NAME :- PRABHAKARAN P
## REGISTER NUMBER :- 212224040236

## EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.

## Aim:
To write a C program to search a given element in the given linked list.

## Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
## Program:

```
struct Node {
    int data;
    struct Node *next;
} *head = NULL;

void search(int item) {
    struct Node *temp = head;
    int pos = 1, found = 0;
    while (temp != NULL) {
        if (temp->data == item) {
            printf("item %d found at location %d\n", item, pos);
            found = 1;
            break;
        }
        temp = temp->next;
        pos++;
    }
    if (!found) {
        printf("Item not found\n");
    }
}

```

## Output:

<img width="754" height="491" alt="image" src="https://github.com/user-attachments/assets/cd0bd745-13d0-4f2d-84e5-c83a00fb424e" />




## Result:
Thus, the program to search a given element in the given linked list is verified successfully.

--------------------------------------------------------------------------------
 
## EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.

## Aim:
To write a C program to insert a node in a linked list.
## Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
## Program:
```
struct Node {
    int data;
    struct Node *next;
} *head = NULL;

void insert(int value) {
    struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;

    if (head == NULL) 
    {
        head = newNode;
    } 
    else 
    {
        struct Node *temp = head;
        while (temp->next != NULL) 
        {
            temp = temp->next;
        }
        temp->next = newNode;
    }
}
```
## Output:

<img width="632" height="517" alt="image" src="https://github.com/user-attachments/assets/b09205a5-cb44-4849-a08d-18512c8aaffd" />



 
## Result:
Thus, the program to insert a node in a linked list is verified successfully.

----------------------------------------------------------------------------------------
 
## EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST

## Aim:
To write a C program to traverse a doubly linked list.

## Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
## Program:

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;

void display()
{
    struct Node* temp=head;
    while(temp!=NULL)
    {
        printf("%d\n",temp->data);
        temp=temp->next;
    }
    
}
```

## Output:

<img width="656" height="502" alt="image" src="https://github.com/user-attachments/assets/72b9d5fb-db57-4940-8f32-a4f2470fbb1d" />




## Result:
Thus, the program to traverse a doubly linked list is verified successfully. 

-------------------------------------------------------------------------------------------

## EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST

## Aim:
To write a C program to insert an element in doubly linked list

## Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
## Program:
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
## Output:

 <img width="889" height="601" alt="437765279-6e066425-507b-48de-977c-42f083b2a0f3" src="https://github.com/user-attachments/assets/f6712eca-3c7c-4b7e-be48-22ed344aee34" />




## Result:
Thus, the program to insert an element in doubly linked list is verified successfully.

----------------------------------------------------------------------------------------------


## EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

## Aim:
To write a C function that deletes a given element from a linked list.

## Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


## Program:
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
## Output:

<img width="882" height="842" alt="437765374-c69c2e34-30ff-492c-a9f4-89c8e8f76e04" src="https://github.com/user-attachments/assets/60827c6b-30a2-4daa-811d-43b8c6c0992d" />




## Result:
Thus, the function that deletes a given element from a linked list is verified successfully.

------------------------------------------------------------------------------------------------------



