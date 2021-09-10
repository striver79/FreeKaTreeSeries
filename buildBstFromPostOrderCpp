Node* build(int post[], int& i, int bound) {
        if (i < 0 || post[i] < bound) return NULL;
        Node* root = new Node(post[i--]);
        root->right = build(post, i, root->data);
        root->left = build(post, i, bound);
        return root;
}
Node *constructTree (int post[], int size)
{
    int i = size - 1; 
    return build(post, i, INT_MIN); 
}
