class Solution {
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> postorder = new ArrayList<Integer>(); 
        
        TreeNode cur = root; 
        while(cur != null) {
            if(cur.left == null) {
                postorder.add(cur.val); 
                cur = cur.right; 
            }
            else {
                TreeNode prev = cur.left; 
                while(prev.right != null && prev.right != cur) {
                    prev = prev.right; 
                }
                
                if(prev.right == null) {
                    prev.right = cur;
                    postorder.add(cur.val); 
                    cur = cur.left; 
                }
                else {
                    prev.right = null; 
                    cur = cur.right; 
                }
            }
        }
        return postorder; 
    }
}
