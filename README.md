## 10.21 day1 不知道还来不来得及开始
  非科班转码没有我想的那么简单。走了不少弯路，我决定今天重新开始。时间也不多了，今年的就业形势也很不太乐观，定个小目标：春招能找到工作就算胜利。从头学起，八股和语言都不能落下，看看三个月后我能做到什么地步。
  
  今天先从数据结构、算法和计算机网络开始，今天看了一部分[计算机基础速成课](https://www.bilibili.com/video/BV1EW411u7)和之前的《js数据结构与算法》这本书有关算法的部分，力扣上的剑指offer也要继续刷。另外还找了算法第四版和图解tcp/ip、http的电子书，准备以后看。
另：稍微算了下时间，明天起计算机网络每天要看6节，leetcode要做两道题（起）。

今晚写了通过前序和中序遍历构造二叉树和一个很简单的fib数列。

+ 前序中序遍历构造二叉树和昨天写的中序后序相似，通过前序获取每次的根结点，再在中序中寻找位置分割出左右子树，用的是迭代的写法，感觉递归还是不太会用，前几天写递归总是想复杂了，与其跑不出来还不如用迭代写，反正现在的技术也漏洞百出，能跑就是好的。感觉还是数据结构没有学懂，不太会利用元素的特性解决问题，判断语句太多了。（学一阵再来写）
```
/**
 * Definition for a binary tree node.
 * function TreeNode(val) {
 *     this.val = val;
 *     this.left = this.right = null;
 * }
 */
/**
 * @param {number[]} preorder
 * @param {number[]} inorder
 * @return {TreeNode}
 */

var buildTree = function(preorder, inorder) {
if(!preorder.length)return null
let root =new TreeNode()
check(inorder,preorder,root)
return root

function check (inorder,preorder,node){
if(inorder.length==1){
node.val = inorder.shift()
return
}
let lefttree=inorder.splice(0,inorder.indexOf(preorder.shift()))
let righttree=preorder.splice(lefttree.length)
node.val = inorder.shift()
if(!preorder.length&&!inorder.length){
    node.left=node.right=null
}else if(!preorder.length&&inorder.length){
    node.left=null
    node.right=new TreeNode()
    check(inorder,righttree,node.right)
}else if(preorder.length&&!inorder.length){
    node.right=null
    node.left=new TreeNode()
    check(lefttree,preorder,node.left)
}else{
    node.left=new TreeNode()
    node.right=new TreeNode()
    check(lefttree,preorder,node.left)
    check(inorder,righttree,node.right)
    }
}
};
```

+ 斐波那契数列就很简单了，没什么可说的，ending.

## 10.22 day2
今天算是按计划进行的一天，总体来说没什么问题，时间安排上也来得及，就是不知道后期看到难的部分还能不能保持效率。
1. 计算机网络：今天主要是介绍整个网络的结构组成和信息交换方式（分组、报文、电路）
2. html:没看太多，基本都会
3. js:一些概念，js居然是DOM,BOM-api和ECMAscript组成的,还有简单数据类型的一部分
4. 算法：简单的排序算法，选择排序、插入排序和希尔排序（通过人为设置增量实现远距离交换，数组越大优势越大的插入排序）
5. 题
+ 剑指offer10-2 青蛙跳台阶问题  
 一个基于动态规划的思考题，本质就是斐波那契数列。算法还没有看到那部分，看了题解大概明白一些，可以通过列出前几项找规律。
+ 剑指offer11 旋转数组的最小数字  
 写了两个版本的，最初当作队列来做，用pop和unshift遍历，效率很低，后来用了简化版的插入排序，比较末尾和前一位值，还是遍历，但运行快了很多，因为减少了数组操作。
