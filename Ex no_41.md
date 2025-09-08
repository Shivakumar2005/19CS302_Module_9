# EX 41 C program to write a function to find the peek of stack using array.
## DATE:
## AIM:
To write a function to find the peek of stack using array.

## Algorithm
1. Start the program and define stack operations.
2. Initialize stack array and top variable.
3. Push elements into the stack.
4. Call the peek function to return the top element. 
5. Display the top element as output.  

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

int peek() {
    if(top == -1)
        return -1;
    else
        return stack[top];
}

int main() {
    push(10);
    push(20);
    push(30);
    printf("Top element is: %d\n", peek());
    return 0;
}


## Output:

<img width="1453" height="664" alt="image" src="https://github.com/user-attachments/assets/efad75f7-2605-490f-b958-47280a12c17d" />


## Result:
Thus the program was executed and the output was verified successfully.
