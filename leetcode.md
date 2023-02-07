
## 重建二叉树

* 输入某二叉树的前序遍历和中序遍历的结果，请构建该二叉树并返回其根节点。

* 假设输入的前序遍历和中序遍历的结果中都不含重复的数字。


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

## 树的子结构

* 输入两棵二叉树A和B，判断B是不是A的子结构。(约定空树不是任意一个树的子结构)

* B是A的子结构， 即 A中有出现和B相同的结构和节点值。


就像昨天说的，递归不彻底是不行的，今天又碰到了二叉树类问题，感觉解决的最好途径就是把递归吃透，其实也没有多么复杂，更像是打补丁，将各种条件堆砌在一起就能完成判断。

```js
var isSubStructure = function(A, B) {

if(!A||!B)return false  //base

return issame(A,B)||isSubStructure(A.left,B)||isSubStructure(A.right,B)

//判断是否在a中能完全找到
function issame(node1,node2){
if(node2==null)return true
return node1&&node2&&node1.val==node2.val&&issame(node1.left,node2.left)&&issame(node1.right,node2.right)       //条件判断
}
```
