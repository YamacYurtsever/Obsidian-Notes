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
