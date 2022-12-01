<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Chela+One&family=Finlandica:ital,wght@1,700&display=swap" rel="stylesheet">
<h1 style="font-size:80px;font-family:Finlandica;padding-top:-100px';" align="center">Trees</h1>
<ul>
<li><a href="#intro" style="text-decoration:none">Tree Concepts</a></li>
<li><a href="#binarytree" style="text-decoration:none">Binary Tree</a></li>
<li><a href="#traverse" style="text-decoration:none">All traversals</a></li>
<li><a href="#dfs" style="text-decoration:none">Depth First Search &nbsp; </a><b> (PATTERN)</b></li>
<li><a href="#bfs" style="text-decoration:none">Breadth First Search</a><b> (PATTERN)</b></li>
<li><a href="#vs" style="text-decoration:none">DFS vs BFS</a></li>
<li><a href="#binaryprob" style="text-decoration:none">Problems on Binary Tree</a><br><br><br></li>
<li><a href="#bst" style="text-decoration:none">Binary Search Tree</a></li>
<li><a href="#bstprob" style="text-decoration:none">Problems on BST</a><br><br><br></li>
<li><a href="#pq" style="text-decoration:none">Heaps</a></li>
<li><a href="#pqprob" style="text-decoration:none">Problems on Heaps</a><br><br><br></li>
<li><a href="#trie" style="text-decoration:none">Trie</a></li>
</ul>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center" style="font-family:Finlandica;font-size:13px;">DHAYA</div>
<h1 id="intro" style="font-size:30px">Trees</h1>
A non-linear hierarchical data structure consisting of a <b>collection of nodes</b> such that each node of the tree stores a value, a list of references to nodes (the “children”).<br><br>
Each node in the tree can be connected to many children (depending on the type of tree), but must be connected to exactly one parent, except for the root node, which has no parent. These <b>connections between nodes are called edges</b> or links. By convention, trees are drawn with descendants going downwards. So, root node will be the topmost node of a tree. <br><br>
<div align="center">
<blockquote><b>We can say that a tree data structure has roots, branches, and leaves<br> connected with one another. </b></blockquote>
</div><br><br>
In contrast to linear data structures, many trees cannot be represented by relationships between neighboring nodes in a single straight line.
<br><br><br>
<h2>Some Terminology</h2><br>
<b>Parent Node:</b> A node that has links to one or more child nodes.<br>
<b>Child Node:</b> A node that is linked to an upper node (parent Node).<br>
<b>Siblings:</b> Children of the same parent node are called siblings<br>
<b>Root Node:</b> A node that doesn’t have any parent Nodes.<br>
<b>Leaf Node:</b> A node that doesn’t have any child Nodes.<br>
<b>Ancestor Nodes:</b> Nodes lying on the path from root node to that node.<br><br><br>
The figure below shows all the terminologies described above:<br>
<img style="padding-left:100px" src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/treebasics.png" height="180" width="500"><br>
PS:- The edges doesn't mean directed but pointed from parent to child.<br><br><br><br><br>
<div align="center">1</div>
<h3>Explanation:</h3>
In the figure above, 1 is the root as well as a parent node to child nodes 2, 3, and 4. Node 3 is a parent node to child nodes 6 and 7. As nodes, 2,3,4 share the same parent node 1, so they are siblings to each other. Similarly, 6 and 7 are also sibling nodes as their parent is the same, that is, 3. Consider node 7, as 1->3->7 is the path from the root node to this node, nodes 1 and 3 are said to be the ancestors of node 7.<br><br>
<h2>Subtree</h2>
A subtree is a portion of a tree that can be viewed as a <b>complete tree on its own</b>. Any node in a tree, together with all the connected nodes below it, comprise a subtree of the original tree. So, each child can be treated like the root node of its own subtree, making <b>recursion a useful technique for tree traversal</b>. <br><br>
<h2>Path</h2>
Every two nodes in a tree are connected and by exactly one path. The number of edges in a path is called the length of the path.<br><br>
<b>Depth</b> of a node n: The length of the path from a node n to the root node. The depth of the root node is 0.<br>
<b>Level</b> of a node n: (Depth of node n) + 1.<br>
<b>Height</b> of a node n: The length of the path from n to its deepest descendant. So the height of the tree itself is the height of the root node, and the height of leaf nodes is always 0.<br><br>
In the above figure for the node 3, height = 1, depth = 1, level = 2<br><br>
<h2 style="font-size:20px">Some Tree Types</h2>
Many different types of trees exist, which are optimized for particular use-cases. Each tree type offers its own particular structure and hence space-time complexity for different operations. Some commonly used trees include,<br>
<br><ul>
<li>Binary Trees</li>
<li>Binary Search Trees</li>
<li>AVL Trees</li>
<li>Red-Black Trees</li>
</ul><br><br>
<h3> N-ary Tree</h3>
An N-ary tree is a tree in which each node has no more than N children. 
<br><br><br><br><br><br><br><div align="center">2</div>
<h2 style="font-size:20px">Applications</h2><br>
The applications of tree data structures are as follows:<br><br>
• <b>Storing hierarchical data</b><br>
&nbsp;&nbsp;Tree data structures are used to store the hierarchical data, which means data<br>&nbsp; arranged in the form of order. <br> 
• <b>Binary Search Tree</b><br>
&nbsp;&nbsp;It is a type of tree data structure that helps in maintaining a sorted stream of<br>&nbsp; data. Used for efficient searching and finding the closest item. <br>
• <b>Heap</b><br>
&nbsp;&nbsp;It is also a tree data structure that can be represented in a form of array. It is<br>&nbsp; used to implement priority queues. Used for efficient sorting. <br>
• <b>Syntax tree</b><br>
&nbsp;&nbsp;Scanning, parsing , generation of code and evaluation of arithmetic expressions in<br>&nbsp; Compiler design.<br>
• <b>Trie</b><br>
&nbsp;&nbsp;It is the fast and efficient way for dynamic spell checking. It is also used for<br>&nbsp; locating specific keys from within a set. <br>
• <b>K-D Tree:</b><br>
&nbsp;&nbsp;A space partitioning tree used to organize points in K dimensional space.<br>
• <b>B-Tree and B+ Tree </b><br>
&nbsp;&nbsp;Used to implement indexing in databases. <br>
• <b>Spanning trees</b><br>
&nbsp;&nbsp;It is the shortest path tree used in the routers to direct the packets to the<br>&nbsp; destination.<br>
• <b>Decision trees</b><br>
&nbsp;&nbsp;Used in machine learning<br><br><br>
Also, JSON and YAML documents can be thought of as trees, but are typically represented by nested lists and dictionaries.<br><br><br><br>
<h2>POINTS TO NOTE</h2>
- Recursion lies in the heart of trees<br>
- Are you missing the first line: root == NULL check<br>

