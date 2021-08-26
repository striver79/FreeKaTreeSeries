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
    public int kthSmallest(TreeNode root, int k) {
        int cnt = 0; 
        int ans = -1; 
        TreeNode cur = root; 
        while(cur != null) {
            if(cur.left == null) {
                // inorder.add(cur.val); 
                cnt++; 
                if(cnt == k) ans = cur.val; 
                cur = cur.right; 
            }
            else {
                TreeNode prev = cur.left; 
                while(prev.right != null && prev.right != cur) {
                    prev = prev.right; 
                }
                
                if(prev.right == null) {
                    prev.right = cur;
                    cur = cur.left; 
                }
                else {
                    prev.right = null; 
                    // inorder.add(cur.val); 
                    cnt++; 
                    if(cnt == k) ans = cur.val; 
                    cur = cur.right; 
                }
            }
        }
        return ans; 
    }
}
