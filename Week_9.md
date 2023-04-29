## Week 9

# AVL Trees

- a self balancing tree where the dfference between height difference between left and rightnode is not more than one.

- we assume that each leaf child has two null nodes. we assign the nu..ll nodes the hight 0. and subsequently, we assign heights to the parents.

- the difference between the hieghts of the a parent node from any of its two childs should not be more than one.FOR EVERY NODE.. IN the best case it the difference is zero.

### Contructing an AVL tree.

- We start inserting an element using BST property.

- if at some point a leaf node is inserted and there is a violation because of that at any parent node then we label that node as z and then we label the child nodes as y and x. (note that we label y and x those nodes of the branch from where the problem has arised.) For instance if we have

```
               14
             /   \
            8      16
          /  \    /  \
        4    10  15   20
       / \
      1   5
           \
            3

here when 3 inserted, there is no violation at 3, niether at 1 or 5, at 4, we still dont have any, at 8 we have a violation.

```

- - In case of unbalance tree, the violating subtree can have four possibillities. EACH of the prob and thier solution logic is given below.

#### LEFT LEFT : Right rotate z to fix it

```
     z
    / \
   y  T4
  / \           --->
 x   T3
/
T1
```

#### Left Right case: we need to perform rotation sin the follwing setps

- left rotate y
- right rotate z

```
     z
    / \
   T1  y
      / \           --->
     x   T3
     /
    T1
```

#### Right Right: left rotate z

#### Right Left: Right rotate (y), Left rotate (z)

!! idea: AVL Tree balancing using memoization.

## Exerccise

4 9 13 2 18 15 6 1

```
                        4
                           9
                              13

- Right right Case:: rotation
                    9
                 4    13
              2          18
                      15
- Right Left Case:: rotation

right rotate (y)

                    9
                 4    13
              2          15
                            18

left rotate (z)        + adding new elements

                    9
                 /     \
               4        15
             /  \      /   \
            2    6    13   18
          /
         1

```

# Red-Black Trees

- out of trepas, avl and red black, avl are the mosst balanced trwapsm but they require most rotation ops in insertion deletion.

- red black is less balnced as compared to avl but, lesser rorations used. Hnece in application requiring frequent insertions and deeltion, red blacs are preferrable.

- root node is black.
- children if any of a red node are black
- every path from a node (inlcuding that node) to any of its descendant null node has the SAME numebr of black node.

- There should not be two consecutuive red nodes

- new node is always ibserted as the red node.
## Recoloring

- Remeber node family tree

- Recoloring
- If we have two consecutive red nodes AND uncle is red than e perfrom recoloring. If the Grandfather node is not a root node, then color granfather red, and then color uncle and parent black.
-
- If two red nodes and uncle if black, then we do rotation.
- Four cases, LL, LR, RL, RR.
-
### Exercise 
4 9 13 8 2 6 7 5 21


- Deletion
Dleetion can result in the violation of red as welll as black property.





