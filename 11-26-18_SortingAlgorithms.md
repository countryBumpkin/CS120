# Sorting Algorithms

* Insertion Sort
* Bubble Sort
* Selection Sort
* Merge Sort
* Quick Sort

## Insertion Sort
*This sort is like sorting cards. You pick one and insert it into the "sorted" side of your hand. Repeat until all cards are sorted.*

1. Element is inserted into the "sorted" portion of the array.
2. Next element is moved to the sorted section of the array. When inserted at the correct index, all the following elements must be moved up in the array.
3. Sorting is complete when the end of the array is reached.

## Bubble Sort
*Easier to implement than insertion sort but slower as more comparisons are required and the order is sometimes scrambled. Worst case big O value is very high while the best case is a constant value.*

1. Select first/last element of the array. This is the element in the "bubble".
2. Compare the bubble to all other elements, swapping them if not in correct order
3. Repeat this comparison process until all elements are sorted, meaning no swaps are performed.

## Selection Sort
*This method has a much better worst case scenario big O value than the previous two since it does not undo any positive progress that has been made towards sorting the list.*

1. Select the smallest element in the array and exchange it with the first element in the list. This first element marks the "sorted" portion of the list.
2. In the unsorted portion of the array, select the next smallest element and place in the index above our "sorted" section, expanding it.
3. Repeat until the list is sorted.

## Merge Sort
*Merge sort is a recursive as it starts with small segments and then merges them to create larger, sorted segments.*

1. Segment the array recursively, until the segment size is one element.
2. Next, these elements are merged with each other using comparisons to determine order.
3. Continue until all segments are combined.

## Quick Sort
*Developed in 1962 by C. A. R. Hoare, this algorithm rearranges the array into two parts. The first part contains the elements lower than the pivot value and the second portion contains the elements greater than or equal to the pivot.*

1. Set the first element of the list to be the pivot.
2. Loop through the elements in the list, arranging them to the left or right of pivot according to value.
3. Start with the bottom half of the array and then finish with the top.
4. The smallest segmentation of the arrays should be two elements.
