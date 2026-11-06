# Nanditha
#include <stdio.h>
#include <stdlib.h>

// Comparator for ascending order
int compare(const void *a, const void *b)
{
    return (*(int *)a - *(int *)b);
}

int findMax(int arr[], int n)
{
    // Sort the array in ascending order
    qsort(arr, n, sizeof(int), compare);

    // Last element is the largest
    return arr[n - 1];
}

int main()
{
    int arr[] = {5, 2, 7, 6};
    int n = sizeof(arr) / sizeof(arr[0]);

    printf("%d\n", findMax(arr, n));

    return 0;
}
