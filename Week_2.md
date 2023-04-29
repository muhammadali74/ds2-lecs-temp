# Week_2

### Stacks

- Defined stacks using arrays.
- Limitataions... fixed size (as of now)

### Queues ATD using Arrays

```
class Queue
    data[size]
    begin = 0
    end = 0
    no_of_elements = 0

def Enq(x):
    if no_of_elements <= size:
        data[end] = x
        end=(end + 1) % size;
        no_of_elements +=1

def Deq():
    if no_of_elements>0:
        x = data[begin]
        begin += (begin+1) % size
        no_of_elemenets -=1
        return x

```

if the size goes out of bound the we need to set the pointer to start again. Also keep track of the total no of elemnts present to keep track of overflow and underflow.

### Implementing List using Arrays

- adding an element:

```
def add(i,x):
    -> push element from i+1 for n-i
    -> set the vlaue of ith element
```

- big oH us used for upper bounds of worst case or best case or avergae case
- similarly theta and other notations are used for tight bounds and lower bounds.
- THE TIME TAKEN FOR adding and removing the elementsis n-i. This is good if we are adding and removing from the later part of the list, but for adding/removing from the starting elems, it requires much shit.

- therefore, instead of doing it linearly we can do it with a Array Deque, which add elements/ removes from start (pushing elemnts back), if operartion needs to be performed on the first half of the lisst and pushes ements fornt just like linearly list, if it is on later part of the list. So it is a two way expansion.

## Making lists using arrays which donot have a static size

### We use a concept called "Growing and Shrinking"

- **GROW**: If the array is full, increase the size by 2n
- **SHRINK**: If array size is greater than 3n, decrease the size by n/2. This just means that if only one-third of the list at any time, is full and two-thirds is empty then this condition wil trigger.

- e.g if a list is of size 8 initially and it gets full then we make the size 16. now suppose thaat we remove elements. if say we now only have 5 elemes in teh arary which is of size 16 now, we see 16 > 3\*5 (3 times n where n is no of elements). In that case we will reduce the size by n/2 i.e by 16/2 = 8

- You will understand the logic behind 3n and 2n in analysis.-
