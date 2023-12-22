- A hierarchical data structure that consists of nodes connected by edges
- **Don't have a fixed size** and can contain **different data types**
- They have the scalability of linked lists while also being able to be searched in [[Time Complexity#^fd9f43 | logarithmic time O(log n)]] ([[#^28e812 | BTSs]])

#### Terms
- **Node**: A part of trees that contains data and may have zero or more children
- **Root**: The topmost node in a tree
- **Parent**: A node that has one or more child nodes
- **Child**: A node directly connected to another node when moving away from the root
- **Leaf**: A node with no children; it is a node at the end of a branch
- **Subtree**: A tree formed by a node and all its descendants.

![[Trees 2023-12-23 01.31.50.excalidraw]]

#### Types of Trees
- **Binary Tree**: 
A tree in which each node has at most two children, typically referred to as the left child and the right child
- **Binary Search Tree (BST)**:
A binary tree where the left subtree of a node contains only nodes with values less than the node's value, and the right subtree contains only nodes with values greater than the node's value ^28e812

#### Tree Traversal
- **Inorder**: Left - Root -Right
- **Postorder**:  Left - Right - Root
- **Preorder**: Root - Left - Right

#### Removing the Root in BSTs
- When the root node is removed:
	- The rightmost node of the left subtree can replace it
	- The leftmost node of the right subtree can replace it

#### Implementation
```C
struct Node {
    int value;
    struct Node* left;
    struct Node* right;
};

struct Node* createNode(int value) {
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->value = value;
    newNode->left = NULL;
    newNode->right = NULL;
    return newNode;
}

struct Node* insert(struct Node* root, int value) {
    if (root == NULL) {
        return createNode(key);
    }

    if (key < root->value) {
        root->left = insert(root->left, value);
    } else if (key > root->value) {
        root->right = insert(root->right, value);
    }

    return root;
}

void inorderTraversal(struct Node* root) {
    if (root != NULL) {
        inorderTraversal(root->left);
        printf("%d ", root->value);
        inorderTraversal(root->right);
    }
}

struct Node* search(struct Node* root, int value) {
    if (root == NULL || root->value == value) {
        return root;
    }

    if (key < root->value) {
        return search(root->left, value);
    } else {
        return search(root->right, value);
    }
}
```