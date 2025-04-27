## EXP NO:3(a) C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

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
#include <stdio.h>
int stack[40], top, i;

void display() {
    for (i = top; i >= 0; i--) {
        printf("%d\n", stack[i]);
    }
}


int main() {
    int n;
    scanf("%d", &n);

    top = -1; // Initialize top

    for (i = 0; i < n; i++) {
        int value;
        printf("Enter element %d: ", i + 1);
        scanf("%d", &value);
        top++;
        stack[top] = value;
    }

    printf("\nStack elements are:\n");
    display();

    return 0;
}



```

Output:

![image](https://github.com/user-attachments/assets/097b10f2-1a4a-4906-b865-17059660b8cf)





Result:
Thus, the program to display stack elements using an array is verified successfully.
 

## EXP NO:3(b)  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```


int size=3,top=1;
float stack[40];
void push (float data)
{
    if (top==size-1 )
    {
        printf("stack is full\n");
        
    }
    else
    {
        top ++;
        stack[top] = data;
        
    }
}

```

Output:

![image](https://github.com/user-attachments/assets/267834a1-f8ec-4a31-bdcf-2dfbccf97c88)





Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
## EXP NO:3(c) C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
int queue[50], rear, front,i;
void display()
{
    if(front==-1)
    {
        printf("No elements to display");
        
    }
    else
    {
        for(i=front;i<=rear;i++)
        {
            printf("%d ",queue[i]);
            
        }
        
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/5e3d11cd-f4f8-4e83-afff-85d24f32b309)



Result:
Thus, the program to display queue elements using array is verified successfully.


 
## EXP NO:3(d) C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

```
int size=4, rear=-1, front=-1; 
float queue[50];
void enqueue(float data)
{
    if(rear<size)
    {
        if(front==-1)
        {
            front=0;
        }
        rear=rear+1;
        queue[rear]=data;
        
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/e3b2d29a-c43a-4453-afd7-248efd0505af)


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
## EXP NO:3(e) C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



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
    if(front==-1&&rear==-1)
    printf("Queue Underflow.");
    else if(front==rear)
    front=rear=-1;
    else{
        front=front+1;
    }
}
```

Output:

![437313102-ad6e1570-a13e-4f1a-acea-5d4ae559923d](https://github.com/user-attachments/assets/fc29c165-a15d-4298-a08b-b51bad81e5ce)



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
