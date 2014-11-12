# Binary Search Tree Implementation(BST)

BSTs are made up of nodes, therefore we first need to create a Node object. This object stores data and links to other nodes(left and right). We also need a show option for displaying data stored in the node.

**Node Class**
```
function Node(data, left, right) {
  this.node = data;
  this.data = left;
  this.left = right;
  this.show = show;
}

function show() {
  return this.data;
}
```

Now we need a class to represent our tree. It consists of one data member or a Node object that represents the root node of the BST, set to null which creates an empty node.

First we need and insert function to add new nodes to the tree.
The function needs the following
- A Node object, passing in the data the node will store.
- To check at insertion for a root node otherwise move to the next step.
- If the node being inserted is not the the root node then traverse the BST to find the proper insertion point. The Node object is assigned to the current node as the function moves from level to level in the BST. The Node object also has to position itself as the root node.
- The next step is to determine where to put the node. This is performed inside a loop that breaks once the correct insertion point is found.

Steps:

1. Set the root node to the current node.
2. If the data value in the inserted node is less than the data value in the current node, set the new node to be the left child of the current node and viceversa for a greater value.
3. If the value of the current child is null, insert the new node here and break. Otherwise iterate again.
4. Set the current node to be the right child of the current node.
5. If the value of the right child is null, insert the new node here and exit the loop.

**BST Class**

```
function BST() {
  this.root = null;
  this.insert = insert;
  this.inOrder = inOrder;
}

function insert(data) {
  var n = new Node(data, null, null);
  if (this.root == null) {
    this.root = n;
  } else {
    var current = this.root;
    var parent;
    while (true) {
      parent = current;
      if (data < current.data) {
        current = current.left;
        if (current === null) {
          parent.left = n;
          break;
        }
      } else {
        current = current.right;
        if (current == null) {
          parent.right = n;
          break;
        }
      }
    }
  }
}
```
#### Finding the Closet value to n

```
var findClosest = function (inputData, node) {
  var minNode;
  var minDistance = Math.infinity;
  while (node !== null) {
    if(Math.abs(node.data - inputData) < minDistance) {
      minNode = node;
      minDistance = Math.abs(node.data - inputData);
    }
    if (inputData < node.data) {
      node = node.left;
    }
    if (inputData > node.data) {
      node = node.right
    }
   }
   return minNode;
};
```
