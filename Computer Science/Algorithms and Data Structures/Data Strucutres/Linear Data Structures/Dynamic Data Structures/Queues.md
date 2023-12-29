- Follow the First-In-First-Out (FIFO) principle
- Elements are added to the rear and removed from the front, which ensures that the oldest element in the queue is the next one to be processed
- Can be searched at [[Time Complexity#^2171dc | linear time O(n)]]
- E.g.: Printer Spooling

#### Key Operations
- **Enqueue**: Adds an element to the rear of the queue
- **Dequeue**: Removes an element from the front of the queue
- **Peek**: Returns the element at the front of the queue without removing it
- **IsEmpty**: Checks whether the queue is empty or not
- **Size**: Returns the number of elements in the queue

#### Implementation
Python:
```python
class Queue:
    def __init__(self):
        self.items = []

    def is_empty(self):
        return len(self.items) == 0

    def enqueue(self, item):
        self.items.append(item)

    def dequeue(self):
        if not self.is_empty():
            return self.items.pop(0)
        else:
            raise IndexError("Dequeue from an empty queue")

    def peek(self):
        if not self.is_empty():
            return self.items[0]
        else:
            raise IndexError("Peek from an empty queue")

    def size(self):
        return len(self.items)
```

C:
```C
#include <stdio.h>
#include <stdlib.h>

#define MAX_SIZE 100

// Structure to represent a queue
struct Queue {
    int items[MAX_SIZE];
    int front;
    int rear;
};

void initializeQueue(struct Queue* queue) {
    queue->front = -1;
    queue->rear = -1;
}

int isEmpty(struct Queue* queue) {
    return (queue->front == -1 && queue->rear == -1);
}

int isFull(struct Queue* queue) {
    return (queue->rear == MAX_SIZE - 1);
}

void enqueue(struct Queue* queue, int value) {
    if (isFull(queue)) {
        printf("Queue is full. Cannot enqueue.\n");
        return;
    }

    if (isEmpty(queue)) {
        // If the queue is empty, set both front and rear to 0
        queue->front = 0;
        queue->rear = 0;
    } else {
        // Increment rear circularly
        queue->rear = (queue->rear + 1) % MAX_SIZE;
    }

    // Enqueue the element
    queue->items[queue->rear] = value;
}

int dequeue(struct Queue* queue) {
    int dequeuedValue;

    if (isEmpty(queue)) {
        printf("Queue is empty. Cannot dequeue.\n");
        exit(EXIT_FAILURE);
    } else if (queue->front == queue->rear) {
        // If there is only one element in the queue
        dequeuedValue = queue->items[queue->front];
        queue->front = -1;
        queue->rear = -1;
    } else {
        // Dequeue the front element and increment front circularly
        dequeuedValue = queue->items[queue->front];
        queue->front = (queue->front + 1) % MAX_SIZE;
    }

    return dequeuedValue;
}

int peek(struct Queue* queue) {
    if (isEmpty(queue)) {
        printf("Queue is empty. Cannot peek.\n");
        exit(EXIT_FAILURE);
    }

    return queue->items[queue->front];
}
```

