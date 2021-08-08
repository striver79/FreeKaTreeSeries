class Solution {
public:
    TreeNode* searchBST(TreeNode* root, int val) {
         while(root != NULL && root->val != val){
            root = val<root->val? root->left:root->right;
        }
        return root;
    }
};
