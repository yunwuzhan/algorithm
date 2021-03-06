比较排序
======
>如果我们对输入的数据不做任何要求，我们所获得的唯一信息就是各个元素的具体的值，仅能通过比较来确定输入序列<a1,a2...an>的元素间次序。

#### 决策树模型 ####

		比较排序可以被抽象为一颗决策树。决策树是一颗完全二叉树，它可以表示在给定输入规模下，某一特定排序算法对所有元素的比较操作。 
		比如说有(a1,a2,a3)需要排序，如下图所示:
		
 ![](https://github.com/yunwuzhan/algorithm/blob/master/resources/decisiontree.gif?raw=true) 

#### 在最坏情况下，任一比较排序算法时间复杂度 ####

		决策树的每个叶节点对应一个n个元素的排列，其中可能有重复的；但是由于决策树表明了所有可能遇到的情况，因而n个元素的所有排列都在
		决策树中出现过。n个元素共有n!种排列，即决策树的叶节点数目至少为n!。又因为一棵高度为h的二叉树（指二叉树的最高树叶高度为h）
		的叶节点数目最多为2h个（这时正好是满二叉树，即每个非叶节点都有两个子节点），因此n!≤2h，得到h≥log(n!)，其中log以2为底。
		根据Stirling公式有n!>(n/e)n，于是h>nlogn-nloge，即h=Ω(nlogn)。

