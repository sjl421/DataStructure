<h3>二叉树</h3>
二叉树是<strong>每个节点最多有2个孩子节点的有序树</strong>。其中以节点的左孩子节点为根的子树叫左子树，以节点的右孩子节点为根的子树叫右子树。</br>
<hr></hr>
<h3>二叉树的性质</h3>
<li>在二叉树的第i层上最多有2<sup>i-1</sup>个节点（i &gt;= 0）</li>
<li>深度为k的二叉树最多有2<sup>k</sup>-1个节点</li>
<hr></hr>
<h3>满二叉树、完全二叉树</h3>
如果一棵二叉树的深度为k，并且该二叉树有2<sup>k</sup>-1个节点，则称该二叉树为<strong>满二叉树</strong>。
</br>
将二叉树的节点，从上到下，从左到右进行编号。如果某棵二叉树的节点的编号和与其深度相同的满二叉树的节点的编号一一对应，那么这棵树就是完全二叉树。
<hr></hr>
<h3>完全二叉树的性质</h3>
<ul>
	<li>一棵有n个节点的完全二叉树，其深度k为：</br>
2<sup>k-1</sup>-1 &lt; n &lt;= 2<sup>k</sup> - 1 &lt;=====&gt;</br>
2<sup>k-1</sup> &lt;= n &lt; 2<sup>k</sup> &lt;=====&gt;</br>
k-1 &lt;= log<sub>2</sub>n &lt; k &lt;=====&gt;</br>
k = 向下取整(log<sub>2</sub>n) + 1
	</li>
	<li>将一棵有n个节点的完全二叉树的所有节点从上倒下，从左到右编号，则对于编号为i（1&lt;=i&lt;=n）的节点而言：
		<ul>
			<li>当i=1时，该节点是根节点，没有双亲节点。否则双亲节点的编号是：向下取整(i/2)</li>
			<li>当2&times;i大于n的时候，该节点是叶子节点，没有左右孩子节点，否则该节点的左孩子节点的编号是2&times;i</li>
			<li>当2&times;i+1大于n的时候，该节点没有右孩子节点，否则该节点的右孩子节点是2&times;i+1</li>
		</ul>
	</li>
</ul>
<hr></hr>
<h3>二叉树的存储</h3>
<ul>
<li><strong>顺序存储</strong></br>
用一组地址连续的存储单元依次自上而下，自左至右地存储<em>完全二叉树</em>的节点，即<em>将完全二叉树上编号为i的节点存储到一维数组的索引为i-1的分量中</em>。</br>
二叉树的顺序存储只适用于完全二叉树。因为，在最坏的情况下，一棵深度为k，并且节点个数也为k的二叉树，需要2<sup>k</sup>-1个存储单元，会造成空间的浪费。
</li>
<li><strong>链式存储</strong></br>
在<strong>二叉链表</strong>中，每个节点包含一个数据域、一个左指针域和一个右指针域。</br>
在<strong>三叉链表</strong>中，除了数据域、左右指针域之外，还包含一个指向双亲节点的指针域。</br>
在<em>二叉链表</em>表示中，在一棵有n个节点的二叉树中，空指针域的个数是n+1。因为n个节点的二叉树共有2n个指针域，其中n个节点需要n-1个指针域指向它们（<strong>根节点不需要某个指针域指向它</strong>），所以空指针域的数量是2n-(n-1)=n+1。
</li>
</ul>
<hr></hr>
<h3>二叉树的遍历</h3>
遍历二叉树是指<strong>按照某条搜索路径访问二叉树的节点，使得每个节点都被访问一次，且仅被访问一次</strong>。</br>
<ul>
	<li><strong>先（根）序遍历</strong></br>
		<ul>
			<li>访问根节点</li>
			<li>先序遍历左子树</li>
			<li>先序遍历右子树</li>
		</ul>
	</li>
	<li><strong>中（根）序遍历</strong></br>
		<ul>
			<li>中序遍历左子树</li>
			<li>访问根节点</li>
			<li>中序遍历右子树</li>
		</ul>
	</li>
	<li><strong>后（根）序遍历</strong></br>
		<ul>
			<li>后序遍历左子树</li>
			<li>后序遍历右子树</li>
			<li>访问根节点</li>
		</ul>
	</li>
	<li><strong>广度优先遍历（Breadth first search）</strong></br>
	从上到下，从左到右按照层级进行遍历
	</li>
</ul>