<br><br><br><br><br><br><br><br><br>
<div align="center">3</div>
<h1 style="font-size:30px" id="binarytree">BINARY TREE</h1>
<div style="display:flex">
<div>
Binary trees are a commonly used tree, which <b>constrain&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;   the number of children</b> for each parent <b>to exactly two</b>. We&nbsp; &nbsp; &nbsp;  can refer to these children as the left and the right child. <br><br>
A recursive definition using just set theory notions is&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  that a (non-empty) binary tree is a tuple (L, S, R),&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  where L and R are binary trees or the empty set and S&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; is a singleton set containing the root.<br>
</div>
<img src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/binarytree.png" height="150" width="150">
</div>
<br>
A binary tree is a special case of a ordered N-ary tree, where N is 2.
A Binary Tree node contains following parts. <br>
- Data<br>
- Pointer to left child<br>
- Pointer to right child<br><br><br><br>

<h2>Types of Binary Trees</h2>
<h3>Complete Binary Trees</h3>
A binary tree is a complete binary tree if all the levels are completely filled except possibly the last level and the last level has all keys as left as possible  <br>
<h3>Full Binary Trees</h3>
A binary tree is a full binary tree if every node has 0 or 2 children.
<h3>Perfect Binary Trees</h3>
A binary tree is said to be perfect if it is both full and complete. <br>
<h3>Degenerate (or pathological) tree</h3>
A tree where each parent node has one child node. This means that the tree will behave like a linked list data structure.
<h3>Skewed tree</h3>
A binary tree in which each node has either one or no child.<br>
In this type of tree, either all nodes are positioned to the left or the right. <br><br><br>
<b>Note</b>:- While solving any problems involving trees, take care of the base cases<br> i.e. root = NULL<br><br><br><br><br><br><div align="center">4</div>
<h1 style="font-size:30px" id="traverse">Traversal</h1>
Tree traversal refers to the <b>process of visiting each node</b> in a tree data structure, exactly once.<br> 
Unlike linked lists, one-dimensional arrays and other linear data structures, which are canonically traversed in linear order, trees may be traversed in multiple ways.<br><br>
They may be traversed in depth-first or breadth-first order. Such traversals are classified by the order in which the nodes are visited.<br>
The following algorithms are described for a binary tree, but they may be generalized to other trees as well.<br><br>
<div style="display:flex;padding-left:80px">
<img src="https://media.geeksforgeeks.org/wp-content/cdn-uploads/level_order_traversal.png" width="200" height="220">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<div>
<br><br>
preorder: 1 2 4 5 3 <br>
inorder: 4 2 5 1 3 <br>
postorder: 4 5 2 3 1 <br><br>
levelorder: 1 2 3 4 5 <br>
zigzag level order: 1 3 2 4 5 <br>
reverse level order: 4 5 2 3 1 <br><br>
diagonal order: 1 3 2 5 4 <br>
boundary order: 1 2 4 5 3<br>
vertical order: 4 2 1 5 3
</div></div><br><br><br>
<h1>Traversal Problems</h1>
Inorder&nbsp;&nbsp; <a href="https://leetcode.com/problems/binary-tree-inorder-traversal/">problem</a> <a href="#inrec">recursive</a> <a href="#inite">iterative</a> <br>
Preorder&nbsp; <a href="https://leetcode.com/problems/binary-tree-preorder-traversal/">problem</a> <a href="#prerec">recursive</a> <a href="#preite">iterative</a> <br>
Postorder <a href="https://leetcode.com/problems/binary-tree-postorder-traversal/">problem</a> <a href="#postrec">recursive</a> <a href="#postite">iterative</a> <br><br>
Levelorder <a href="https://leetcode.com/problems/binary-tree-level-order-traversal/">problem</a> <a href="#level">solution</a> <br>
Zigzag level order <a href="https://leetcode.com/problems/binary-tree-zigzag-level-order-traversal/">problem</a> <a href="#zlevel">solution</a> <br>
Reverse level order <a href="https://leetcode.com/problems/binary-tree-level-order-traversal-ii/">problem</a> <a href="#rlevel">solution</a> <br><br>
Diagonal order <a href="https://practice.geeksforgeeks.org/problems/diagonal-traversal-of-binary-tree/1">problem</a> <a href="#diagonal">solution</a> <br>
Boundary order <a href="https://practice.geeksforgeeks.org/problems/boundary-traversal-of-binary-tree/1/">problem</a> <a href="#boundary">solution</a> <br>
Vertical order <a href="https://practice.geeksforgeeks.org/problems/print-a-binary-tree-in-vertical-order/1">problem</a> <a href="#vertical">solution</a><br><br>
Construct Binary Tree from Preorder and Inorder Traversal <a href="https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/">problem</a> <a href="#constructree">solution</a><br><br><br><br><br><div align="center">5</div>
<h1 id="dfs">Depth first order - DFS</h1>
We go as deep as we can to look for a value, and when there is nothing new to discover, we retrace our steps to find something new. In other words, it travels as far as possible along each tree branch before exploring the others.<br>
There are three common ways to traverse them in depth-first order: in-order, pre-order and post-order<br><br>
<h3>in-order (LDR)</h3>
A traversal in which a node's left subtree, then the node itself, and finally its right subtree are traversed.<br>
<h3>pre-order (DLR)</h3>
A traversal in which the parent node is traversed before its children.<br>
Most commonly used variation of the depth-first search.<br>
<h3>post-order (LRD)</h3>
A traversal in which the parent node is traversed after its children.<br>
Perhaps the rarest of the three when it comes to solving problems.<br><br><br>
Imagine deleting a tree. If we use preorder traversal and delete the root node, first, we would lose the pointers to the left and right subtrees and wouldn’t be able to delete those. That’s a memory leak. If we use inorder traversal and delete the left child followed by the root, the right subtree couldn’t be deleted. If we use the postorder traversal and delete the root node after deleting both the subtrees, then we get the desired result.<br><br>
These specifically assumes a binary tree as it is referring exactly to two subtrees.<br><br><br>
<h3>Complexities</h3>
The time complexity of the algorithm is O(N), where N is the total number of nodes in the tree as we traverse each node once.<br><br>
The space complexity of the algorithm is also O(N) as we need O(N) space for the stack. Since we can have a skewed tree where with each node, depth increases.<br><br><br>
<h2>How to identify the DFS pattern:</h2>
If the problem involves traversing trees sudch that components of the solution are listed along paths from the root to the leaves and finding the optimal solution requires traversal along these paths. The classic example of this is finding the height of the given tree.<br><br>
<br><br><br><div align="center">6</div>
<h1>Recursive implementations</h1>

