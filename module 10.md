## EXP NO:4(a) C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

```
struct Node{
    float data; 
    struct Node *next;
}*head;

void search(float data)
{
    struct Node *ptr;
    float item=data;
    int i=0,flag;
    ptr = head;
    if(ptr == NULL)
    {
    printf("\nEmpty List\n");
    }
    else
    {
        while (ptr!=NULL)
        {
            if(ptr->data == item)
            {
                printf("item %.2f found at location %d",item,i+1);
                flag=0;
            }
            i++;
            ptr = ptr -> next;
        }
        if(flag!=0)
        {
            printf("Item not found\n");
        }
    }
 
}


```

Output:


![image](https://github.com/user-attachments/assets/7a70a340-a007-4ea8-96ff-95fdb7e8efcc)



Result:
Thus, the program to search a given element in the given linked list is verified successfully.


 
## EXP NO:4(b)  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

```
struct Node{
    int data; 
    struct Node *next;
}*head;
void insert(int data)
{
    struct Node *x=(struct Node *)malloc(sizeof(struct Node));
    struct Node *t=head;
    x->data=data;
    x->next=NULL;
    if(t==NULL)
    {
        head=x;
        return;
    }
    else
    {
        while(t->next!=NULL)
        {
            t=t->next;
        }
        t->next=x;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/757c5571-00f8-462d-98f5-4de48617136b)

Result:
Thus, the program to insert a node in a linked list is verified successfully.


 
## EXP NO:4(c) C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void display()
{
    struct Node *temp=head;
    if(head==NULL)
    {
        printf("List is empty\n");
    }
    else
    {
        while(temp!=NULL)
        {
            printf("%.2f\n",temp->data);
            temp=temp->next;
        }
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/dfec3e38-7cbc-464c-9513-accb4cb5aa9e)



Result:
Thus, the program to traverse a doubly linked list is verified successfully. 



## EXP NO:4(d) C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
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

struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;
void insert(float data)
{
   struct Node *x = (struct Node *) malloc(sizeof(struct Node));
   struct Node *ptr=head;
   x->data=data;
   x->next=NULL;
   if(ptr == NULL)
   {
       head=x;
       return;
   }
   else
   {
       while(ptr->next!=NULL)
       {
           ptr=ptr->next;
       }
       ptr->next=x;
       x->next=NULL;
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/423c9c66-c92e-4332-bb55-50be0051cd65)


Result:
Thus, the program to insert an element in doubly linked list is verified successfully.



## EXP NO:4(e) C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




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
struct Node{
    char data; 
    struct Node *next;
}*head;
void delete()
{
    if(head==NULL){
        printf("List is empty\n");
        return;
    }
    else if(head->next==NULL){
        head=NULL;
        free(head);
        printf("Node deleted from the begining ...\n");
    }
    else{
        struct Node *ptr;
        ptr=head;
        head=head->next;
        free(ptr);
        printf("Node deleted from the begining ...\n");
    }
}

```
Output:



![437484154-56157a63-71cf-45e1-bdda-d7aa23a09278](https://github.com/user-attachments/assets/3e05bd37-ad00-4475-acf1-1e3739505054)




Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





