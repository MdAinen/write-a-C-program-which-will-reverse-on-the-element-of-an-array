#include <stdio.h>

void reverseArray(int arr[], int size) {
    int temp;
    int start = 0;
    int end = size - 1;
    while (start < end) {
        temp = arr[start];
        arr[start] = arr[end];
        arr[end] = temp;
        start++;
        end--;
    }
}

int main() {
    int size;
    printf("Enter the size of the array: ");
    scanf("%d", &size);
    int arr[size];
    printf("Enter %d elements of the array: \n", size);
    for (int i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }
    reverseArray(arr, size);
    printf("Reversed array: \n");
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
    return 0;
}
