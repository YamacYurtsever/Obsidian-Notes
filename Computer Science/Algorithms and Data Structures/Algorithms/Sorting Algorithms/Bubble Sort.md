```C
void bubbleSort(arr[], int n) {
	for (int i = 0; i < n - 1; i++) {
		for (int j = 0; j < n - i - 1; j++) {
			if (arr[j + 1] < arr[j]) {
				// Swap elements if they are in wrong order
				int temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
			}
		}
	}
	return;
}
```

- Since after each iteration of the outer loop, the largest element is guaranteed to be at the last index, there is no need to compare and swap it again. Hence, n - i - 1 is used as the upper limit for the inner loop.
- [[Time Complexity]]: O($n^2$)