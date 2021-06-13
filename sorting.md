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

## Merge Sort (Iterative)

```java
public class IterativeMergeSort {
    public static void mergeSort(int[] array) {
        if (array == null || array.length < 2) return;
        int len = array.length;
        int[] temp = new int[len];
        for (int interval = 1; interval < len - 1; interval <<= 1) {
            for (int i = 0; i < len - interval; i += 2 * interval) {
                int mid = i + interval;
                int e = Math.min(len, mid + interval);
                merge(array, temp, i, mid, e);
            }
        }
    }

    private static void merge(int[] array, int[] temp, int s, int m, int e) {
        int i = s, j = m, k = s;
        while (i < m || j < e) {
            if (i == m || (j < e && array[i] > array[j]))
                temp[k++] = array[j++];
            else
                temp[k++] = array[i++];

        }
        System.arraycopy(temp, s, array, s, e - s);
    }
}
```
* Time complexity: O(n * log(n))
* Space complexity: O(n)
