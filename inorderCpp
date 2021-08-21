class Solution {
private:
    void dfs(TreeNode *node, vector<int> &inorder) {
        if(node == NULL) return; 
        
        dfs(node->left, inorder); 
        inorder.push_back(node->val); 
        dfs(node->right, inorder); 
    }
public:
    vector<int> inorderTraversal(TreeNode* root) {
        vector<int> inorder;
        dfs(root, inorder);
        return inorder; 
    }
};
