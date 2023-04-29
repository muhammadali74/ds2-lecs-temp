# Week5

## Skip List

- A skip list is a cobination of multiple linked lists (sort of). 
- The base linked list contains all values and points to next node.
- The other linked lists skip some elements
- The skipping of elemtns is decided based on fair randomness.
- For traversing, we start on the top most layer linked list.
- There is a head and a tail. The head and tail node should have the maximum no of levels.
- The head node is called the Sentinal nodes
- THe first node level is called level 0. It contains all the nodes as the no of elements in the skip list
- **level 1** would have around (1/2)n nodes since the porbablily of getting heads is half.
- **level 2** has probability of (1/2)^2 so it would have 1/4 n nodes and so on
- on level log2n the no of nodes would be 1.
- so on average, given a skip list of size n, the total no of nodes would be n/2 + n/4 + ... n/2^logn = n(1 + 1/2 + 1/4 + 1/2^logn)  =2n
- onn avergae the height, or the no of sentinal nodes ois log2n.
- the traversal complexity, sice we are skipping osme nodes eevry time and then going down the traversal time which was linear in linked,,, was reduced to O(logn).

- If, instead of using probabilty for adding node levels, we fix a cconvention at we skip one elemnt realtive to the prevous ones on ach consecutiv step, then the problem is that nsertion deeltion would be a headache. cz if say, i deleted an element then i would need to  do rearrangemnt of all the pointers to keep the method consistent.
- thats why we do coin flip wali cheez.
- also, it is conventionally 
