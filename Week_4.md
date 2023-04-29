# Week 4

## Amortized Analysis

- We see the time complexity of operations in usual iccaison even though it might take more time in some occasional condtions,.

## Aggregate Method

- When the array is resized, the total time taken to append the new element is the time to copy all the previous elements and 1

- So the

- Two methods for doing amortized analysis.
- aggregate method
- accounting method

## Scheme for increasing the size of array

- Incrreasing by a constant factor i.e doubling, tripling
- Increasing by constant no of cells. e.g increasing by 5 cells for example.

- in aggregate method we add the subsequent adding operations.
- In acounting method, we save our computations as reserve at each step ( or we can say we distribute evenly on each cell)and use the reserved computations up when needed.

# Session2

## We discussed: Array::

- Search O(1)
- add(i) O(n)

## Linked List

- Insertionjas two operations.
- TO reach the location of insertion, we need to traverse... TRVAERSAL: O(n) or i
- once at the location.. insertion O(1)
- addFirst O(1)
- addLast O(1)
- remove(i) O(n)--> wahi add wala scene. pehle traversal phir removal(which takes constant time)

## Doubly Linked List

- In double linked list, each node has pointers of next as well as previous nodes. THis way we can traverse forward as well as backward/

- This means in any case we wont be traversing more than half of the linked list.

## IMPLEMLMENTING QUEUE

- we can implement a stack and queue using linked list,
- We can also implement deque
  IN implementing DEQUE:
  addFIrt O(1)
  add Last O(1)
  Rm first O(1)
  Rm last O(n) -- problem

therefore, we can use doubly linked list here to implemtn dequq. it would be better,
