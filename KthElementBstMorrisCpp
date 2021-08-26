class Solution {
public:
    int kthSmallest(TreeNode* root, int k) {
        // nvector<int> inorder; 
        int cnt = 0; 
        int ans = -1; 
        TreeNode* cur = root; 
        while(cur != NULL) {
            if(cur->left == NULL) {
                // inorder.push_back(cur->val); 
                cnt++; 
                if(cnt == k) ans = cur->val;  
                cur = cur->right; 
            }
            else {
                TreeNode* prev = cur->left; 
                while(prev->right != NULL && prev->right != cur) {
                    prev = prev->right; 
                }
                
                if(prev->right == NULL) {
                    prev->right = cur;
                    cur = cur->left; 
                }
                else {
                    prev->right = NULL; 
                    // inorder.push_back(cur->val); 
                    cnt++; 
                    if(cnt == k) ans = cur->val;
                    cur = cur->right; 
                }
            }
        }
        return ans; 
    }
};
