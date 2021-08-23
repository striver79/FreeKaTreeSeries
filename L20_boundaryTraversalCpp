class Solution {
    bool isLeaf(Node* root) {
        return !root->left && !root->right;
    }
    
    void addLeftBoundary(Node* root, vector<int> &res) {
        Node* cur = root->left;
        while (cur) {
            if (!isLeaf(cur)) res.push_back(cur->data);
            if (cur->left) cur = cur->left;
            else cur = cur->right;
        }
    }
    void addRightBoundary(Node* root, vector<int> &res) {
        Node* cur = root->right;
        vector<int> tmp;
        while (cur) {
            if (!isLeaf(cur)) tmp.push_back(cur->data);
            if (cur->right) cur = cur->right;
            else cur = cur->left;
        }
        for (int i = tmp.size()-1; i >= 0; --i) {
            res.push_back(tmp[i]);
        }
    }
    
    void addLeaves(Node* root, vector<int>& res) {
        if (isLeaf(root)) {
            res.push_back(root->data);
            return;
        }
        if (root->left) addLeaves(root->left, res);
        if (root->right) addLeaves(root->right, res);
    }
public:
    vector <int> printBoundary(Node *root)
    {
        vector<int> res;
        if (!root) return res;

        if (!isLeaf(root)) res.push_back(root->data);

        addLeftBoundary(root, res); 
        
        // add leaf nodes
        addLeaves(root, res);

        addRightBoundary(root, res); 
        return res;
    }
};
