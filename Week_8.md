
# Treap

- In treap we can perform left and right rotations
- In minimum treap, the parent node's random number must be greater than that of the childs
- In maxmimum treap, the pafrent's node ran num must be greater than that of the child.

### Min heap deletion:
- We set the random value of the node to be deleted as (infinity). The idea, is we perform rortations until that node becomes a leaf and then we simply delete it. 
- for choosing rotation, we perfrom rotation with the node whose value is minumim among the two child nodes.

### Max heap deletion:
- We set the random value of the node to be deleted as (- infinity). The idea, is we perform rortations until that node becomes a leaf and then we simply delete it. 
- for choosing rotation, we perfrom rotation with the node whose value is **maximum** among the two child nodes.

### Complexity
- A rotation takes a constant time. O(1)



