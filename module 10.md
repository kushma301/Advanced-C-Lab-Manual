EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:
```
#include<stdio.h>
struct person{
    int x;
    char y[20];
};
int main()
{
   struct person p;
   printf("Enter age: ");
   scanf("%d",&p.x);
   printf("Enter Name: ");
   scanf("%s",p.y);
   printf("Age:%d\n",p.x);
   printf("Name:%s\n",p.y);
   
   if(p.x>6)
   {
       printf("eligibility:yes");
   }
   else
   {
       printf("eligibility:no");
   }
}
```

Output:

<img width="420" height="217" alt="437369883-e171cb54-885c-4994-8b16-11e4a6731983" src="https://github.com/user-attachments/assets/98498908-7440-4790-9ac6-b4be05f4e545" />

Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:
```
#include <stdio.h>

struct Result {
    int sum;
};
struct Result calculate(int a, int b) {
    struct Result res;
    res.sum = a + b;
    return res;
}
int main() {
    int num1, num2;
    struct Result result;
    scanf("%d %d", &num1, &num2);
    result = calculate(num1, num2);    
    printf("%d\n", result.sum);
    return 0;
}
```

Output:

<img width="407" height="308" alt="437373347-1a06ac13-bb32-4a4b-b2c9-ef6f24b5ba14" src="https://github.com/user-attachments/assets/ef1d3c64-9caa-49b0-a1bb-d84b8f12a71f" />

Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:
```
#include <stdio.h>
int main()
{
    char fn[100];
    scanf("%s",fn);
    FILE *file=fopen(fn,"w");
    printf("%s File Created Successfully\n",fn);
    printf("%s File Opened\n",fn);
    fclose(file);
    printf("%s File Closed\n",fn);
}
```

Output:

<img width="991" height="388" alt="437373966-7ed35802-57df-473e-a516-2810e8998ace" src="https://github.com/user-attachments/assets/75a500df-e2f4-482a-8585-b9f20707369d" />

Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:
```
#include <stdio.h>
int main()
{
    char fn[100];
    scanf("%s",fn);
    
    FILE *file=fopen(fn,"w");
    printf("%s Opened\n",fn);
    
    int n;
    char wd[100];
    scanf("%d",&n);
    for(int i=0;i<n;i++)
    {
        scanf("%s",wd);
        fputs(wd,file);
    }
    printf("Data added Successfully");
}
```

Output:

<img width="777" height="363" alt="437374228-6055b7d6-0636-464f-98d4-7ac0d3713dad" src="https://github.com/user-attachments/assets/c0e682f1-2165-4921-a51a-15438efac16f" />

Result:
Thus, the program to insert an element in doubly linked list is verified successfully.



EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
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


Program:
```
#include <stdio.h>
#include <stdlib.h>
struct Subject
{
    char name[20];
    int marks;
};
int main()
{
    int i,n;
    scanf("%d",&n);
    struct Subject *s = (struct Subject *)malloc(n*sizeof(struct Subject));
    if(s==NULL)
    {
        printf("Memory Alocation Failed\n");
        return 1;
    }
    for(i=0;i<n;i++)
    {
        scanf("%s %d",s[i].name,&s[i].marks);
    }
    for(i=0;i<n;i++)
    {
        printf("%s  %d\n",s[i].name,s[i].marks);
    }
    
    free (s);
    
    return 0;
}
```

Output:

<img width="359" height="271" alt="437295856-297a272e-1888-4dcc-a7ce-9b03c9c2bac3" src="https://github.com/user-attachments/assets/9b6bad5e-a33d-4079-81b0-4a6b779271de" />

Result:
Thus, the function that deletes a given element from a linked list is verified successfully.



