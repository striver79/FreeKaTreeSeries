int floorInBST(TreeNode<int> * root, int key)
{
    int floor = -1; 
    while (root) {
 
        if (root->val == key) {
            floor = root->val;
            return floor;
        }
 
        if (key > root->val) {
            floor = root->val;
            root = root->right;
        }
        else {
            root = root->left;
        }
    }
    return floor;
}
