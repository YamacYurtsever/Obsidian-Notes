- Used to organize and store data in an ordered manner, where each element can be quickly accessed directly by its index in the array
- The index usually starts from 0, and the elements are stored in contiguous memory locations
- **Has a fixed size** and can contain **only one data type**
- Can be searched at [[Time Complexity#^2171dc | linear time O(n)]]

#### Key Operations
- **Declaration**: Declares the type of elements the array will hold and specifies its size
- **Initialization**: Initializes the array with values at the time of declaration
```C
int numbers[5]; // Decleration
int values[] = {1, 2, 3, 4, 5}; // Decleration & Initialization
```
- **Accessing**:
```C
int third_element = numbers[2]
```
- **Modifying**
```C
numbers[0] = 10
```

#### Multi-Dimensional Arrays
- Multidimensional arrays are a natural extension of the concept of arrays, allowing you to organize data in more than one dimension
- They are often used to represent tables, matrices, or other higher-dimensional structures
```C
int matrix[3][4];
int matrixInitialized[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
int row1col2 = matrixInitialized[1][2];
int row3col2 = 12;
```