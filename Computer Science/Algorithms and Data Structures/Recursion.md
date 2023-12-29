A programming concept where a function calls itself

- **Recursive Case**
Approaches base case

- **Base Case**
Exit condition

```python
def fibonacci(n):
    if n <= 1:   # Base Case
        return n
	else:        # Recursive Case
        return fibonacci(n-1) + fibonacci(n-2)

```

^fa4b58
