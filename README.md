# Sorting algorithms
Name|Best-case time complexity|Average time complexity|Worst-case time complexity|Space complexity|Stable?
--|--|--|--|--|--
[Bubble sort](https://en.wikipedia.org/wiki/Bubble_sort)|O(n) comparisons, O(1) swaps|O(n^2) comparisons and swaps|O(n^2) comparisons and swaps|O(1)|Yes
[Counting sort](https://en.wikipedia.org/wiki/Counting_sort)|-|O(n+k)|O(n+k)|O(n+k)|Yes
[Heapsort](https://en.wikipedia.org/wiki/Heapsort)|O(n log n)|O(n log n)|O(n log n)|O(1)|No
[Insertion sort](https://en.wikipedia.org/wiki/Insertion_sort)|O(n) comparisons, O(1) swaps|O(n^2) comparisons and swaps|O(n^2) comparisons and swaps|O(1)|Yes
[Merge sort](https://en.wikipedia.org/wiki/Mergesort)|O(n log n)|O(n log n)|O(n log n)|O(n)|Yes
[Quicksort](https://en.wikipedia.org/wiki/Quicksort)|O(n log n)|O(n log n)|O(n^2)|O(log n)|No
[Radix sort](https://en.wikipedia.org/wiki/Radix_sort)|O(k*n)|O(k*n)|O(k*n)|O(k+n)|Yes
[Selection sort](https://en.wikipedia.org/wiki/Selection_sort)|O(n^2) comparisons, O(1) swaps|O(n^2) comparisons, O(n) swaps|O(n^2) comparisons, O(n) swaps|O(1)|No

# Quicksort
## Why is the average time complexity `n log n`?
Because ...
* Each partitioning is O(n) because you have to visit every element.
* Partitioning is repeated for the height of the tree.
* Hence, the time complexity is `n * height`.

#### Height of tree
##### Ideal case
You choose a pivot that partitions the input in half. In the case, the height of the tree is `log(n)` because `n ≤ 2^h - 1`.

##### Worst case
You choose a pivot that is the smallest or largest element. In the case, the height of the tree is `n`.

## How to avoid the worst-case scenario?
* Randomly choose a pivot.
* Choose the median as a pivot.

# Quicksort versus Merge sort versus Heapsort
Name|Strengths|Weaknesses
---|---|---
Quicksort|* Fastest in practice<br>* Parallelizable because it is a divide-and-conquer algorithm|* Slow worst-case<br>* Not stable
Merge sort|* Fast worst-case<br>* Parallelizable because it is a divide-and-conquer algorithm<br>* Stable|Space inefficient
Heapsort|* Fast worst-case<br> * Space efficient|* Slow in practice<br>* Not stable

# Note
* The space complexity O(1) means in-place sorting.
* Stable sorting algorithms maintain the relative order of records with equal values.
* n and 2n are both O(n).
* Quicksort and heapsort are single words but merge sort is not.
