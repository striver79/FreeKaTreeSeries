class Solution {
    private:
    void dfs(TreeNode *node, vector<int> &postorder) {
        if(node == NULL) return; 
        
        dfs(node->left, postorder); 
        dfs(node->right, postorder); 
        postorder.push_back(node->val); 
    }
public:
    vector<int> postorderTraversal(TreeNode* root) {
        vector<int> postorder;
        dfs(root, postorder);
        return postorder; 
    }
};
