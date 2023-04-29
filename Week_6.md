# Week 6

## Hash Table

- **Hash Functions**: a function which takes a key and it returns you the index in O(1) time.
- Using this you can directly know the index given the key. hence you dont need any traversal

## Problems with hashtables:
- there could be repetition.
- for e.g if we have defined our hasfunction in a way that it gives us index from o-49 by doing id%50. then we could have repition
- 03871 % 50 and 03921 % 50 gives the same index i.e 21. 
- This case/probpem is called collision.
- In deal case we might define a hash function which never does repetition but that is not the case everytime. 
## Collision Resolution
### Chaining (Chained Hashtable)
- If we have mutiple values against the same index then we would have a chained hashtable now. Every index is pointing towards a list/bucket/collection. So we have mutlipe things attached to a single index. If the hashfucntion gives same index for two values then we can store both on that single index by pointing that index to a bucket containing both keys and their correspondng values.
- Accessing mutiple values: if a user wants to access a key value pair, then we can go to the index whihc stores the bucket and then traverse the bucket until it finds that keyvalue pair. 

- We ideally want to have a function in which the key values are uniformly divided over the index. i.e  there is minimal repetition/colision. But it is not always the case. One cant claim that thier hsh funcutio will wlways be unirformly distributed.

- E.G Data : 4 20 39 17 29 34 11 60 45 58 48 12
- Hash function: (x-3) % 11
- we have possile indexes (0 - 10) since mod 11 hai.
- [ 0:{58} 1:{4, 48} 2:{60} 3:{39, 17} 4:{4} 5:{} 6:{20} 7:{} 8:{11} 9:{34, 45, 12} 10:{} ]

- Our hash function should be such that it gives us a fixed range for hash tables 
- The size of data is repsented by n and that of Hastable si represented by N

### Probing / Open addressing
- If the index returned by hash function is already occupied by a ey, then go to the next index until you find an empty index for your key.
- The method discuessed above ^^ is called "Linear probing".
- in open addressing, we should have have the size of hashtable (N) greater than that of our data n.


- We saw linear probing, quadratic probing, double hashing. 


### Analysis of Hashtables.
- When the hashtable is 80 90% full, we need to resize it since the collison wil be maximum in tis condition.
- In this case we 'double' the size.
- If hashtable is implemented uing arrays, then it can be resized as we saw before in dyn array resize.

- Now when we have made a new array, now the hashfunction is not x% old size of array but x % newsizeofarray. so generally the hashfunction is x%N where N is the size of of array of hashtable at a given time.

- elements are not copied in the same orders, but acc to the new hash function.

#### Load Factor
- the percentage of hastable which is occupied. 
- Load factor = n/N. if 75 element are there in a 100 size hastable them loadfactor = 0.75

- In linear probing, it is recommded to keep load factor NOt more than 0.5. 
- In quadratic probing, slighlty more than 0.5

 