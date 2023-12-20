### Linear Search
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

### Binary Search
```C
int binarySearch(int arr[], int n, int target) {
    int low = 0;
    int high = n - 1;

    while (low <= high) {
        int mid = low + (high - low) / 2;
        
        if (arr[mid] == target) {
            return mid;      // Element found, return index
        } else if (arr[mid] < target) {
            low = mid + 1;   // Search the right half
        } else {
            high = mid - 1;  // Search the left half
        }
    }
    return -1;  // Element not found
}
```
- [[Time Complexity]]: O(log n)
- ! Needs to be sorted before being searched