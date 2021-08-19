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
class Pair {
    TreeNode node; 
    int num; 
    Pair(TreeNode _node, int _num) {
        num = _num; 
        node = _node; 
    }
}
class Solution {

    public List<Integer> postorderTraversal(TreeNode root) {
        Stack<Pair> st = new Stack<Pair>(); 
        st.push(new Pair(root, 1)); 
        List<Integer> pre = new ArrayList<>();
        List<Integer> in = new ArrayList<>();
        List<Integer> post = new ArrayList<>();
        if(root == null) return post;

        while(!st.isEmpty()) {
            Pair it = st.pop(); 

            // this is part of pre
            // increment 1 to 2 
            // push the left side of the tree
            if(it.num == 1) {
                pre.add(it.node.val); 
                it.num++; 
                st.push(it); 
                
                if(it.node.left != null) {
                    st.push(new Pair(it.node.left, 1)); 
                }
            }

            // this is a part of in 
            // increment 2 to 3 
            // push right 
            else if(it.num == 2) {
                in.add(it.node.val); 
                it.num++; 
                st.push(it); 

                if(it.node.right != null) {
                    st.push(new Pair(it.node.right, 1)); 
                }
            }
            // don't push it back again 
            else {
                post.add(it.node.val); 
            }
        } 

        return post; 

    }
}