```cpp
vector<int> depthFirstTraversal(Node* root){
    vector<int> res;
    xyzorder(root, res);
    return res;
}
```

All the three depth first traversals can be used in the place of <span style="background-color:#eee; border-radius: 2px;"><i>&nbsp;xyzorder&nbsp;</i></span><br><br>
<h2 id="inrec">Inorder</h2>

```cpp
void inorder(Node* root, vector<int> &res) {
    if (root == NULL) return;
    inorder(root->left, res);
    res.push_back(root->val);
    inorder(root->right, res);
}
```
<br><h2 id="prerec">Preorder</h2>

```cpp
void preorder(Node* root, vector<int> &res) {
    if (root == NULL) return;
    res.push_back(root->val);
    preorder(root->left, res);
    preorder(root->right, res);
}
```
<br><h2 id="postrec">Postorder</h2>

```cpp
void postorder(Node* root, vector<int> &res) {
    if (root == NULL) return;
    postorder(root->left, res);
    postorder(root->right, res);
    res.push_back(root->val);
}
```
<br><br><br><br><br><div align="center">7</div>
<h1>Iterative implementations</h1><br>
Stack is a useful data structure to convert a recursive code into an iterative code. Under the hood, the compiler uses a call stack to convert a recursive code into an iterative code.<br><br>
<h2 id="preite">Preorder - DLR</h2><br>

```cpp
vector<int> preorderTraversal(Node* root) {
    vector<int> res;
    if (root == NULL) return res;
    stack<Node*> s;
    s.push(root);
        
    while(!s.empty()){
        Node* temp = s.top();
        s.pop();
        
        // when you visit a node, print its data first
        res.push_back(temp->val);
        
        // then you take the left and then right
        // but since, its a stack you have to do it reverse
        if (temp->right) s.push(temp->right);
        if (temp->left) s.push(temp->left);
    }
        
    return res;
}
```
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">8</div>
<h2 id="postite">Postorder - LRD</h2><br>
We can do this in the same way as iterative preorder.<br>
We will find DRL (DLR in above) and then reverse it.<br><br><br>

```cpp
vector<int> postorderTraversal(TreeNode* root) {
    vector<int> res;
    if (root == NULL) return res;
    stack<TreeNode*> st;
    st.push(root);
    
    while (!st.empty()) {
        TreeNode* temp = st.top();
        if (temp->left) {
            // first preference to left
            st.push(temp->left);
            temp->left = NULL;
        }
        else if (temp->right) {
            // and then to right
            st.push(temp->right);
            temp->right = NULL;
        } else {
            // don't make a node visited until its left and right are visited
            res.push_back(temp->val);
            st.pop();
        } 
    }
    
    return res;
}
```
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">9</div>
<h2 id="inite">Inorder - LDR</h2>

```cpp
vector<int> inorderTraversal(Node* root) {
    vector<int> res;
    if (root == NULL) return res;
    stack<Node*> s;
    Node* cur = root;
        
    while(cur || !s.empty()) {
        // at any point always try to reach the leftmost node (L)
        while (cur != NULL) {
            s.push(cur);
            cur = cur->left;
        }
        
        // when it is NULL, process its parent node as we are sure now
        // left subtree is completed (D)
        Node* temp = s.top();
        s.pop();
        res.push_back(temp->val);
        
        // after processing a node, reach to its right subtree (R)
        cur = temp->right;
    }
        
    return res;
}
```
<br><br>
Time complexity: O(n)<br>
Space complexity: O(log n)<br><br>
Morris traversal can perform this in O(1) extra space.
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center" style="font-family:Finlandica;font-size:13px;">DHAYA</div>
<h1 id="bfs" style="font-size:30px">Breadth first order - BFS</h1><br>
A level-order traversal effectively performs a breadth-first search over the entirety of a tree; nodes are <b>traversed level by level</b>, where the root node is visited first, followed by its direct child nodes and their siblings, followed by its grandchild nodes and their siblings, etc., until all nodes in the tree have been traversed.<br><br>
<div style="padding-left:100px"><b>
DFS: Where is my baby (child) ?<br>
BFS: Where are my siblings or am i born alone ?
</b></div><br>
To keep track of the child nodes that were encountered but not yet explored, While DFS uses recursion/stack, BFS uses a queue (First In First Out). <br><br><br>
<h3>Extra points</h3>
<ul>
<li>Visits all the nodes in a level before starting to visit the next level.</li>
<li>At any time, the queue contains at most two levels of nodes. We will smartly use the situation when the queue contains exactly one level of nodes while solving problems.</li>
</ul><br><br>
<h3>Complexities</h3>
The time complexity of the algorithm is O(N), where N is the total number of nodes in the tree as we traverse each node once.<br><br>
The space complexity of the algorithm is also O(N) as we need O(N) space for the queue.  Since we can have a maximum of N/2 nodes at a level (this could happen only at the last level), therefore we will need O(N) space to store them in the queue.<br><br><br><br>
<h2>How to identify the BFS pattern:</h2>
If the problem involves traversing trees in a level-by-level fashion (breadth-first search manner), it can be efficiently solved using this approach.<br><br>
<br><br><br><br><br><br><br><br><br><br><div align="center">11</div>
<h2>Problems featuring this pattern</h2>
<ul>
<li>Various types of <b>tree traversals</b> such as level order, zigzag order etc ... as they need to traverse the tree by level</li>
<li><b>Left and Right views</b>: As when the queue contains exactly one level of nodes, the first of them will be a part of the left view and the last of them will be a part of the right view</li>
<li><b>Minimum depth</b> of a tree: Since we search level by level, we are guaranteed to find the shallowest leaf node earlier than other leaf nodes.<br>
Note: But for finding the maximum depth, both are equally efficient interms of time as we need to visit each node.</li>
<li>Level averages, largest value on each level of a tree etc.. </li>
<li>Next right node of a given key, Connect Level Order Siblings
</ul>
<br><br><br><br><h2 id="level">Level order implementation</h2>

```cpp
vector<vector<int>> levelOrder(Node* root) {
    vector<vector<int>> res;
    if (root == NULL) return res;
    queue<Node*> q;
    q.push(root);
        
    while (!q.empty()) {
        int size = q.size();
        vector<int> level;
        // as we know the number of nodes present in a current level,
        // the children we are going to visit, will move to the queue
        // but gets stored in the next level
        
        while (size--) {
            Node* temp = q.front();
            q.pop();
            level.push_back(temp->val);
            if (temp->left) q.push(temp->left);
            if (temp->right) q.push(temp->right);
        }
        res.push_back(level);
    }
    
    return res;
}
```

