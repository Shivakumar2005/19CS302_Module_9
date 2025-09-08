# EX 43 C program to Write a function to display queue elements using array.
## DATE:08/09/2025
## AIM:
To Write a function to display queue elements using array.

## Algorithm
1. Start the program and declare queue array with front and rear.
2. Define enqueue function to insert elements into the queue.
3. Define display function to print all elements from front to rear.
4. In main, insert some elements into the queue. 
5. Call display function to show all queue elements.  

## Program:
#include <stdio.h>
#define SIZE 5

int queue[SIZE], front = -1, rear = -1;

void enqueue(int value) {
    if(rear == SIZE - 1)
        printf("Queue Overflow\n");
    else {
        if(front == -1) front = 0;
        queue[++rear] = value;
    }
}

void display() {
    if(front == -1)
        printf("Queue is empty\n");
    else {
        printf("Queue elements: ");
        for(int i = front; i <= rear; i++)
            printf("%d ", queue[i]);
        printf("\n");
    }
}

int main() {
    enqueue(10);
    enqueue(20);
    enqueue(30);
    display();
    return 0;
}


## Output:

<img width="1268" height="673" alt="image" src="https://github.com/user-attachments/assets/9339c774-6d0a-4dac-96a9-5f7a24a34c5b" />


## Result:
Thus the program was executed and the output was verified successfully.
