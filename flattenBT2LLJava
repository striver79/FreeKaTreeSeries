// TC - O(N) 
// SC - O(N)
class Solution {
    TreeNode prev = null;
    public void flatten(TreeNode root) {
        if(root == null) return; 
        
        flatten(root.right); 
        flatten(root.left); 
        
        root.right = prev;
        root.left = null; 
        prev = root; 
    }
}

// TC - O(N) 
// SC - O(N) 
// Iterative 
class Solution {

    public void flatten(TreeNode root) {
        if(root == null) return; 
        
        Deque<TreeNode> st = new ArrayDeque<>(); 
        st.push(root); 
        while(!st.isEmpty()) {
            TreeNode cur = st.peek();
            st.pop();
            
            if(cur.right != null) {
                st.push(cur.right); 
            }
            if(cur.left != null) {
                st.push(cur.left); 
            }
            if(!st.isEmpty()) {
                cur.right = st.peek(); 
            }
            cur.left = null;
        }
        
    }
}

// TC - O(N) 
// SC - O(1) 
class Solution {
    public void flatten(TreeNode root) {
        TreeNode cur = root;
		while (cur != null)
		{
			if(cur.left != null)
			{
				TreeNode pre = cur.left;
				while(pre.right != null)
				{
					pre = pre.right;
				}
				pre.right = cur.right;
				cur.right = cur.left;
				cur.left = null;
			}
			cur = cur.right;
		}
    }
}
