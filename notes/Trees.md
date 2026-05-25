# Trees — Comprehensive Notes

## Tree Traversals

### Inorder (Left → Root → Right)
```python
def inorder(node):
    if not node: return
    inorder(node.left)
    print(node.val)
    inorder(node.right)
```
- Result: Sorted order for BST

### Preorder (Root → Left → Right)
```python
def preorder(node):
    if not node: return
    print(node.val)
    preorder(node.left)
    preorder(node.right)
```
- Use: Building tree from traversal

### Postorder (Left → Right → Root)
```python
def postorder(node):
    if not node: return
    postorder(node.left)
    postorder(node.right)
    print(node.val)
```
- Use: Deleting tree, collecting leaf data

## Height vs Depth
- **Height**: Max distance to leaf
- **Depth**: Distance from root

## LCA (Lowest Common Ancestor)
```python
def lca(root, p, q):
    if not root or root == p or root == q: return root
    left = lca(root.left, p, q)
    right = lca(root.right, p, q)
    if left and right: return root
    return left if left else right
```

## BST Validation
- All left nodes < parent
- All right nodes > parent
- Both subtrees must be valid BSTs

## Last Updated: 2026-05-26
**Reviewed by**: Night Review Session
**Confidence Level**: 🟡 Medium (needs more practice)
