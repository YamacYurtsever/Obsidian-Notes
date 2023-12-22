- Follow the Last-In-First-Out (LIFO) principle
- The last element added is the first one to be removed first
- Can be searched at [[Time Complexity#^2171dc | linear time O(n)]]
- E.g.: Going Back on a Browser

#### Key Operations
- **Push**: Adds an element to the top of the stack.
- **Pop**: Removes the element from the top of the stack.
- **Peek**: Returns the element at the top of the stack without removing it
- **isEmpty**: Checks if the stack is empty
- **Size**: Returns the number of elements in the stack

#### Implementation
Python
```python
class Stack:
    def __init__(self):
        self.items = []

    def is_empty(self):
        return len(self.items) == 0

    def push(self, item):
        self.items.append(item)

    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        else:
            raise IndexError("pop from an empty stack")

    def peek(self):
        if not self.is_empty():
            return self.items[-1]
        else:
            raise IndexError("peek from an empty stack")

    def size(self):
        return len(self.items)
```
C
```C
#include <stdio.h>
#include <stdlib.h>

#define MAX_SIZE 100

struct Stack {
    int items[MAX_SIZE];
    int top;
};

void initialize(struct Stack* stack) {
    stack->top = -1;
}

int is_empty(struct Stack* stack) {
    return stack->top == -1;
}

int is_full(struct Stack* stack) {
    return stack->top == MAX_SIZE - 1;
}

void push(struct Stack* stack, int value) {
    if (is_full(stack)) {
        printf("Stack overflow\n");
        exit(EXIT_FAILURE);
    }

    stack->items[++stack->top] = value;
}

int pop(struct Stack* stack) {
    if (is_empty(stack)) {
        printf("Stack underflow\n");
        exit(EXIT_FAILURE);
    }

    return stack->items[stack->top--];
}

int peek(struct Stack* stack) {
    if (is_empty(stack)) {
        printf("Stack is empty\n");
        exit(EXIT_FAILURE);
    }

    return stack->items[stack->top];
}

int size(struct Stack* stack) {
    return stack->top + 1;
}
```