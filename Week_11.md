# Deletion in Red Black Tree

- if the noed to be deleted is red, the simply delete it

## If it is black

- if it has only one child it owuld be black, then promorte child and deleted N

## If it has no child

- see lecture slides boht lambi hai

# B-Tree

- B trees are multiway trees.
- it has more than two childs
- if we have n keys in a node than it can have n+1 childs.
- if a node has n childs then it has n-1 keys
- All leave nodes are at the same level
- root node should have at least two children
- In b-tree, we ensure memory management. Reduce disk usuage (load) time. Neighbouring keys are available in memory since a node contains several keys,

### 2 3 4 tree

- a variant of binary tree where each node has atleast 2 and atlmost 4 childs
- this means each nide wouldl have atleast 1 and atmost 3 keys

### 2 - 4 Tree

- similar to 2 3 4

### insertion in B trees

- when we insert in b trees, we do it like normally in binary tree. Howeever, we need to amke sure, that we are not making any new level beacuse makinga new level will violate b tree property (since all leaf nodes need to be at the same level.)
- if there are less than n number of nodes in the leaf node that are value should be inseted in, then we simply insert it. If not, then we need to perfrom an operation called 'splitting'.

### Splitting:

- IN splitting, the take the median key of the leaf node (say level m) (middle value if no of keys is odd and either of the two if no of keys is even). We 'merge' this median with the key in the node above it (level m-1) and then split the remaning values into two. One ont he right of the new key of level m-1 are the righ part of median key and on its left is the left part of the median key. The other children location remian as it is.pK


#### B Tree exercise
5 3 21 9 1 13 2 7 10 12 4 8\
```
3 5 12

        5
1 2 3     9 13 21

        5 13
1 2 3    7 9 10      21

           5 9 13
1 2 3     7    10 12      21

        2 5 9 13
1  3 4   7    10 12    21

       9
    2 5       13
1   3 4 7    12 12  21

```
- for deletion in b trees, we need 3 operations
- splitting
- merging
- rotation

## Order of Tree
- if a tree is of order 'd' , then that a-b tree has a = ceil(d/2) and b = d.

- a tree of order d can contain atmost d-1 keys and atleast ceil(d/2) - 1 keys.

- e.g a tree of order 5 has (a,b) = (3,5) and keys(min,max) = (2,4)

### Maximum Number of keys in B-tree
- of order m of height h

summation (n=1, h) m^n-1 * (m-1)^n


## Performance of B tree
- The height of a B treeo of order d is O(log_d n) ( d is the base)
- O(logd n) = O(log2 n/log2 d)

- insertion dletion is also in logarrithimic time.

******

# Handling Textual Data

# Tries
- used for pattern mathing and string macthing
- like a tree where each iteration to the leaf makes a word
- maximum 26 childs in english for each node

- In a standard trie, no word 'string' can be a prefix of another string.
- this can be solved by introducing an end marker.
- so this way, for instance, two words bell and belly both be stored.

- Height of tree is equal to the longest string
- T has s leaves. same as the no of words.

- COomplexity O(m) where n is the length of word being searched

#### Example:


## Compressed Trie
- a compressed trie ensure that each individual node in the trie ahs atleast two chidlren.
- It compresses all signle chld nodes into a single node

- Not necessarily on upto the leaf node. this can be done in the middle as well.

## Suffix Trie
- can be used for searching any substring from a single string in minimumm time
- contrcuts a tree by having individual longest common substrings on the first level and siilar in the subsequent levels

e.g
```
                             NULL
e             i       mi                  nimize       ze
             /|\        /\                  /\         
   mize | nimize | ze  nimize | ze 
```

***

For storing frequency of words in a documen (post)
Two options
- Binary Vector (stores if a word is present or not in a doc and distance determines the frequency for all docs)

- Count Vector (stores a number for each word for each record represents freqeuncy of that word in the doc)

### Problems with corpus:
- size is a big problem. One row for every word. one col for every doc
- Sparsity: an emptish vector which is under populated ( most of the entries are null/zero. relativrley few entry conveying information). e.g some words are only present in one of the docs and not other [which can usually happen].


# Inverted Index
- Anothjer solution is to use inverted index. You have words and for each word, we have a list of the numbers of docs which contain these words. Can be implement in a ditionary using hastables keyvalue pairs

- 