<br><br><br><br><div align="center">12</div>
<h2>Connect Level Order Siblings</h2>
Given a binary tree, connect each node with its level order successor(right node). The last node of each level should point to a null node.<br><br>

```cpp
void connect(Node *root) {
    queue<TreeNode*> q;
    q.push(root);
    
    while (!q.empty()){
        int size = q.size();
        while (size--) {
            Node* temp = q.front();
            q.pop();
            if (temp->left) q.push(temp->left);
            if (temp->right) q.push(temp->right);
            if (size == 0) temp->next = NULL;
            else temp->next = q.front();
        }
    }
  } 
```
<br><br><br>
If the problem says "the last node of each level should point to the first node of the next level", modify the if condition as follows:

```cpp
if (!q.empty()) temp->next = q.front();
else temp->next = NULL;
```
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">13</div>
<h2 id="zlevel">Zig Zag Level order</h2>

```cpp
vector<vector<int>> zigzagLevelOrder(Node* root) {
    vector<vector<int>> res;
    if (root == NULL) return res;
    queue<Node*> q;
    q.push(root);
    bool isOddLevel = true;
    
    while (!q.empty()) {
        int size = q.size();
        vector<int> level;
        
        while (size--) {
            Node* temp = q.front();
            q.pop();
            level.push_back(temp->val);
            if (temp->left) q.push(temp->left);
            if (temp->right) q.push(temp->right);
        }
        
        if (!isOddLevel) reverse(level.begin(), level.end());
        res.push_back(level);
        isOddLevel = !isOddLevel;
    }
    return res;
}
```
<br><br>
<h2 id="rlevel">Reverse Level Order</h2>
<ul>
<li>We will maintain a stack of vectors.</li>
<li>After having each level of nodes in the vector, we will push it to the stack, so that the top of the stack contains the last level and the bottom of the stack contains the first level (only root). </li>
<li>After traversing, we will push the top of the stack into result vector until the stack is empty.</li>
</ul>
<br><br><br>
Else, just add this to the level order traversal code before returning.

```cpp
reverse(res.begin(), res.end());
```
<br><br><br><div align="center">14</div>
<h2 id="diagonal">Diagonal Order</h2>
If the diagonal element are present in two different subtress then left subtree diagonal element should be taken first and then right subtree.<br><br>

```cpp
void dlr(Node*root, int dval, map<int, vector<int>> &mp){
    if (root == NULL) return;
    mp[dval].push_back(root->val);
    dlr(root->left,dval+1,mp);
    dlr(root->right,dval,mp);
}

vector<int> diagonal(Node *root)
{
   vector<int> res;
   map<int, vector<int>> mp;
   dlr(root, 0, mp);
   for (auto it : mp) {
       res.insert(res.end(), it.second.begin(), it.second.end());
   }
   return res;
}
```

<br><br><br>
Aliter,

```cpp
vector<int> diagonal(Node *root)
{
    vector<int> res;
    if (root==NULL) return res;
    queue<Node*> q;
    q.push(root);
    
    while (!q.empty()){
        Node* temp = q.front();
        q.pop();
        while (temp) {
            res.push_back(temp->data);
            if (temp->left) q.push(temp->left);
            temp = temp->right;
        }
    }
    return res;
}
```
<br><br><br><div align="center">15</div>
<h1 id="boundary">Boundary traversal</h1>
Given a Binary Tree, find its Boundary Traversal. The traversal should be in the following order: <br><br>
<b>Left boundary nodes</b>: defined as the path from the root to the left-most node ie- the leaf node you could reach when you always travel preferring the left subtree over the right subtree. <br>
<b>Leaf nodes</b>: All the leaf nodes except for the ones that are part of left or right boundary.<br>
<b>Reverse right boundary nodes</b>: defined as the path from the right-most node to the root. The right-most node is the leaf node you could reach when you always travel preferring the right subtree over the left subtree. Exclude the root from this as it was already included in the traversal of left boundary nodes.<br><br>
<b>Note</b>: If the root doesn't have a left subtree or right subtree, then the root itself is the left or right boundary. <br><br><br>
<h2>Solution</h2>
The complexity of this problem lies in separating this into separate problems so as to not to print any node twice. Care must be taken while writing code as the every two of the three can intersect.<br><br>
Also note that left boundary doesn't mean the path from root to the left node obtained while continously going left. The left boundary can have right pointers to when the nodes doesn't have left pointers.
<br><br><br><b>Solution starts in the next page.</b><br><br><br>

```cpp
// Helper function to print leaves
void lr(Node *root, vector<int> &res){
        if (root==NULL) return;
        if (root->left==NULL && root->right==NULL) {
            // print the leaf node
            res.push_back(root->data);
        } else {
            // left leaves should be printed before right ones always
            lr(root->left, res);
            lr(root->right, res);
        }
    }
```
<br><br><br>
<div align="center">16</div>

```cpp
vector <int> boundary(Node *root){
    vector<int> res;
    if (root==NULL) return res;
    // 1. print root first
    res.push_back(root->data);               
    
    // 2. left boundary except the leaf
    Node* temp = root->left;
    while (temp) {
        if (temp->left || temp->right) res.push_back(temp->data);
        // first priority to left child at each step
        if (temp->left) temp = temp->left;
        else temp = temp->right;
    }
    
    // 3. print all the leaves
    if (root->left || root->right) lr(root, res);
    
    // 4. right boundary except the leaf
    stack<int> s;
    temp = root->right;
    while (temp) {
        if (temp->left || temp->right) s.push(temp->data);
        // first priority to right child at each step
        if (temp->right) temp = temp->right;
        else temp = temp->left;
    }
    // reversing using stack
    while (!s.empty()) {
        res.push_back(s.top());
        s.pop();
    }

    return res;
}
```
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">17</div>
<h1 id="vertical">Vertical order traversal</h1><br><br>

```cpp
vector<int> verticalOrder(Node *root)
{
    vector<int> res;
    if (root==NULL) return res;
    
    map<int, vector<int>> mp;
    unordered_map<Node*, int> dist;
    queue<Node *> q;
    q.push(root);
    dist[root] = 0;
    
    while(!q.empty()) {
        Node* temp = q.front();
        q.pop();
        mp[dist[temp]].push_back(temp->data);
        
        if (temp->left) {
            dist[temp->left] = dist[temp]-1;
            q.push(temp->left);
        }
        if (temp->right) {
            dist[temp->right] = dist[temp]+1;
            q.push(temp->right);
        }
    }
    
    for (auto it:mp) res.insert(res.end(), it.second.begin(), it.second.end());
    return res;
}
```
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">18</div>
<h1 id="constructree">Construct Binary Tree from Preorder and Inorder Traversal</h1>
<br><br><br>

