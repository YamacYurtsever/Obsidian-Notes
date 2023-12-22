```C
void bubbleSort(arr[], int n) {
	for (int i = 0; i < n - 1; i++) {
		bool sorted = true;
		for (int j = 0; j < n - i - 1; j++) {
			if (arr[j + 1] < arr[j]) {
				// Swap elements if they are in wrong order
				int temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
				sorted = false;
			}
		}
		if (sorted)
			break;
	}
	return;
}
```

- Since after each iteration of the outer loop, the largest element is guaranteed to be at the last index, there is no need to compare and swap it again. Hence, n - i - 1 is used as the upper limit for the inner loop.
- [[Time Complexity]]: O($n^2$)

*Calculation*:  
- $\sum\limits_{i = 0}^{n-2}(n - i - 1)$ = (n - 1) + (n - 2)  + (n - 3) + ... + 1
- Arithmetic Series: $S_n = n * \frac{(n - 1) + 1}{2} = n * \frac{n}{2} = \frac{n^2}{2}$
- As n approaches infinity -> $n^2$