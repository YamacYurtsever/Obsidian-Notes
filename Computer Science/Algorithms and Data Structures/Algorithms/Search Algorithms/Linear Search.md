```C
int linearSearch(int arr[], int n, int target) {
    for (int i = 0; i < n; ++i) {
        if (arr[i] == target) {
            return i;  // Element found, return index
        }
    }
    return -1;  // Element not found
}
```
- [[Time Complexity]]: O(n)