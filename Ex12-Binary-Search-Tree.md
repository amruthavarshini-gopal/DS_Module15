# Ex12 Binary Search Tree

## DATE: 05.03.2025

## Aim:

To write a C function to insert the elements in the binary search tree

## Algorithm:

1.Start the program.
2.Check if the current node is NULL; if true, create a new node with the given key.
3.Allocate memory for the new node, set its key, and initialize its left and right children to NULL.
4.If the current node is not NULL, compare the key with the current node's key.
5.If key <= node->key, recursively insert the key into the left subtree and update the left child pointer.
6.If key > node->key, recursively insert the key into the right subtree and update the right child pointer.
7.Return the current node after the insertion.
8.End the program.

## Program:
```
/*
Program to insert the elements in the binary search tree
Developed by: Amruthavarshini Gopal
RegisterNumber: 212223230013 
*/
structnode{ int key;
struct node*left, *right;
};
struct node* insert(struct node* node, int key)
{
if(node==NULL)
{
struct node* node=(struct node*)malloc(sizeof(struct node));
node->key=key;
node->left=NULL;
 node->right=NULL;
 returnnode;
}
else
{
struct node* cur;
 if(key<=node->key)
{
cur=insert(node->left,key);
 node->left=cur;
}
 
else
{
cur=insert(node->right,key);
 node->right=cur;
}
returnnode;
}
}
```

## Output:

![438647698-b883fe30-2634-4bce-92d1-64f9b2021cd7](https://github.com/user-attachments/assets/04f7db06-6d3c-4c82-a35e-300a3667d077)


## Result:

Thus, the C function to insert the elements in the binary search tree is implemented successfully.
