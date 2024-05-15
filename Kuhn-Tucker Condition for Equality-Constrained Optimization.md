## Equality-Constrained Problems
考虑classical equality-constrained problem
![[Pasted image 20240515171026.png]]
其中 $\textbf{h}$ 为向量函数：
![[Pasted image 20240515171107.png]]
## Jacobian
定义[[Jacobian]]矩阵：
![[Pasted image 20240515171725.png]]
有如下性质：
![[Pasted image 20240515171743.png]]
假定 $m\leq n$ 避免over-constrained
![[Pasted image 20240515171815.png]]
## The Lagrange Theorem
![[Pasted image 20240515172134.png]]
### Proof when Constraints are Linear
当 $\textbf{h}(\textbf{x})$ 为线性时是满足的
使用[[Linear Programming#Farkas' Lemma]]
![[Pasted image 20240515173054.png]]
### The Need for a Regularity Condition
当 $\textbf{h}(\textbf{x})$ 非线性时需要满足regularity condition
![[Pasted image 20240515172939.png]]
### Proof when Constraints are Nonlinear
![[Pasted image 20240515173847.png]]
![[Pasted image 20240515173938.png]]
![[Pasted image 20240515173904.png]]
![[Pasted image 20240515174030.png]]
![[Pasted image 20240515174039.png]]
#### Remark
![[Pasted image 20240515174132.png]]
## First-Order Optimality Condition for (EP) is Not Enough
## Second-Order Necessary Conditions
假定 $f,\textbf{h}\in \mathcal{C}^2$
![[Pasted image 20240515173646.png]]
## Second-Order Sufficient Conditions
![[Pasted image 20240515174330.png]]
## Sensitivity: The Meaning of the Lagrangian Multipliers
