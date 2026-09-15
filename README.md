# Binary Tree Inorder Traversal

> 🤖 **Automation Note:** This solution code was authored by **Unmesh**. The repository creation, AI explanation, and GitHub syncing were fully automated using LeetSync. For details on how this repository was generated, see [Automation.md](Automation.md).

**Difficulty:** Easy | **Tags:** Stack, Tree, Depth-First Search, Binary Tree  
**LeetCode Link:** https://leetcode.com/problems/binary-tree-inorder-traversal/

## Problem

Given the `root` of a binary tree, return *the inorder traversal of its nodes' values*.

 

**Example 1:**

**Input:** root = [1,null,2,3]

**Output:** [1,3,2]

**Explanation:**

**Example 2:**

**Input:** root = [1,2,3,4,5,null,8,null,null,6,7,9]

**Output:** [4,2,6,5,7,1,3,9,8]

**Explanation:**

**Example 3:**

**Input:** root = []

**Output:** []

**Example 4:**

**Input:** root = [1]

**Output:** [1]

 

**Constraints:**

	
- The number of nodes in the tree is in the range `[0, 100]`.
	
- `-100 <= Node.val <= 100`

 
**Follow up:** Recursive solution is trivial, could you do it iteratively?

## Solution

```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution:
    def inorderTraversal(self, root: TreeNode | None) -> list[int]:
        result=[]
        def IOT(node):
            if node is None:
                return
            IOT(node.left)
            result.append(node.val)
            IOT(node.right)

        IOT(root)
        return result
```

---
*Authored by **Unmesh** • Synced automatically by [LeetSync](https://github.com) on 2026-09-15.*
