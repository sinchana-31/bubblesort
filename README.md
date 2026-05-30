# bubblesort
#include <stdio.h>
#include <stdbool.h>

// Function to perform Bubble Sort
void bubbleSort(int arr[], int size) {
    int temp;
    bool swapped;

    // Outer loop for passes
    for (int i = 0; i < size - 1; i++) {
        swapped = false;

        // Inner loop for adjacent element comparisons
        for (int j = 0; j < size - i - 1; j++) {
            // Change > to < to sort in descending order
            if (arr[j] > arr[j + 1]) {
                // Swap elements
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
                
                swapped = true; // Mark that a swap occurred
            }
        }

        // If no two elements were swapped by inner loop, then break
        if (swapped == false) {
            break;
        }
    }
}

// Function to print the array
void printArray(int arr[], int size) {
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
bubblesort
the sorting of elements

