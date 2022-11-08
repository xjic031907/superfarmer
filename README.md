## 10.21 day1 不知道还来不来得及开始
  非科班转码没有我想的那么简单。走了不少弯路，我决定今天重新开始。时间也不多了，今年的就业形势也很不太乐观，定个小目标：春招能找到工作就算胜利。从头学起，八股和语言都不能落下，看看三个月后我能做到什么地步。
  
  今天先从数据结构、算法和计算机网络开始，今天看了一部分[计算机基础速成课](https://www.bilibili.com/video/BV1EW411u7)和之前的《js数据结构与算法》这本书有关算法的部分，力扣上的剑指offer也要继续刷。另外还找了算法第四版和图解tcp/ip、http的电子书，准备以后看。
另：稍微算了下时间，明天起计算机网络每天要看6节，leetcode要做两道题（起）。

今晚写了通过前序和中序遍历构造二叉树和一个很简单的fib数列。

+ 前序中序遍历构造二叉树和昨天写的中序后序相似，通过前序获取每次的根结点，再在中序中寻找位置分割出左右子树，用的是迭代的写法，感觉递归还是不太会用，前几天写递归总是想复杂了，与其跑不出来还不如用迭代写，反正现在的技术也漏洞百出，能跑就是好的。感觉还是数据结构没有学懂，不太会利用元素的特性解决问题，判断语句太多了。（学一阵再来写）
```javascript
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

2. html：没看太多，基本都会  

3. js：一些概念，js居然是DOM,BOM-api和ECMAscript组成的,还有简单数据类型的一部分  

4. 算法：简单的排序算法，选择排序、插入排序和希尔排序（通过人为设置增量实现远距离交换，数组越大优势越大的插入排序）  

5. 题  
+ 剑指offer10-2 青蛙跳台阶问题    
 一个基于动态规划的思考题，本质就是斐波那契数列。算法还没有看到那部分，看了题解大概明白一些，可以通过列出前几项找规律。  
 
+ 剑指offer11 旋转数组的最小数字    
 写了两个版本的，最初当作队列来做，用pop和unshift遍历，效率很低，后来用了简化版的插入排序，比较末尾和前一位值，还是遍历，但运行快了很多，因为减少了数组操作。  

## 10.23 day3
想了想，还是把vue也看一看，毕竟吃饭的东西，早点看也灵活些。  

1. 计算机网络：简单介绍了下osi七层结构的概念和用途  

2. html：网页元素的全局属性  <b>hidden属性可以不渲染元素，但css可见性更优先</b>  

3. js：还没看 一会直播看  

4. 算法：今天算是大洗牌了，重写了昨天的笔记，修正了学习方向。开了个新文档专门记录算法学习。今天学了归并排序和快速排序，目前心态良好。  

5. 题：直接写的两个算法，稍微改了改交了几题

6. vue：拦截、监听元素原理（大概）部分指令作用


## 10.24 day4
又封校了 sad 明天又要早起  

1. 计算机网络：今天讲了物理层的传输原理，包括从模拟信号转换为数字信号传输的过程。三种通信方式（单工通信，半双工通信，全双工通信）  

2. html：字符编码，包括主要的转义字符。  

3. js：函数作用域 闭包的概念、原理：父对象变量对子对象均可见  

4. 算法：继续学习排序算法，手写了堆排序和计数排序。  

5. 题：堆排序和计数排序。

6. vue：class和style在2和3中因为拦截方式不同导致的差异，vue3创建vue对象的标准写法。


## 10.25 day5
这两天来点轻松的部分

1. 计算机网络：物理层 码分多址(cdma)  

2. html：语义结构，没有实际意义，只是为了方便观看。  

3. js：数组，运算符  

4. 算法：今天看了简单的部分，贪心算法，写了一些题。  

5. 题：贪心算法的题目，比较简单。

6. vue：数组或对象修改后，vue修改虚拟dom从而重构页面的过程。在遍历时规定唯一key值可以提高运行性能。


## 10.26 day6
这两天来点轻松的部分#2

1. 计算机网络：物理层 ppp协议

2. html：文本标签

3. js：数据类型转换，错误对象：throw,try-catch 

4. 算法：继续贪心  

5. 题：贪心算法的题目，比较简单。

6. vue：evt对象，事件修饰符，按键修饰符 非常好用的语法糖


## 10.27 day7
这两天来点轻松的部分#3

1. 计算机网络：数据链路层 以太网 csma/cd协议

2. html：列表标签

3. js：object对象及其prototype方法

4. 算法：今天写了二分查找的题  

5. vue：表单修饰符


## 10.28 day8
今天没有烂！

1. 计算机网络：mac地址

2. html：图像标签

3. js：属性描述对象（6个元属性），array方法

4. 算法：今天写了二分查找的题X2  

5. vue：写了购物车组件，确实看起来很容易但老出一些小问题，watch监听和fetch


## 10.29 day9
没有烂，只是忘了写^_^

1. 计算机网络：网桥 交换机 VLAN

2. html：链接标签

3. js：包装对象，string对象

4. 算法：二分查找continue...

5. vue：摸了，axios


## 10.30 day10
感冒了没什么精神，明天加油

1. 计算机网络：数据链路层简介

2. html：多媒体标签

3. js：math对象，date对象

4. 算法：二分查找continue again

5. vue：摸了，组件 子传父，父传子

## 11.5 day16
前一阵被封控了，这几天里找到了新的讲八股的文章，明天搞。html读过一遍了，现在是css的时间，算法每天都在写，vue先缓一阵，我的建议是别急。

1. css：font border

2. js：dom

3. 算法：昨天数组，今天字符串

## 11.6 day17
看了网络基础，算法也刷起来

1. css：position

2. js：dom-nodelist htmlcollection

3. 算法：链表，做的很快，不知道是题简单还是水平上升了？

4. 网络：经典tcp/ip结构层划分

## 11.7 day18
网络东西很多啊，慢慢搞，树比原来写的快了不少

1. css：单位

2. js：document element

3. 算法：树！

4. 网络：网页请求全过程

## 11.8 day19
http开搞

1. css：无

2. js：attr

3. 算法：排序

4. 网络：http