```cpp
TreeNode* buildTreeFunc(vector<int>& preorder, vector<int>& inorder, int preStart, int preEnd, int inStart, int inEnd) {
    if (inStart > inEnd) return NULL;
    
    int rootIndex;
    // index of current root element in current inorder
    for (int i=inStart; i<=inEnd; i++) {
        if (inorder[i] == preorder[preStart]) {
            rootIndex = i;
            break;
        }
    }
    
    TreeNode* root = new TreeNode(preorder[preStart]);
    // left subtree size
    int lsize = rootIndex - inStart;
    
    root->left = buildTreeFunc(preorder, inorder, preStart+1, preStart+lsize, inStart, rootIndex-1);
    root->right = buildTreeFunc(preorder, inorder, preStart+lsize+1, preEnd, rootIndex+1, inEnd);
    return root;
}

TreeNode* buildTree(vector<int>& preorder, vector<int>& inorder) {
    return buildTreeFunc(preorder, inorder, 0, preorder.size()-1, 0, inorder.size()-1);
}
```
<br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">19</div>
Consider three depth first search traversals, (inorder, preorder and postorder)<br>
<ul>
<li>If all the three traversals are given, then there will be one unique tree constructed from it.</li>
<li>If two of the three traversals are given, then there will be one unique tree constructed from it and we can also find the other traversal.</li>
<li>If only one traversal is given, then there can be many trees constructed from it. A unique tree is not possible.</li>
</ul>
<br><br><br><br><br>
<h1 id="vs">DFS vs BFS</h1>
DFS is essentially pre-order tree traversal.<br><br>
DFS is better at:
<ul>
<li>finding nodes far away from the root</li>
<li>wide trees</li>
<li>best in implementing recursion</li>
<li>implemeting parent, ancestor relationships without using additional data structure</li>
</ul><br>
BFS is better for:
<ul>
<li>finding nodes close/closest to the root</li>
<li>deep trees</li>
<li>best in finding shortest distances</li>
</ul>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center" style="font-family:Finlandica;font-size:13px;">DHAYA</div>
<h1 id="binaryprob">Problems on Binary trees</h1><br>
Height of a binary tree &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 
<a href="https://practice.geeksforgeeks.org/problems/height-of-binary-tree/1">problem</a> <a href="#height">solution</a><br>
Diameter of a binary tree &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 
<a href="https://leetcode.com/problems/diameter-of-binary-tree/">problem</a> <a href="#diameter">solution</a><br><br>
Maximum sum leaf to root path &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
<a href="https://leetcode.com/problems/binary-tree-level-order-traversal/">problem</a> <a href="#maximumsumpath">solution</a><br>
Sum of the longest leaf to root path &nbsp; &nbsp; &nbsp;<a href="https://leetcode.com/problems/binary-tree-level-order-traversal/">problem</a> <a href="#longlensum">solution</a><br><br>
Check if binary tree is Sum Tree &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; 
<a href="https://practice.geeksforgeeks.org/problems/sum-tree/1">problem</a> <a href="#sumtreecheck">solution</a><br>
Transform to Sum Tree &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <a href="https://practice.geeksforgeeks.org/problems/transform-to-sum-tree/1">problem</a> <a href="#sumtree">solution</a><br><br>
Views of a tree<br>
Left view of a tree &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;
<a href="https://practice.geeksforgeeks.org/problems/left-view-of-binary-tree/1">problem</a> <a href="#leftview">solution</a><br>
Right view of a tree &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;<a href="https://practice.geeksforgeeks.org/problems/right-view-of-binary-tree/1">problem</a> <a href="#rightview">solution</a><br>
Top view of a tree &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;
<a href="https://practice.geeksforgeeks.org/problems/top-view-of-binary-tree/1">problem</a> <a href="#topview">solution</a><br>
Bottom view of a tree &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <a href="https://practice.geeksforgeeks.org/problems/bottom-view-of-binary-tree/1">problem</a> <a href="#bottomview">solution</a><br><br>
Symmetric Tree &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; <a href="https://leetcode.com/problems/binary-tree-level-order-traversal/">problem</a> <a href="#rightview">solution</a><br>
Invert Binary Tree (mirror) &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 
<a href="https://leetcode.com/problems/invert-binary-tree/">problem</a> <a href="#topview">solution</a><br>
Check if Binary Tree is Isomorphic &nbsp; &nbsp; &nbsp;&nbsp; <a href="https://leetcode.com/problems/binary-tree-level-order-traversal/">problem</a> <a href="#bottomview">solution</a><br><br>
Construct Binary Tree from String &nbsp; &nbsp; &nbsp; &nbsp; <a href="https://www.codingninjas.com/codestudio/problems/binary-tree-from-bracket_1118117">problem</a> <a href="#constructstring">solution</a><br>
Convert Binary tree into DLL &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; <a href="https://practice.geeksforgeeks.org/problems/binary-tree-to-dll/1">problem</a> <a href="#constructll">solution</a><br>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">21</div>
<h1 id="height">Height of a binary tree</h1>
The length of the path from root to its deepest descendant(leaf).<br><br>

```cpp
int height(Node* root){
    if (root == NULL) return 0;
    return 1 + max(height(root->left), height(root->right));
}
```

<br><br><br><br><br><h1 id="diameter">Diameter of a binary tree</h1>
Given the root of a binary tree, return the length of the diameter of the tree.<br>
The diameter of a binary tree is the length of the longest path between any two nodes in a tree. This path may or may not pass through the root.<br>
The length of a path between two nodes is represented by the number of edges between them.<br><br><br>

