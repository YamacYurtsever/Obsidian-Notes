- A linear data structure consisting of nodes where each node points to the next node in the sequence
- Unlike arrays, linked lists do not have a fixed size, and their elements are stored in dynamically allocated nodes
- This dynamic structure allows for efficient insertion and deletion operations at any position in the list
- Can be searched at [[Time Complexity#^2171dc | linear time O(n)]]

![[Linked Lists 2023-12-22 13.05.15.excalidraw]]

#### Types of Linked Lists
- Singly Linked Lists
	- Each node has a pointer to the next node
- Doubly Linked Lists
	- Each node has a pointer to both the next and previous node
- Circular Linked Lists
	- The last node points to the first node

#### Implementation
```C
typedef struct node {
	int value;
	struct node* next;
} node;

// Example Usage
int main() {
	node node1, node2, node3;
	
	node1.value = 10;
	node2.value = 20;
	node3.value = 30;
	
	node1.next = &node2;
	node2.next = &node3;
	node3.next = NULL;
	
	node* head = &node1;
	node* current = head;

	while (current != NULL) {
		printf("%i\n", current->number);
		current = current->next;
	}

	return 0;
}
```

#### Inserting to the Beginning
```C
int InsertToBeginning(node* head, int newValue) {
	// Create New Node
	node* newNode = malloc(sizeof(node));
	if (newNode == NULL)
		return 1;
	newNode->value = newValue;
	
	// Insert to Beginning
	newNode->next = head;
	head = newNode;

	return 0;
}
```

#### Inserting to the Index
```C
int InsertToIndex(node* head, int newValue, int index) {
	// Create New Node
	node* newNode = malloc(sizeof(node));
	if (newNode == NULL)
		return 1;
	newNode->value = newValue;
	
	// Traverse the Linked List Until the Index
	node* current = head;
	for (int i = 0; i < index; i++) {
		current = current->next;
		if (current == NULL) {
			printf("Index out of range\n");
			return 2;
		}
	}
	
	// Insert to the Index
	newNode->next = current->next;
	current->next = newNode;

	return 0;
}
```




