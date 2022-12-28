#include <stdio.h>
#include <stdlib.h>

typedef struct node {
    int value;
    struct node *left;
    struct node *right;
} Node;

typedef struct tree {
    Node *root;
} Tree;

Node *create_node(int value) {
    Node *node = malloc(sizeof(Node));
    node->value = value;
    node->left = NULL;
    node->right = NULL;
    return node;
}

void insert(Node **root, int value) {
    if (*root == NULL) {
        *root = create_node(value);
        return;
    }
    if (value < (*root)->value) {
        insert(&(*root)->left, value);
    } else {
        insert(&(*root)->right, value);
    }
}

void inorder(Node *root) {
    if (root == NULL) {
        return;
    }
    inorder(root->left);
    printf("%d ", root->value);
    inorder(root->right);
}

void preorder(Node *root) {
    if (root == NULL) {
        return;
    }
    printf("%d ", root->value);
    preorder(root->left);
    preorder(root->right);
}

void postorder(Node *root) {
    if (root == NULL) {
        return;
    }
    postorder(root->left);
    postorder(root->right);
    printf("%d ", root->value);
}

int main(void) {
    int new,n;
    Tree tree;
    tree.root = NULL;
    printf("Choose enter the number of values to be inseted : ");
    scanf("%d", &n);
    do{
        printf("\nEnter the value : ");
        scanf("%d", &new);
        insert(&tree.root,new);
        n--;
    }while(n!=0);
    printf("\ninorder : ");
    inorder(tree.root);
}
   
