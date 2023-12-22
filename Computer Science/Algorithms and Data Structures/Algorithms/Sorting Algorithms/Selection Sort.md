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

*Calculation*:
- Each round in the outer for loop -> (n - 1) + (n - 2) + (n - 3) + ...
- Arithmetic series -> $S_n = n * \frac{(n - 1) + 1}{2} = n * \frac{n}{2} = \frac{n^2}{2}$
- As n approaches infinity -> $n^2$