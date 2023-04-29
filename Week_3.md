# Week 3

### ADT's in textbook

- 2.1 ArrayStack
- Array Queue
- Array Deque
- DualArrayDqeue
- RootishArrayStack

## Dynamic Array

- Total resize cost is O(m) where m is the number of elements added

- Total cost of adding = O(n-i) + O(m)
- The growth behviour of cost time is linear.
- **!!!! REMEMBER we are looking at worst case scenario of amortized analysis. NOt of worst case scenario**

## Array Queue

```
add(x):
    if (n+1)> lenght(a) then resize() {grow}
    a[(j+n) mod length(a)] <-- x
    n = n+1
    return true

remove():
    x = a[j]
    j = (j+1)mod len(a)
    n = n-1
    if length(a)>= 3n then resize() {shrink}

```

- we can have two different implementations of this. Either we can use two pointers i and j. On epointing to the first element and one pointing to the last element. Or we can use j as a pointer and n as the no. of variables and use them just like the implementation of add(x) above.

- When the arrayQueue will grow or shrink then the elements get moved in sequence, in the newly made array. i.e the pointer j becomes 0.

## Array Deque

- has nothing to do with a fucking deque. shit name the author has given to this.

```
add(i,x):
    if n = len(a) then resize()
    if i<n/2 then
    j = (j-1) mod len(a)
    for k in 0,1,2,..,i-1 do
        a[(J+k) mod len(a)] = a[(j+k+1) mod len(a)]

    else
        for k in n,n-1,..,i+1 do
            a[j+k) mmod len(a)] = ()shift agay ya peechay)

    a[(j+1) mod len(a)]
    n = n+1
```
