class Solution {

    public boolean isValidBST(TreeNode root) {
        Stack<TreeNode> stack = new Stack<TreeNode>();
        TreeNode node = root;
        TreeNode prev = null; 
        while(true){
            if(node != null){
                stack.push(node);
                node = node.left;
            }
            else{
                if(stack.isEmpty()){
                    break;
                }
                node = stack.pop();
                // inorder.add(node.val);
                if(prev != null && node.val <= prev.val) return false; 
                prev = node; 
                node = node.right;
            }
        }
        return true; 
    }
}
