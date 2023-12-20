##### Truncation: 
- Discarding the fractional part of a number, leaving only the integer component
```C
int a = 5;
int b = a / 2;
// b = 2 because the fractional part got truncated
```

##### Overflow:
- Reaching a value for a [[Variables | variable]], that is higher than the maximum value possible to represent with the [[Data Representation#Memory Sizes of Variables | memory size]] of that variable
```C
int maxInt = 2147483647;
int result = maxInt + 1;
// result = -2147483648
```
- Integers are represented with [[Data Representation#Memory Sizes of Variables | 4 bytes]], thus the operation in the code above will lead to a **wrap around** to the minimum representable value for a signed 32-bit integer, which is -2147483648

##### Floating Point Imprecision
- Floating-point numbers in computers have limited precision due to the finite representation of real numbers in [[Data Representation#^79c0a2 | binary]]
- This imprecision can result in rounding errors, making it challenging to represent some decimal numbers accurately
```C
float a = 0.1;
float b = 0.2;
float sum = a + b;

printf("a: %.20f\n", a);
printf("b: %.20f\n", b);
printf("Sum: %.20f\n", sum);

/*
a: 0.10000000149011611938
b: 0.20000000298023223877
Sum: 0.30000001192092895508
*/
```

##### Type Casting
- Changing the data type of a variable
```C
float a = 5 / 2;
float b = (int)a;
// a = 2.5 & b = 2
```

##### Unsigned
- Numerical [[Variables | variable]] are signed by default meaning they can be both positive and negative
- Using the keyword unsigned before a variable doubles their positive range at the expense of not being able to store negative values
```C
unsigned int x = -5;
// This will result in an error
```

#### Constants
- Values in a program that, once assigned, cannot be changed during the program's execution
- They are used to represent fixed values, such as mathematical constants or configuration settings
```C
const float PI = 3.14159;
PI += 1;
// This will result in an error
```

