We study algorithms that produce iterates according to well determined rules–Deterministic Algorithm rather than some random selection process–Randomized Algorithm.
## Classes of Problems
![[Pasted image 20240524000255.png]]
## Iterative methods: Finite vs Convergence
![[Pasted image 20240524000334.png]]
## Search directions
![[Pasted image 20240524000429.png]]
$p^k$ 选做是 $x^k$ 的一个函数，标量 $\alpha_k$ 使用line search rules确定
## The general idea
![[Pasted image 20240524000547.png]]
![[Pasted image 20240524000616.png]]
![[Pasted image 20240524000630.png]]
## Speed of convergence
### Q-convergence
![[Pasted image 20240524000711.png]]
### R-convergence
![[Pasted image 20240524000808.png]]
## Unconstrained minimization of smooth functions
![[Pasted image 20240524000935.png]]
直接寻找global minimizer太困难，将目标改为寻找local minimizer
![[Pasted image 20240524000956.png]]
## Descent method
![[Pasted image 20240524001039.png]]
## Accurate Line Search
$$\alpha_k=\arg\min_{\alpha\geq 0}\left\{f(x^k+\alpha p^k)\right\}$$
## Inaccurate Line Search
![[Pasted image 20240524001217.png]]
## Methods
[[Steepest Descent Method]]
[[Newton Method]]
[[The Barzilai-Borwein Method]]
[[Conjugate Direction Method]]
[[Quasi-Newton Method]]
