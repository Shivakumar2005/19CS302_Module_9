# EX 42 C program to write a fuctions to perform push,pop,display,peek in stack using array.
## DATE:08/09/2025
## AIM:
To write a fuctions to perform push,pop,display,peek in stack using array.

## Algorithm
1. Start the program and declare stack array with top = -1.
2. Define push function to insert an element into the stack.
3. Define pop function to delete the top element from the stack.
4. Define peek function to return the top element of the stack. 
5. Define display function to print all elements of the stack and call these functions in main.  

## Program:
#include <stdio.h>
#define SIZE 5

int stack[SIZE], top = -1;

void push(int value) {
    if(top == SIZE - 1)
        printf("Stack Overflow\n");
    else
        stack[++top] = value;
}

void pop() {
    if(top == -1)
        printf("Stack Underflow\n");
    else
        printf("Popped element: %d\n", stack[top--]);
}

int peek() {
    if(top == -1)
        return -1;
    else
        return stack[top];
}

void display() {
    if(top == -1)
        printf("Stack is empty\n");
    else {
        printf("Stack elements: ");
        for(int i = top; i >= 0; i--)
            printf("%d ", stack[i]);
        printf("\n");
    }
}

int main() {
    push(10);
    push(20);
    push(30);
    display();
    printf("Top element: %d\n", peek());
    pop();
    display();
    return 0;
}


## Output:

<img width="1466" height="664" alt="image" src="https://github.com/user-attachments/assets/876156b1-dbf9-4e29-8817-9d514780a0d7" />


## Result:
Thus the program was executed and the output was verified successfully.
