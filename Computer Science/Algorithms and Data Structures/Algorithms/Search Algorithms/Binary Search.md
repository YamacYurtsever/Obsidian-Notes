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
-  Needs to be sorted before being searched
- [[Time Complexity]]: O(log n)