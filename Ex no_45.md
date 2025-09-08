# EX 45 C program that implements a queue using an array, and performs insertion (enqueue) and display operations.
## DATE:08/09/2025
## AIM:
To write a C program that implements a queue using an array, and performs insertion (enqueue) and display operations. 

## Algorithm
1. Start the program and declare queue array with front and rear initialized to -1.
2. Define enqueue function to insert an element into the queue.
3. Check for overflow before inserting an element.
4. Define display function to print all elements from front to rear. 
5. Call enqueue and display functions in main to demonstrate queue operations.  

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

<img width="1457" height="666" alt="image" src="https://github.com/user-attachments/assets/0bce2315-f9f5-421e-b405-c5c8996b12d4" />


## Result:
Thus the program was executed and the output was verified successfully.
