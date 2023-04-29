# Week 1

Considerations while analyzing a data structure:
- Linear vs Non llinear
- Sequential vs Non Sequential
- Static vs Dynamic
- Homogonous vs non
- By Time and Space Complexity

## Abstraction
- Hiding the internal functioning of a particular data structure and providing an interface usuage to the user.
- A Data Structure/Tyoe wich is internally based on some other built-in data type but we make an interface to provide a speciifcset of functionailities. without exposing how it is actually working,
- For Abstract data strcutures, you may maybe later chnage the internal structure, implementation of the ds but as long as the interface remains the same (gives same input/output),  you are all good

## Abstract DS INterfaces and their Implemntations
- Lists --> Arrays
- Stack --> Arrays
- Queue --> Linked Lists
- - Priority
- - Circular
- - DEQUE

- Set
- - Unsorted Set
- - Sorted Set

## Arrays (static)
- Contigious block of memory gets allocated in the memory so access is O(1), since we only need to give the offset number of what physical memory we want to access
- But this puts a limit that an array has to be static, since a specific contigous memory block HAS to be allocated
- This random access also accounts for the fact that the arrays are homogenous since EACH cell has to be of the same size so that we can just give an offset (array start memory x the number of element we want to access) e.g (2 * 5) something like that
- 