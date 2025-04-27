

## EXP NO 6(a): C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
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
          int data;
          struct Node *next;
          }*head;
          void display()
          {
          struct Node *p; p=head; while(p!=NULL)
          {
          printf("%d\n",p->data); p=p->next;
          }
          }
```

Output:

![437513316-a8a1af1d-222b-440a-ba6c-3ca31023584f](https://github.com/user-attachments/assets/8e7c86f6-de86-4d9e-8bd5-e1268cd23675)


Result:
Thus, the program to display stack elements using linked list is verified successfully. 



## EXP.NO 6(b): C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
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
          int data;
          struct Node *next;
          }*head; void pop()
          {
          if(head==NULL)
          {
          printf("stack is empty");
          }
          else
          {
          head=head->next;
          }
          }
```

Output:

![437513433-3068daed-dfb2-45da-b97e-981059a2fdc6](https://github.com/user-attachments/assets/9f40e24c-5d89-44b2-8161-6e53fa660e4f)



Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
## EXP NO:6(c) C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
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
                   char data;
                   struct Node *next;
                   }*front=NULL,*rear=NULL; 
                   void display()
                   {
                   if(front==NULL)
                   {
                   printf("queue is empty");
                   }
                   else
                   {
                   printf("queue elements:\n"); 
                   while(front!=NULL)
                   {
                   printf("%c\n",front->data); 
                   front=front->next;
                   }
                   }
                   }
```
Output:

![437514095-af82331b-ca27-4037-9bc1-a7c4c48afd9f](https://github.com/user-attachments/assets/624db7d4-8e3f-41e9-a56f-74f42f3d0789)



Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
## EXP NO:6(d) C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

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
              struct Node *p=(struct Node*)malloc(sizeof(struct Node)); 
              p->data=data;
              p->next=NULL; 
              if(front==NULL)
              {
              front=rear=p;
              }
              else
              {
              rear->next=p; 
              rear=p;
              }
              }
```

Output:

![437514348-6cc3b8d2-b580-4f84-ba41-ba20f0efe01d](https://github.com/user-attachments/assets/87f3c88a-47ae-46d1-bc2f-27daec3d2691)


Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



## EXP NO:6(e) C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


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
                 char data;
                 struct Node *next;
              }*front=NULL,*rear=NULL;
              void peek()
              {
              printf("%c",front->data);
              }
```

Output:

![437514636-a6143772-4fe6-4d53-8f28-eb071c67fc71](https://github.com/user-attachments/assets/06d87702-a376-4cff-b166-3ba013ad0591)




Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


