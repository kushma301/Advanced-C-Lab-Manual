

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
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *temp;
    temp=head;
    while(temp!=NULL)
    {
        printf("%.3f\n",temp->data);
        temp=temp->next;
    }
}
```

Output:

<img width="714" height="450" alt="511673344-d432ee0c-cbe7-4681-a4b0-712b0040b9e0" src="https://github.com/user-attachments/assets/12087162-8962-4f4c-9357-b72d047b68ba" />


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING 
LINKED LIST.
Aim:
To write a C program to pop an element from the given stack using liked list.

Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
Program:
```
struct Node   
{  
float data;  
struct Node *next;  
}*head;  
void pop()
{
    struct Node*temp;
    if(head==NULL)
    {
        printf("stack is empty\n");
    }
    else
    {
        temp=head;
        head=temp->next;
        free(temp);
    }
    
}
```

Output:

<img width="1174" height="634" alt="511673363-f9ed5f74-abe1-42f0-80c7-e86e66c0f0f8" src="https://github.com/user-attachments/assets/1044fdf0-91ba-41e3-9d87-b8f623200d24" />



Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
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
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    struct Node *temp;
    temp=front;
    if(rear==NULL)
    {
        printf("queue is empty");
    }
    else
    {
        while(temp!=NULL)
        {
            printf("%d\n",temp->data);
            temp=temp->next;
        }
    }
}
```

Output:

<img width="647" height="545" alt="511673379-5bcbbfba-8406-4c18-a76e-91bbda589b82" src="https://github.com/user-attachments/assets/c1c7ae95-ab5f-4b01-b327-acf7c75a8d0c" />

Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
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
struct Node
{
 int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data)
{
    struct Node *newnode;
    newnode=(struct Node*)malloc(sizeof(struct Node));
    newnode->data=data;
    newnode->next=NULL;
    if(front==NULL && rear==NULL)
    {
        front=rear=newnode;
    }
    else
    {
        rear->next=newnode;
        rear=newnode;
    }
}
```

Output:

<img width="859" height="546" alt="511673407-ecd69c27-2b64-42ec-ab38-1f7b42304a26" src="https://github.com/user-attachments/assets/1e506f1e-59e3-44af-805d-8773dc6f84d6" />


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.


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
struct Node
{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%d",front->data);
}
```

Output:

<img width="500" height="562" alt="511673438-cb3e513e-2ea2-4c09-a816-7e30cfb5f462" src="https://github.com/user-attachments/assets/e32dfe64-1e2e-4f48-aea1-71d76cae5339" />


Result:
Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


