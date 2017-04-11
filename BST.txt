/**Binary Search Tree Implementation
** A Binary Tree is a data structure in which we have nodes containing data and two references to other nodes, one to the left
	and on to the right.

	Binary Tree consists of nodes. Nodes are nothing but objects of a class and each node has data and a link to the left node and right
	node. We call the starting node of the tree the root. 
**/

class Node{
	int data;
	Node left;
	Node right;

	//Left and Right Node of a Leaf Node points to NULL so you will know that you have reached to the end of the tree

	public Node(int data){
		this.data = data;
		left = null;
		right = null;
	}
}

/**A Binary Search Tree is a type of Binary Tree which has a special property. Nodes smaller than the root goes to the left of the root
	and nodes greater than root goes to the right of the root


Operations of a BST 

Insert(int n)
Add a node to the tree with value n. It is O(lgn)
This is very similiar to the find() operation. To insert a node our first task is to find the place to insert the node. Take current=root
Start from the current and compare root.data with n. If current.data is greater than n that means we need to go to the left of the root
If current .data is smaller than n that means we need to go to the right of the root.
If any point of time current is null that means we have reached to the leaf node, insert your node here with help from the parent code. 

Find (int n )
Find a node in the tree with value n. It is O(lgn)

Delete (int n)
Delete a node in the tree with value n. It is O(lgn)
This is more complicated than Find() and Insert() operations. Here we have to deal with 3 cases.
-Node to be deleted is a leaf node (No children)

If a node to be deleted has no children then just traverse to that node, keep track of the parent node and the side in which the node
exist (left or right) and set parent.left=null or parent.right=null

-Node to be deleted has only one child

If a node to be deleted has only one child then just traverse to that node, keep track of a parent node and the side  in which the
node exist(left or right). Check which side is null (since it only has one child). If the node to be deleted has a child on the
left side- take the entire sub tree from the left side and add it to the parent and the side which the deleted node exists.

-Node to be deleted has two children 
You cannot just replace the deleted node with any of its children. You have the find the successor of the node to be deleted. This
is the smallest node in the subtree to be deleted. 

Display() 
Prints the entire tree in increasing order. It is O(lgn)





**/

