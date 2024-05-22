$$L(x)=\sum_{j=0}^k y_j \ell_j(x)$$
$$\ell_j(x) = \frac{(x-x_0)}{(x_j-x_0)} \cdots \frac{(x-x_{j-1})}{(x_j-x_{j - 1})} \frac{(x-x_{j+1})}{(x_j-x_{j+1})} \cdots \frac{(x-x_k)}{(x_j-x_k)}$$
![[Pasted image 20240523001727.png]]
* 优点：公式结构对称、便于记忆与编程, 便于分析
* 缺点：增加或减少一个插值节点时, 公式变化较大, 计算不方便