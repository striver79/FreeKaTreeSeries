class Solution {

public:
    vector<int> inorderTraversal(TreeNode* root) {
        stack<TreeNode*> st; 
        TreeNode* node = root;
        vector<int> inorder; 
        while(true) {
            if(node != NULL) {
                st.push(node); 
                node = node->left; 
            }
            else {
    
                if(st.empty() == true) break; 
                node = st.top(); 
                st.pop(); 
                inorder.push_back(node->val); 
                node = node->right; 
            }  
        }
        return inorder; 
    }
};
