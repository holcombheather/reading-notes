# Trees Cheat Sheet

# Tree Data Structures Cheat Sheet

## Common Terminology
- **Node**: A tree node is a component which may contain its own values and references to other nodes.
- **Root**: The root is the node at the beginning of the tree.
- **K**: A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- **Left**: A reference to one child node in a binary tree.
- **Right**: A reference to the other child node in a binary tree.
- **Edge**: The edge in a tree is the link between a parent and child node.
- **Leaf**: A leaf is a node that does not have any children.
- **Height**: The height of a tree is the number of edges from the root to the furthest leaf.

## Tree Traversals
- **Depth First**: Prioritizes going through the depth (height) of the tree first.
  - Pre-order: root >> left >> right
  - In-order: left >> root >> right
  - Post-order: left >> right >> root
- **Breadth First**: Iterates through the tree by going through each level of the tree node-by-node.

## Binary Trees Vs K-ary Trees
- **Binary Tree**: Restricts the number of children to two. There is no specific sorting order.
- **K-ary Tree**: Nodes are able have more than 2 child nodes. We use K to refer to the maximum number of children that each Node is able to have.

## Adding a Node
In a binary tree, nodes can be added wherever space allows. One strategy is to fill all "child" spots from the top down using breadth first traversal.

## Time and Space Complexity (Big O)
- For inserting a new node: O(n) time, O(w) space, where w is the largest width of the tree.
- For searching a specific node: O(n) time.
- For a perfect binary tree: Maximum width is 2^(h-1), where h is the height of the tree.

## Binary Search Trees (BST)
- In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, and all values that are larger than the root are placed to the right.
- Searching a BST is faster. If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.
- The Big O time complexity of BST's insertion and search operations is O(h), or O(height). In a balanced (or "perfect") tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.
- The Big O space complexity of a BST search would be O(1).