! All of the algorithms below are sorting in ascending order
### Selection Sort
```C
void selectionSort(arr[], int n)
	int smallestIndex, temp;
	for (int i = 0; i < n - 1; i++) {
		smallestIndex = i;
	
		// Find the index of the smallest element in the unsorted part of the array
		for (int j = i + 1; j < n; j++) {
			if (arr[j] < arr[smallestIndex])
				smallestIndex = j;
		}

		// Swap the smallest element with the current element (arr[i])
		temp = arr[i];
		arr[i] = arr[smallestIndex];
		arr[smallestIndex] = temp;
	}
	return;
}
```
[[Time Complexity]]: O($n^2$)

- *Calculation*:
- Each round in the outer for loop -> (n - 1) + (n - 2) + (n - 3) + ...
- Arithmetic sequence -> $S_n$ = $n * \frac{(n - 1) + 1}{2}$ = $n * \frac{n}{2}$ = $\frac{n^2}{2}$
- As n approaches infinity -> $n^2$

### Bubble Sort
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
[[Time Complexity]]: O($n^2$)

*Calculation*:
- Each round in the outer loop -> (n - 1) + (n - 2) + (n - 3) + ...
- Arithmetic sequence -> $S_n$ = $n * \frac{(n - 1) + 1}{2}$ = $n * \frac{n}{2}$ = $\frac{n^2}{2}$
- As n approaches infinity -> $n^2$

### Merge Sort
```C
void mergeSort(int arr[], int left, int right) {
    if (left == right) // One element left
	    return;
	else {
        int mid = (left + right) / 2;

        // Sort first and second halves
        mergeSort(arr, left, mid);
        mergeSort(arr, mid + 1, right);

        // Merge the sorted halves
        merge(arr, left, mid, right); 
    }
    return;
}
```

[[Time Complexity]]: O(n log n)

*Calculation*:
- Divide Step: We divide the array into two halves at each recursive call -> $log_2(n)$
- Merge Step: At each level of recursion, there is a total of n elements to merge (considering both halves) -> n$log_2(n)$
- Thus, T(n) = Divide + Merge = n$log_2(n)$ + $log_2(n)$ = (n + 1)$log_2(n)$
- As n approaches infinity -> n log n