```cpp
int heights(Node* root, int &maxLen) {
    if (root == NULL) return 0;
    int left = heights(root->left, maxLen);
    int right = heights(root->right, maxLen);
    
    // At any node, the maximum possible length involving it is the sum of heights of the node using left and right subtrees. We will be smartly using recursion to return the heights each time.
    if ((left + right) > maxLen) maxLen = left + right;
    return 1 + max(left, right);
}

int diameterOfBinaryTree(Node* root) {
    int maxLen = 0;
    heights(root, maxLen);
    return maxLen;
}
````
<br><br><br><br><br><div align="center">22</div>
<h1 id="maximumsumpath">Maximum sum leaf to root path</h1>

```cpp
void func(Node* root, int sum, int &maxSum) {
    if (root == NULL) return;
    sum += root->data;
    if (root->left == NULL && root->right == NULL) {
        if (sum > maxSum) maxSum = sum;
    } else {
        func(root->left, sum, maxSum);
        func(root->right, sum, maxSum);
    }
}
int maxPathSum(Node* root)
{
    if (root==NULL) return 0;
    int maxSum = INT_MIN;
    func(root, 0, maxSum);
    return maxSum;
}
```

<br><br><h1 id="longlensum">Sum of the longest leaf to root path</h1>
If two or more paths compete for the longest path, then the path having maximum sum of nodes is being considered.<br>

```cpp
void func(Node* root, int len, int sum, int &maxLen, int &ans) {
    if (root==NULL) return;
    sum += root->data;
    if (len > maxLen) {
        maxLen = len;
        ans = sum;
    } else if (len == maxLen) {
        ans = max(ans, sum);
    }
    func(root->left, len+1, sum, maxLen, ans);
    func(root->right, len+1, sum, maxLen, ans);
}
int sumOfLongRootToLeafPath(Node *root)
{
    if (root==NULL) return 0;
    int maxLen=-1, ans=0;
    func(root, 0, 0, maxLen, ans);
    return ans;
}
```
<div align="center">23</div>
<h1>Check if binary tree is Sum Tree</h1>
<h2 id="sumtreecheck">Sum Tree</h1>
A Binary Tree where the value of a node is equal to the sum of the nodes present in its left subtree and right subtree.<br><br>

```cpp
bool isSumTree(Node* root)
{
    if (root == NULL) return true;
    if (root->left == NULL && root->right == NULL) return true;
    if (!isSumTree(root->left) || !isSumTree(root->right)) return false;
    int sum = 0;
    if (root->left) {
        sum += root->left->data;
        if (!isLeaf(root->left)) sum += root->left->data;
    }
    if (root->right) {
        sum += root->right->data;
        if (!isLeaf(root->right)) sum += root->right->data;
    }
    return (root->data == sum);
}
```
<br><br><br>
Aliter,

```cpp
int dfs(Node* root) {
    if (root == NULL) return 0;
    if (root->left==NULL && root->right==NULL) return root->data;
    int leftSum = dfs(root->left);
    int rightSum = dfs(root->right);
    if (leftSum == -1 || rightSum == -1) return -1;
    if (root->data != leftSum + rightSum) return -1;
    return 2*root->data;
}

