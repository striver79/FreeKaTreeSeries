#include<bits/stdc++.h> 

int findMaxDistance(map<BinaryTreeNode<int>*, BinaryTreeNode<int>*> &mpp, BinaryTreeNode<int>* target) {
    queue<BinaryTreeNode<int>*> q; 
    q.push(target); 
    map<BinaryTreeNode<int>*,int> vis; 
    vis[target] = 1;
    int maxi = 0; 
    while(!q.empty()) {
        int sz = q.size();
        int fl = 0; 
        for(int i = 0;i<sz;i++) {
            auto node = q.front();
            q.pop();
            if(node->left && !vis[node->left]) {
                fl = 1; 
                vis[node->left] = 1; 
                q.push(node->left); 
            }
            if(node->right && !vis[node->right]) {
                fl = 1; 
                vis[node->right] = 1; 
                q.push(node->right); 
            }
            
            if(mpp[node] && !vis[mpp[node]]) {
                fl = 1; 
                vis[mpp[node]] = 1; 
                q.push(mpp[node]); 
            } 
        }
        if(fl) maxi++; 
    }
    return maxi; 
}
BinaryTreeNode<int>* bfsToMapParents(BinaryTreeNode<int>* root, 
                                     map<BinaryTreeNode<int>*, BinaryTreeNode<int>*> &mpp, int start) {
    queue<BinaryTreeNode<int>*> q; 
    q.push(root); 
    BinaryTreeNode<int>* res; 
    while(!q.empty()) {
        BinaryTreeNode<int>* node = q.front(); 
        if(node->data == start) res = node; 
        q.pop(); 
        if(node->left) {
            mpp[node->left] = node; 
            q.push(node->left); 
        }
        if(node->right) {
            mpp[node->right] = node;
            q.push(node->right); 
        }
    }
    return res; 
}
int timeToBurnTree(BinaryTreeNode<int>* root, int start)
{
    map<BinaryTreeNode<int>*, BinaryTreeNode<int>*> mpp; 
    BinaryTreeNode<int>* target = bfsToMapParents(root, mpp, start); 
    int maxi = findMaxDistance(mpp, target); 
    return maxi; 
}
 
