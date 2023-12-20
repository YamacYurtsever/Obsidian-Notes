- Parameters (also called Arguments and Inputs) in programming refer to variables or values that are passed into a [[Functions | function]] when it is called
- These parameters provide input to the [[Functions | function]], allowing it to perform actions or computations based on the provided values

### Pass by Value vs Pass by Reference
| Pass by Value                                                         | Pass by Reference                                              |
| --------------------------------------------------------------------- | -------------------------------------------------------------- |
| A copy of the value is passed to the function                         | A reference or memory address is passed to the function        |
| Modifications inside the function do not affect the original variable | Modifications inside the function affect the original variable |
| E.g.: [[Variables#Primitive Variables \| Primitive Variables]]        | E.g.: [[Variables#Composite Variables \| Composite Variables]] | 

```C
#include <stdio.h>

void modifyValueByValue(int x) {
    x = x * 2;
}

void modifyValueByReference(int *x) {
    *x = *x * 2;
}

int main() {
    int num1 = 10;
    int num2 = 10;

	modifyValueByValue(num1);      // num1 = 10
    modifyValueByReference(&num2); // num2 = 20

    return 0;
}
```