bool isSumTree(Node* root) {
    return (dfs(root) != -1);
}
```
<br><br><br><br><br><br><div align="center">24</div>
<h1 id="sumtree">Transform to Sum Tree</h1>
Given a Binary Tree, where each node can have positive or negative values. Convert this to a tree where each node contains the sum of the left and right sub trees of the original tree. The values of leaf nodes are changed to 0.
<br><br>

```cpp
void toSumTree(Node *root)
{
    if (root == NULL) return;
    int left = 0, right = 0;
    if (root->left) {
        left = root->left->data;
        toSumTree(root->left);
        left += root->left->data;
    }
    if (root->right) {
        right = root->right->data;
        toSumTree(root->right);
        right += root->right->data;
    }
    root->data = left + right;
}
```
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div align="center">25</div>
<h1 style="">Views of a tree</h1>
For a binary tree, there exists four types of views.<br><br>

- <b> Left View :</b><br>
The set of nodes visible when the tree is viewed from the left side.
- <b> Right View :</b><br>
The set of nodes visible when the tree is viewed from the right side.
- <b> Top View :</b><br>
The set of nodes visible when the tree is viewed from the top.
- <b> Bottom View :</b><br>
The set of nodes visible when the tree is viewed from the bottom.

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br><br><div align="center">26</div>
<h2 id="leftview">Left View</h2>
<h3>DFS implementation</h3>

```cpp
void dlr(Node* temp, int level, int &maxLevel, vector<int> &res) {
    if (temp==NULL) return;
    if (level>maxLevel) {
        res.push_back(temp->data);
        maxLevel = level;
    }
    dlr(temp->left,level+1,maxLevel,res);
    dlr(temp->right,level+1,maxLevel,res);
}
vector<int> leftView(Node *root)
{
    vector<int> res;
    int maxLevel = -1;
    dlr(root,0,maxLevel,res);
    return res;
}
```
<br><h3>BFS implementation</h3>

```cpp
vector<int> leftView(Node *root)
{
   vector<int> res;
   if (root==NULL) return res;
   queue<Node*> q;
   q.push(root);
   bool isLeftNode = true;
   
   while(!q.empty()){
        int size = q.size();
        while(size--) {
            Node* temp = q.front();
            q.pop();
            if (isLeftNode) {
                res.push_back(temp->data);
                isLeftNode = false;
            }
            if (temp->left) q.push(temp->left);
            if (temp->right) q.push(temp->right);
       }
       isLeftNode = true;
   }
   return res;
}
```
<div align="center">27</div>
<h2 id="rightview">Right View</h2>
<h3>DFS implementation</h3>

```cpp
void drl(Node* temp, int level, int &maxLevel, vector<int> &res) {
    if (temp==NULL) return;
    if (level>maxLevel) {
        res.push_back(temp->data);
        maxLevel = level;
    }
    drl(temp->right,level+1,maxLevel,res);
    drl(temp->left,level+1,maxLevel,res);
}
vector<int> rightView(Node *root)
{
    vector<int> res;
    int maxLevel = -1;
    drl(root,0,maxLevel,res);
    return res;
}
```
<br><br><h3>BFS implementation</h3>

```cpp
vector<int> rightView(Node *root)
{
    vector<int> res;
    if (root==NULL) return res;
    queue<Node*> q;
    q.push(root);
    
    while(!q.empty()){
        int size = q.size();
        int lastNode;
        while(size--) {
            Node* temp = q.front();
            q.pop();
            lastNode = temp->data;
            if (temp->left) q.push(temp->left);
            if (temp->right) q.push(temp->right);
        }
        res.push_back(lastNode);
    }
    return res;
}
```
<br><br><div align="center">28</div>

<h2 id="topview">Top View </h2>
DFS implementation

```cpp
void dlr(Node* root, map<int, pair<int,int>> &mp, int vlevel, int hlevel) {
    if (root==NULL) return;
    if (mp.find(vlevel) == mp.end() || mp[vlevel].second > hlevel) {
        mp[vlevel] = {root->data,hlevel};
    }
    dlr(root->left,mp,vlevel-1,hlevel+1);
    dlr(root->right,mp,vlevel+1,hlevel+1);
}
vector<int> topView(Node *root)
{
    vector<int> res;
    map<int, pair<int,int>> mp;
    dlr(root, mp, 0, 0);
    for (auto it:mp) {
        res.push_back(it.second.first);
    }
    return res;
}
```
<br>BFS implementation

```cpp
vector<int> topView(Node *root)
{
    vector<int> res;
    if (root==NULL) return res;
    map<int, int> mp;
    unordered_map<Node*, int> dist;
    queue<Node *> q;
    q.push(root);
    dist[root] = 0;
    while (!q.empty()) {
        Node* temp = q.front();
        q.pop();
        if (mp.find(dist[temp]) == mp.end()) mp[dist[temp]] = temp->data;
        if (temp->left) {
            q.push(temp->left);
            dist[temp->left] = dist[temp]-1;
        }
        if (temp->right) {
            q.push(temp->right);
            dist[temp->right] = dist[temp]+1;
        }
    }
    for (auto it:mp) res.push_back(it.second);
    return res;
}
```
<div align="center">29</div>
<h2 id="bottomview">Bottom View</h2>
DFS implementation

```cpp
void dlr(Node* root, map<int, pair<int,int>> &mp, int vlevel, int hlevel) {
    if (root==NULL) return;
    if (mp.find(vlevel) == mp.end() || mp[vlevel].second <= hlevel) {
        mp[vlevel] = {root->data,hlevel};
    }
    dlr(root->left,mp,vlevel-1,hlevel+1);
    dlr(root->right,mp,vlevel+1,hlevel+1);
}
vector<int> bottomView(Node *root)
{
    vector<int> res;
    map<int, pair<int,int>> mp;
    dlr(root, mp, 0, 0);
    for (auto it:mp) {
        res.push_back(it.second.first);
    }
    return res;
}
```
<br>BFS implementation

```cpp
vector <int> bottomView(Node *root) {
    vector<int> res;
    if (root==NULL) return res;
    map<int, int> mp;
    unordered_map<Node*, int> dist;
    queue<Node *> q;
    q.push(root);
    dist[root] = 0;
    while (!q.empty()) {
        Node* temp = q.front();
        q.pop();
        mp[dist[temp]] = temp->data;
        if (temp->left) {
            q.push(temp->left);
            dist[temp->left] = dist[temp]-1;
        }
        if (temp->right) {
            q.push(temp->right);
            dist[temp->right] = dist[temp]+1;
        }
    }
    for (auto it:mp) res.push_back(it.second);
    return res;
}
```
<div align="center" style="font-family:Finlandica;font-size:13px;">DHAYA</div>
<h1>Symmetric Tree</h1>
Given the root of a binary tree, check whether it is a mirror of itself (i.e., symmetric around its center).
<br><br><br>

```cpp
// Helper function to check two trees are mirrors of each other
bool areMirror(Node* r1, Node *r2){
    if (r1 == NULL && r2 == NULL) return true;
    if (r1 == NULL || r2 == NULL) return false;
    if (r1->val != r2->val) return false;
    return (areMirror(r1->left,r2->right) && areMirror(r1->right,r2->left));
}
bool isSymmetric(Node* root) {
    if (root == NULL) return true;
    return areMirror(root->left, root->right);
}
```
<br><br><br>
<h1>Invert Binary Tree</h1>
Given the root of a binary tree, invert the tree, and return its root.<br>
i.e. find the mirror for the given tree<br><br>

```cpp
Node* invertTree(Node* root) {
    if (root == NULL) return NULL;
    Node* temp = root->left;
    root->left = invertTree(root->right);
    root->right = invertTree(temp);
    return root;
}
```
<br><br><br><br><br><br><br><br><br><br><br>
<br><br><div align="center">16</div>
<h1>Check if Binary Tree is Isomorphic</h1>
Two trees are called isomorphic if one can be obtained from another by a series of flips, i.e. by swapping left and right children of several nodes. Any number of nodes at any level can have their children swapped. <br><br>

```cpp
bool isIsomorphic(Node *root1, Node *root2)
{
    if (root1 == NULL && root2 == NULL) return true;
    if (root1 == NULL || root2 == NULL) return false;
    if (root1->data != root2->data) return false;
    bool withoutSwap = isIsomorphic(root1->left,root2->left) && isIsomorphic(root1->right,root2->right);
    bool withSwap = isIsomorphic(root1->left,root2->right) && isIsomorphic(root1->right,root2->left);
    return (withSwap || withoutSwap);
}
```

<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<br><br><div align="center">28</div>
<h1 id="constructstring">Construct Binary Tree from String with bracket representation</h1>
Construct a binary tree from a string consisting of parenthesis and single digit integers. The whole input represents a binary tree. It contains an integer followed by zero, one or two pairs of parenthesis. The integer represents the root’s value and a pair of parenthesis contains a child binary tree with the same structure. Always start to construct the left child node of the parent first if it exists.<br><br><br>
Click <a href="https://www.geeksforgeeks.org/construct-binary-tree-string-bracket-representation/">here</a> for more info<br><br><br><br><br>

```cpp
Node* treeFromString(string str)
{
	if (str.length() == 0) return NULL;
    stack<Node*> st;
    Node* root = newNode(str[0]-'0');
    st.push(root);
    int index = 1;
    
    while (index < str.length()) {
        if (str[index]=='(') {
            index++;
            Node* temp = newNode(str[index]-'0');
            Node* parent = st.top();
            if (parent->left) parent->right = temp;
            else parent->left = temp;
            st.push(temp);
        } else {
            st.pop();
        }
        index++;
    }
    
    return root;
}
```
<br><br><br><br><br><br><br><br><div align="center">29</div>
<h1 id="constructll">Convert Binary tree into Doubly Linked List</h1>
Given a Binary Tree (BT), convert it to a Doubly Linked List(DLL) In-Place. The left and right pointers in nodes are to be used as previous and next pointers respectively in converted DLL. The order of nodes in DLL must be same as Inorder of the given Binary Tree. The first node of Inorder traversal (leftmost node in BT) must be the head node of the DLL.<br><br><br><br>

```cpp
Node* last = NULL;
void dlr(Node* root) {
    if (root==NULL) return;
    dlr(root->left);
    root->left = last;
    if (last) last->right = root;
    last = root;
    dlr(root->right);
}

