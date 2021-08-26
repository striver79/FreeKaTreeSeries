class Solution {
public:
    bool isValidBST(TreeNode* root) {
        stack<TreeNode*> st; 
        TreeNode* node = root;
        TreeNode* prev = NULL; 
        while(true) {
            if(node != NULL) {
                st.push(node); 
                node = node->left; 
            }
            else {
    
                if(st.empty() == true) break; 
                node = st.top(); 
                st.pop(); 
                // inorder.push_back(node->val); 
                if(prev != NULL && node->val <= prev->val) return false; 
                prev = node; 
                node = node->right; 
            }  
        }
        return true;
    }
};
