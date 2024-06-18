## Unconstrained Problems
考虑无约束问题：
$$\begin{array}{ll}\textrm{minimize}& f (\textbf{x}) \\ \textrm{subject to} & \textbf{x} \in \mathbb{R}^n\end{array}$$
则有如下的必要最优性条件：
![[Pasted image 20240515164648.png]]
第一个必要条件可直接由[[Global and Local Optimal Solution#First-Order Necessary Condition]]得出，因为所有方向均为可行方向
第二个必要条件则由[[Global and Local Optimal Solution#Second-Order Necessary Condition]]得出
## Sufficient Conditions
![[Pasted image 20240515164946.png]]
注意和上一个定理，必要条件是Hessian矩阵半正定[[Positive-definite Matrix#Positive Semi-definite Matrix]]，充分条件是Hessian矩阵正定[[Positive-definite Matrix#Positive-definite Matrix]]，因而可以推出strictly local minimizer。使用Talor展开可得出[[Taylor's Theorem]]
![[Pasted image 20240515165115.png]]
若 $f$ 是凸函数且连续可微，则条件简化，而且可以得到global minimizer
即global minimizer等价于梯度为 $0$
![[Pasted image 20240515165303.png]]
$\bar{x}$ 处的梯度为 $0$ ，且Hessian在 $\bar x$ 的一个邻域内保持半正定，则 $\bar x$ 为local minimizer
