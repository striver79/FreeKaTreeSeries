// LC: https://leetcode.com/problems/binary-tree-preorder-traversal
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    private void dfs(TreeNode node, List<Integer> preorder) {
        if(node == null) return; 
        
        preorder.add(node.val); 
        dfs(node.left, preorder);
        dfs(node.right, preorder); 
    }
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> preorder = new ArrayList<Integer>(); 
        dfs(root, preorder);
        return preorder; 
    }
}
