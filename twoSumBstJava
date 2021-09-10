public class BSTIterator {
    private Stack<TreeNode> stack = new Stack<TreeNode>();
    boolean reverse = true; 
    
    public BSTIterator(TreeNode root, boolean isReverse) {
        reverse = isReverse; 
        pushAll(root);
    }

    /** @return whether we have a next smallest number */
    public boolean hasNext() {
        return !stack.isEmpty();
    }

    /** @return the next smallest number */
    public int next() {
        TreeNode tmpNode = stack.pop();
        if(reverse == false) pushAll(tmpNode.right);
        else pushAll(tmpNode.left); 
        return tmpNode.val;
    }
    
    private void pushAll(TreeNode node) {
        while(node != null) {
             stack.push(node);
             if(reverse == true) {
                 node = node.right; 
             } else {
                 node = node.left; 
             }
        }
    }
}
class Solution {
    public boolean findTarget(TreeNode root, int k) {
        if(root == null) return false; 
        BSTIterator l = new BSTIterator(root, false); 
        BSTIterator r = new BSTIterator(root, true); 
        
        int i = l.next(); 
        int j = r.next(); 
        while(i<j) {
            if(i + j == k) return true; 
            else if(i + j < k) i = l.next(); 
            else j = r.next(); 
        }
        return false; 
    }
}
