---
layout: post
title:      "Binary Search Tree"
date:       2019-02-11 02:03:02 +0000
permalink:  binary_search_tree
---


Today I learned about Binary Search Trees. I found a problem on LeetCode that required a binary search solution, which I at the time didn't know how to solve so I decided to learn what they are and how to solve some problems with it. 

Binary Search Tree is a tree with a root node and child nodes but every child to the left of the root node will be less than the root node, and every child to the right of the root node will be greater than the root node. 

This is an example of a Binary Search Tree:

![](https://cdncontribute.geeksforgeeks.org/wp-content/uploads/BSTSearch.png)

There should be zero numbers on the left side of the root node (8) that are greater than the number 8 and zero numbers on the right side that are less than the number 8. For each respective child of the root node, if the following number is less than the current child, the new node will be added to the left side of the current node, and vice versa for a number that's greater than the current child. 

We'll go into a problem to further clarify this: 

I found this problem in Stephen Grider's [Data Structures and Algorithm's ](https://www.udemy.com/coding-interview-bootcamp-algorithms-and-data-structure/) Udemy Course: 

1. Implement the Node class to create a binary search tree.  The constructor should initialize values 'data', 'left', and 'right'
2.  Implement the 'insert' method for the Node class. Insert should accept an argument 'data', then create an insert a new node at the appropriate location in the tree. 
3. Implement the 'contains' method for the Node class.  Contains should accept a 'data' argument and return the Node in the tree with the same value.

Using class syntax, we create the Node class to implement a binary search tree method: 

```
    class Node {
		       constructor(data) {
				   this.data = data;
				   this.left = null;
				   this.right = null; 
				}
				// initialize a node with the provided data, and the left and right child nodes with a default value of null. 
				// now we want to be able to insert a new Node at the appropriate location of the tree
				
				insert(data) {
				   let newNode = new Node(data)
					 
					 if (data < this.data && this.left ) {             
					    this.left.insert(data)
					 } else if ( data < this.data ) {
					    this.left = newNode
					 } else if (data > this.data && this.right) {
					   this.right.insert(data)
					 } else if (data > this.data) {
					   this.right = newNode
						 }
				}
		}
```

 If the data in the new Node is less than the current node *AND* there is already a child node to the left of the current node, then recursively call insert() until you reach the end node.  Once you get to the final node where there is *NOT* a child node to the left, then add the new Node as the left node. You would implement this same funcitonality for any node that's data is greater than the current node. 
 
 
 For the contains method, we want to find the node that includes the data that we pass into the argument. If there is no data that matches, we'll return null. 
 
```
   contains(data) {
	    if (data === this.data ) {
			   return this;
				 }  else if ( data < this.data && this.left) {
				    this.left.contains(data)
				 }  else if ( data > this.data && this.right) {
				    this.right.contains(data)
				 } else {
				    return null 
				}
		}
		
```

We want to provide the immediate base case, or the expression that if true, will immediately provide the result we're looking for i.e. the match to the argument. If the argument data does not match the current node data, we'll recursively call the contains method depending on whether data is less than or greater than the current node. This method will continue to be called until we either return null or return the match. 

As you can see, once you understand the concept of how binary search trees work, it is easy to solve these types of problems. 



