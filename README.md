#include <stdio.h>
int main()
{
    int arr[] = {50,60,70,80,50};
    int size = sizeof(0);
    printf("Array elements:");
    for(int i =0; i<size; i++)
    {
        printf("%d",arr[i]);
    }
    printf("\n");
    return 0 ;
}   


   #new one#
#include <stdio.h>

// Function to insert an element at a specific position in an array
void insertElement(int arr[], int *size, int element, int position) {
    // Check if position is valid
    if (position < 0 || position > *size) {
        printf("Invalid position!\n");
        return;
    }

    // Shift elements to the right to create space
    for (int i = *size; i > position; i--) {
        arr[i] = arr[i - 1];
    }

    // Insert the new element
    arr[position] = element;

    // Update the size of the array
    (*size)++;
}

int main() {
    int arr[100] = {1, 2, 4, 5};
    int size = 4;

    printf("Original array: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    insertElement(arr, &size, 3, 2); // Insert 3 at index 2

    printf("Array after insertion: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    return 0;
}
