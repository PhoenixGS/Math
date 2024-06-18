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
即拉格朗日函数在local minimizer $\bar{x}$ 关于 $x$ 的梯度为 $0$
### Proof when Constraints are Linear
当 $\textbf{h}(\textbf{x})$ 为线性约束时是满足的
使用[[Linear Programming#Farkas' Lemma]]
![[Pasted image 20240515173054.png]]
### The Need for a Regularity Condition
当 $\textbf{h}(\textbf{x})$ 非线性时需要满足regularity condition，即 $\nabla h(\bar x)$ 满秩
![[Pasted image 20240515172939.png]]
### Proof when Constraints are Nonlinear
![[Pasted image 20240515173847.png]]
![[Pasted image 20240515173938.png]]
![[Pasted image 20240515173904.png]]
![[Pasted image 20240515174030.png]]
tangent plane定义为 $S$ 上所有穿过 $x^*$ 的可微曲线在 $x^*$ 处的导数集合
![[Pasted image 20240515174039.png]]
在限制 $S$ 为 $h(x)=0$ 时，tangent plane为 $H=\{d\in \mathbb{R}^n\vert \nabla h(x^*)d=0\}$ 
#### Remark
![[Pasted image 20240515174132.png]]是否regular与 $h$ 的定义有关而不是和 $S$ 的形状相关
![[Pasted image 20240618140836.png]]
## First-Order Optimality Condition for (EP) is Not Enough
![[Pasted image 20240618140951.png]]
## Second-Order Necessary Conditions
假定 $f,\textbf{h}\in \mathcal{C}^2$
![[Pasted image 20240515173646.png]]
在一阶条件上，还需满足 $\nabla_x^2L(\bar x,\bar y)$ 在tangent plane上半正定
## Second-Order Sufficient Conditions
![[Pasted image 20240515174330.png]]
必要条件是一阶条件加上 $\nabla_x^2 L(\bar x,\bar y)$ 在 $M$ 上正定，则为strict local minimum
## Sensitivity: The Meaning of the Lagrangian Multipliers
![[Pasted image 20240515180702.png]]![[Pasted image 20240515180714.png]]
即 $\bar{y}_i(\textbf{c})$ 是目标函数对边界限制值的影子价格