Node * bToDLL(Node *root)
{
    if (root==NULL) return NULL;
    Node* ans = NULL;
    dlr(root);
    while (root->left) root = root->left;
    return root;
}
```
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><div align="center">34</div>
<h1 style="font-size:30px;" id="bst">Binary Search Trees</h1>
Binary Search tree (BST), also called an ordered or sorted binary tree. <br><br>
Binary Search Tree is a node-based binary tree data structure which has the following properties:<br>
- Left subtree of a node contains only nodes with keys lesser than the node’s key.<br>
- Right subtree of a node contains only nodes with keys greater than the node’s key.<br>
- The left and right subtree each must also be a binary search tree.<br><br>

<div align="center" style="font-family:Finlandica;font-size:14px;"><b><i>
NodeValues(left subtree) <= CurrentNodeValue <= NodeValues(right subtree)
</i></b><br>
<img src="https://raw.githubusercontent.com/saivault/dsanotes/main/store/bst.png" height="200" weight="200">
</div><br><br>
The time complexity of operations on the binary search tree is directly proportional to the height of the tree. Binary search trees allow binary search for fast lookup, addition, and removal of data items. Since the nodes in a BST are laid out so that each comparison skips about half of the remaining tree, the lookup performance is proportional to that of binary logarithm.<br><br><br>
The complexity analysis of BST shows that <b>on average, the insert, delete and search takes O(log n)</b> for n nodes. In the worst case, they degrade to that of a singly linked list: O(n). To address the boundless increase of the tree height with arbitrary insertions and deletions, <b>self-balancing variants</b> of BSTs are introduced to bound the worst lookup complexity to that of the binary logarithm. AVL trees were the first self-balancing binary search trees. <br><br><br><br><br>
<b>Question: </b>Given a BST, find the nodes with the minium value and maximum value ?<br><br><br><br><br>
<div align="center">41</div>
<h2>SEARCH A NODE WITH THE GIVEN VALUE</h2>

```cpp
bool search(Node* root, int x) {
    if (root == NULL) return false;
    if (root->data < x) return search(root->right, x);
    if (root->data > x) return search(root->left, x);
    return true;
}
```
<br><br><br><br><h2>CHECK IF A BINARY TREE IS BST</h2>

```cpp
 bool isBstUtil(Node* root, int min, int max) {
    if (root == NULL) return true;
    if (root->data < min || root->data > max) return false;
    return isBstUtil(root->left, min, root->data-1) && 
        isBstUtil(root->right, root->data+1, max);
}

bool isBST(Node* root)  {
    return isBstUtil(root, INT_MIN, INT_MAX);
}
```
<br><br><br><br><h2>LOWEST COMMON ANCESTOR OF TWO NODES</h2>

```cpp
Node* LCA(Node *root, int n1, int n2)
{
   if (root==NULL) return NULL;
   if (root->data>n1 && root->data>n2) return LCA(root->left, n1, n2);
   if (root->data<n1 && root->data<n2) return LCA(root->right, n1, n2);
   return root;
}
```
<br><br><br><br><br><br><div align="center">42</div>
<h2>CONSTRUCT BST FROM PREORDER TRAVERSAL</h2><br><br>
Click <a href="https://leetcode.com/problems/construct-binary-search-tree-from-preorder-traversal/">here</a> for the problem link.<br><br>

```cpp
TreeNode* func(vector<int>& preorder, int low, int high) {
    if (low > high) return NULL;
    TreeNode* root = new TreeNode(preorder[low]);
    
    // index of the root element of right subtree
    int index=low+1;
    while (index<=high && preorder[index]<=preorder[low]) index++;
    
    root->left = func(preorder, low+1, index-1);
    root->right = func(preorder, index, high);
    return root;
}

TreeNode* bstFromPreorder(vector<int>& preorder) {
    return func(preorder, 0, preorder.size()-1);
}
```
Time complexity: O(n<sup>2</sup>)<br><br><br><br>Aliter,

```cpp
TreeNode* func(vector<int>& preorder, int &index, int max) {
    if (index==preorder.size() || preorder[index]>max) return NULL;
    TreeNode* root = new TreeNode(preorder[index]);
    index++;
    
    root->left = func(preorder, index, root->val - 1);
    root->right = func(preorder, index, max);
    return root;
}

TreeNode* bstFromPreorder(vector<int>& preorder) {
    int low = 0;
    return func(preorder, low, INT_MAX);
}
```
Time complexity: O(n)<br><br><br><br><br><br><div align="center">43</div>
Given a preorder or postorder traversal, we can construct a unique binary search tree in O(n) time from it. <br>
Given an inorder traveral, there will be many possible binary search trees. If you consider the middle element of the inorder array as root node every time, you are going to construct a balanced binary search tree.<br><br><br>
<h1>BST and inorder</h1>
One main property about a binary search tree is that its inorder is a sorted array.<br>
&nbsp;&nbsp;=> k<sup>th</sup> smallest element in bst = k<sup>th</sup> element in inorder (ldr) <br>
&nbsp;&nbsp;=> k<sup>th</sup> largest element in bst &nbsp;= k<sup>th</sup> element in reverse inorder (rdl) <br><br><br><br><h2>DELETE NODE IN A BST</h1><br>
Click <a href="https://leetcode.com/problems/delete-node-in-a-bst/">here</a> for the problem link.<br><br>

```cpp
Node* deleteNode(Node* root, int key) {
    if (root == NULL) return NULL;
    if (root->val < key) root->right = deleteNode(root->right, key);
    else if (root->val > key) root->left = deleteNode(root->left, key);
    else {
        Node* rchild = root->right;
        Node* lchild = root->left;
        delete root;
        if (lchild == NULL) return rchild;
        Node* temp = lchild;
        while (temp->right) temp = temp->right;
        temp->right = rchild;
        return lchild;
    }
    return root;
}
```
<br><br><br>
<h2>LARGEST BST IN A BINARY TREE</h2>
Click <a href="https://practice.geeksforgeeks.org/problems/largest-bst/1">here</a> for the problem link.<br>
<br><br><br><br><br><div align="center">44</div>

```cpp
vector<int> func(Node* root, int &ans) {
    vector<int> res;
    // res[0] stores the size of bst with current node as the bst
    // res[0] = -1 if current subtree is not a bst
    // res[1] will be the minimum value encountered in this subtree
    // res[2] will be the maximum value encountered in this subtree
    
    if (root==NULL) {
        res.push_back(0);
        return res;
    }
    
    vector<int> ltree = func(root->left, ans);
    vector<int> rtree = func(root->right, ans);
    
    // two conditions for current subtree to be a valid bst
    // maximum value obtained in left subtree should be less then root->data
    // minimum value obtained in right subtree should be greater then root->data
    
    if ((ltree[0]==-1) || (rtree[0]==-1) || (root->left && ltree[2]>=root->data) || (root->right && rtree[1]<=root->data)) {
        res.push_back(-1);
        return res;
    }
    
    int min = root->left ? ltree[1] : root->data;
    int max = root->right ? rtree[2] : root->data;
    int count = 1+ltree[0]+rtree[0];
    if (count > ans) ans = count;
    
    res.push_back(count);
    res.push_back(min);
    res.push_back(max);
    return res;
}
    
int largestBst(Node *root) {
	int ans = 0;
	func(root, ans);
	return ans;
}
```
