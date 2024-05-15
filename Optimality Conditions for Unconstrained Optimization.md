## Minimization of Convex Function
![[Pasted image 20240515161807.png]]
该定理较为trival
## Optimality Conditions in $\mathbb{R}$
![[Pasted image 20240515162107.png]]
即定义域为实数轴的特殊情况，使用导数可判断local minimizer
## Descent directions 下降方向
![[Pasted image 20240515162702.png]]
利用梯度
![[Pasted image 20240515162737.png]]梯度的反方向即为最速下降方向
![[Pasted image 20240515162844.png]]
## Feasible directions 可行方向
![[Pasted image 20240515162928.png]]
例子：
![[Pasted image 20240515163114.png]]
## First-Order Necessary Condition
![[Pasted image 20240515164122.png]]
即向任何方向都不能变得更小
## Second-Order Necessary Condition
![[Pasted image 20240515164257.png]]
## Unconstrained Problems
考虑无约束问题：
$$\begin{array}{ll}\textrm{minimize}& f (\textbf{x}) \\ \textrm{subject to} & \textbf{x} \in \mathbb{R}^n\end{array}$$
则有如下的必要最优性条件：
![[Pasted image 20240515164648.png]]
## Sufficient Conditions
![[Pasted image 20240515164946.png]]
注意和上一个定理，必要条件是Hessian矩阵半正定[[Positive-definite Matrix#Positive Semi-definite Matrix]]，充分条件是Hessian矩阵正定[[Positive-definite Matrix#Positive-definite Matrix]]，因而可以推出strictly local minimizer
![[Pasted image 20240515165115.png]]
若 $f$ 是凸函数，则条件简化
![[Pasted image 20240515165303.png]]
Hessian半正定，则为local minimizer[[Global and Local Optimal Solution#Global and Local Optimizers]]
