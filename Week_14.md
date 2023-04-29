#### Heoa DOESNOT have Binary serach propoerty

# Binary Heap Construction
- Normally make a complete binary tree

## Removal.
- Since it imlpements prioirty queue, etc, therefore the element that gets removed is the root
- We replace the root node's value with right most node value.

- Then, we traverse it down by swapping it with minumum node's valeu at each node.

# Meldable heap

- KEY OPERATION: Merging two heaps (merge(a,b))

### Merge(a , b)
- a recursive function which, at each level compares the root node of and b, and makes the minumum root as the root node of that level of the meldable tree.
- uses a randoaized number to to decide.
- Based on a random numbr, at each level except top to decide whether to merge with right or left two tres.

- Remove: remove the root and call merge on the elft and right subtrees

- analysis
- opearyion based
- conceptual