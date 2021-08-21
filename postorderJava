// LC: https://leetcode.com/problems/binary-tree-postorder-traversal
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
    private void dfs(TreeNode node, List<Integer> postorder) {
        if(node == null) return; 
        
        dfs(node.left, postorder);
        dfs(node.right, postorder); 
        postorder.add(node.val); 
    }
    public List<Integer> postorderTraversal(TreeNode root) {
        List<Integer> postorder = new ArrayList<Integer>(); 
        dfs(root, postorder);
        return postorder; 
    }
}
