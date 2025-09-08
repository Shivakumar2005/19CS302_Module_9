# EX 44 C functions to perform enqueue, dequeue, display, peek in Queue using Array.
## DATE:08/09/2025
## AIM:
To write a C Write a functions to perform enqueue, dequeue, display, peek in Queue using Array.

## Algorithm
1. Start the program and declare queue array with front and rear.
2. Define enqueue function to insert an element into the queue.
3. Define dequeue function to remove an element from the queue.
4. Define peek function to return the front element of the queue. 
5. Define display function to print all queue elements and call functions in main.  

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

void dequeue() {
    if(front == -1 || front > rear)
        printf("Queue Underflow\n");
    else
        printf("Dequeued element: %d\n", queue[front++]);
}

int peek() {
    if(front == -1 || front > rear)
        return -1;
    else
        return queue[front];
}

void display() {
    if(front == -1 || front > rear)
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
    printf("Front element: %d\n", peek());
    dequeue();
    display();
    return 0;
}

## Output:

<img width="1522" height="690" alt="image" src="https://github.com/user-attachments/assets/38c7bdde-dc83-4604-8ce3-42d402a013c7" />


## Result:
Thus the program was executed and the output was verified successfully.
