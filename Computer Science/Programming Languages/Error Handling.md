- A programming concept that involves managing and responding to errors (exceptions )that may occur during the execution of a program
- The goal is to gracefully handle unexpected situations, prevent program crashes, and provide meaningful feedback to users or developers about what went wrong

### Exit Codes
- Specific exit codes are used to indicate success, errors, or other conditions
- 0 is usually the exit code for success

```C
int main() {
    if (some_condition) {
        return EXIT_FAILURE;
    }
    return EXIT_SUCCESS;
}

```

### Exception Handling 
- **Try Block**:
	- Contains the code that might raise an exception
- **Except Block**:
	- Specifies how to handle a specific type of exception
	- If an exception occurs in the try block, the corresponding except block is executed
- **Else Block** (Optional):
	- Contains code that should run if no exceptions occurred in the try block
	- It is executed only if no exceptions were raised

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Error: Division by zero.")
else:
    print("No errors.")
```