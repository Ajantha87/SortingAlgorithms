# SortingAlgorithms

<img src="https://cdn.educba.com/academy/wp-content/uploads/2019/10/Sorting-Algorithms-in-Java.jpg"></img>

<h2> A Sorting Algorithm is used to rearrange a given array or list elements according to a comparison operator on the elements. The comparison operator is used to decide the new order of element in the respective data structure. </h2>


<h3> Bubble Sort </h3>

Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in wrong order.

First Pass:
	
	( 5 1 4 2 8 ) –> ( 1 5 4 2 8 ), Here, algorithm compares the first two elements, and swaps since 5 > 1.
	( 1 5 4 2 8 ) –>  ( 1 4 5 2 8 ), Swap since 5 > 4
	( 1 4 5 2 8 ) –>  ( 1 4 2 5 8 ), Swap since 5 > 2
	( 1 4 2 5 8 ) –> ( 1 4 2 5 8 ), Now, since these elements are already in order (8 > 5), algorithm does not swap them.

Second Pass:
	
	( 1 4 2 5 8 ) –> ( 1 4 2 5 8 )
	( 1 4 2 5 8 ) –> ( 1 2 4 5 8 ), Swap since 4 > 2
	( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )
	( 1 2 4 5 8 ) –>  ( 1 2 4 5 8 )
	
Now, the array is already sorted, but our algorithm does not know if it is completed. The algorithm needs one whole pass without any swap to know it is sorted.

Third Pass:

	( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )
	( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )
	( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )
	( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )
	

<h3> Insertion Sort </h3>

Insertion sort is a simple sorting algorithm that works similar to the way you sort playing cards in your hands. The array is virtually split into a sorted and an unsorted part. Values from the unsorted part are picked and placed at the correct position in the sorted part.

	1: Iterate from arr[1] to arr[n] over the array.

	2: Compare the current element (key) to its predecessor.

	3: If the key element is smaller than its predecessor, compare it to the elements before. Move the greater elements one position up to make space for the swapped element.
	
	
		arr[] = 12 11 13 5 6

		Let us loop for i = 1 (second element of the array) to 4 (last element of the array)

		i = 1. Since 11 is smaller than 12, move 12 and insert 11 before 12
		11, 12, 13, 5, 6

		i = 2. 13 will remain at its position as all elements in A[0..I-1] are smaller than 13
		11, 12, 13, 5, 6

		i = 3. 5 will move to the beginning and all other elements from 11 to 13 will move one position ahead of their current position.
		5, 11, 12, 13, 6

		i = 4. 6 will move to position after 5, and elements from 11 to 13 will move one position ahead of their current position.
		5, 6, 11, 12, 13 

	
<h3> Merge Sort </h3>

Like QuickSort, Merge Sort is a Divide and Conquer algorithm. It divides input array in two halves, calls itself for the two halves and then merges the two sorted halves. The merge() function is used for merging two halves. The merge(arr, l, m, r) is key process that assumes that arr[l..m] and arr[m+1..r] are sorted and merges the two sorted sub-arrays into one. See following C implementation for details.

	if r > l
	
		1. Find the middle point to divide the array into two halves:  
			middle m = (l+r)/2

		2. Call mergeSort for first half:   
			Call mergeSort(arr, l, m)

		3. Call mergeSort for second half:
			Call mergeSort(arr, m+1, r)

		4. Merge the two halves sorted in step 2 and 3:
			Call merge(arr, l, m, r)
	
	
<h3> Selection Sort </h3>

The selection sort algorithm sorts an array by repeatedly finding the minimum element (considering ascending order) from unsorted part and putting it at the beginning. The algorithm maintains two subarrays in a given array.

	1: The subarray which is already sorted.
	
	2: Remaining subarray which is unsorted.
	
		arr[] = 64 25 12 22 11

		// Find the minimum element in arr[0...4]
		// and place it at beginning
		11 25 12 22 64

		// Find the minimum element in arr[1...4]
		// and place it at beginning of arr[1...4]
		11 12 25 22 64

		// Find the minimum element in arr[2...4]
		// and place it at beginning of arr[2...4]
		11 12 22 25 64

		// Find the minimum element in arr[3...4]
		// and place it at beginning of arr[3...4]
		11 12 22 25 64 	