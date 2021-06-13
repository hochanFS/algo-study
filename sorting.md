# Sorting

## Insertion Sort
The most rudimentary way of sorting.


```java
public void insertionSort(int[] arr) {
    int n = arr.length;
    for (int i = 1; i < n; i++) {
        j = i;
        while (j > 0 && a[j] > a[j - 1])
            swap(a, i, j--);
    }
}
```
* Time complexity: O(n^2)
* Space complexity: O(1)
