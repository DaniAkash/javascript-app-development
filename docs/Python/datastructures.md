
### Why Hash Tree / Dictionary is good
* It gives the result in O(1)
* 
### Why json instead of xml
* json is faster as its hash / dict
* json takes less space than xml for the same amount of data
* json is part of all major languages, but xml needs addons to be installed.

##### Trees
It is a non-linear data structure
Trees are used in
* File Directory Structure
* DOM in html

##### Why we need interfaces
Basically for interoperability among multiple technologies

##### Array implementation of binary tree
          1
    2           3
4       5   6       7
convert this to array : 1,2,3,4,5,6,7
Left child of array 2n+1
Right child of array 2n+2
Root Of an element (n-1)/2

Complete Tree : If left are full and not none at all levels
Full Tree : No element is None

Binary Max Heap : Root always greater than children
Binary Min Heap : Root always lower than children

#### Implement Min Heap or Max using arrays

#### Get max of of a list
Use Min Heap or use some sorting and get max

#### uses of a heap
1. min or max of list
2. sorting a list etc
3. Priority Queue

#### streaming values 
store only 2 values in heap and then do a min heapify

#### File Compression - Huffman encoding
This uses binary tree as a base for encoding characters

#### Mirror of a tree

#### Get circumference of a tree

#### Get level order (vertical and horizondal)

#### Vertical Order traversal
assign weightage to each node
if you go left (child) : reduce 1
if you go right (child) : add 1


#### Tree / Forest Overall Data
* forest is collection of trees
* tree is a restricted graph (with root and it cannot be cyclic)
* Binary Search Tree is a restricted Tree
* Heap is a Tree with root restriction
* B+ is a Tree with leaf restriction
* All of these can be done in both array and linked list.

#### When to use array?
If there is insertion only in leftmost and right most we can use array.

#### When to use linked list?
If there is insertion in the middle, then we can use linked list.

#### MST (minimum spanning tree)
From a node to all other nodes what is the easiest and fastest path.
