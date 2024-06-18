## Optimization Problems
$$\begin{array}{ll}\textrm{minimize}& f (\textbf{x}) \\ \textrm{subject to} & \textbf{x} \in S\end{array}$$
a **feasible solution** of a given problem is a vector that satisfies the constraints of the problem
## Global and Local Optimizers
A global minimizer is a vector $\bar{\textbf{x}}$ such that
$$\bar{\textbf{x}}̄\in S\textrm{ and }f(\bar{\textbf{x}})\leq f(\bar{\textbf{x}}) \quad \forall \bar{\textbf{x}}\in S$$
**local minimizer**, that is, a vector $\bar{\textbf{x}}$ such that 
$$\bar{\textbf{x}}\in S\textrm{ and }f(\bar{\textbf{x}})\leq f(x) \quad \forall x\in S\cap N(\bar{\textbf{x}})$$
where $N(\bar{\textbf{x}})$ is a **neighbourhood** of $\bar{\textbf{x}}$. Typically, $N(\bar{\textbf{x}})$ is a ball centered at $\bar{\textbf{x}}$ having suitably small radius.
The value of the objective function $f$ at a global minimizer or a local minimizer is also of interest. The **global minimum value** or a **local minimum value**, according to whether $\bar{\textbf{x}}$ is a global minimizer or a local minimizer, respectively.
## Minimization of Convex Function
![[Pasted image 20240515161807.png]]
该定理较为trival。即定义在凸集上的凸函数，取到minimum的集合是凸集，且local minimum均为global minimum
## Optimality Conditions in $\mathbb{R}$
![[Pasted image 20240515162107.png]]
即定义域为实数轴的特殊情况，可使用导数以及二阶导来判断local minimizer
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
即向任何可行方向都不能变得更小
## Second-Order Necessary Condition
![[Pasted image 20240515164257.png]]
在[[#First-Order Necessary Condition]]的基础上，若 $\nabla f(x^*)^Td=0$ ，则还需满足 $d^TH(x^*)d\geq 0$ 。证明与上都直接使用Taylor展开[[Taylor's Theorem]]即可。注意以上均为必要条件