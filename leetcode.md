
## 重建二叉树

输入某二叉树的前序遍历和中序遍历的结果，请构建该二叉树并返回其根节点。

假设输入的前序遍历和中序遍历的结果中都不含重复的数字。

之前写的时候自己封装了函数，调用了3个参数写递归，这次直接用它封装好的框架试试，递归不彻底就是彻底不递归。

而且这次没有操作字符串，一定程度上也节约了性能
```js
var buildTree = function(preorder, inorder) {
    if (!preorder.length) return null

    const tree = new TreeNode(preorder[0]) //创建树

    let inorderRootIndex = inorder.indexOf(tree.val)

    //递归构建左子树
    let preorderLeft = preorder.slice(1, inorderRootIndex + 1)  //前序左子树，之所以1开始时为了去掉已经访问过的根节点
    let inorderLeft = inorder.slice(0, inorderRootIndex)  //中序左子树
    tree.left = buildTree(preorderLeft, inorderLeft)

    //递归构建右子树
    let preorderRight = preorder.slice(inorderRootIndex + 1) //前序左子树
    let inorderRight = inorder.slice(inorderRootIndex + 1)  //中序左子树
    tree.right = buildTree(preorderRight, inorderRight)

    return tree
};
```
