## LP Dual and Lagrangian Function
![[Pasted image 20240517143341.png]]
![[Pasted image 20240517143424.png]]
线性规划的Lagrangian对偶
## Lagrangian Duality
![[Pasted image 20240517143611.png]]
![[Pasted image 20240517143640.png]]
## Weak Duality Theorem
![[Pasted image 20240517144453.png]]
类似于LP对偶中的Weak Duality
由 $\theta(u,v)\leq f(x)-u^Tc(x)-v^Th(x)\leq f(x)$ 可得
![[Pasted image 20240517144556.png]]
## Duality Gap
![[Pasted image 20240517144705.png]]
即如果弱对偶定理中的不等式严格成立的话，则存在duality gap
## Strong Duality Theorem
![[Pasted image 20240517144728.png]]
当 $f$ 以及 $-c_i$ 均为凸函数，且满足Slater Constraint Qualification[[Kuhn-Tucker Condition for Inequality-Constrained Optimization#Slater CQ for (CP)]]，则duality gap不存在
若 $\inf$ 为有限的，则 $\sup$ 在 $\bar u\geq 0$ 取到；若 $\inf$ 在 $\bar u$ 处取到，则有 $\bar u^Tc(\bar x)=0$
![[Pasted image 20240517144919.png]]
## Wolfe Dual for Convex Program
![[Pasted image 20240517144938.png]]
在为凸规划且 $\chi=\mathbb{R}^n$ 的情况下 ，Lagrangian对偶可写成另一种更简单的形式
因为此时 $L(x,u)$ 为凸且 $x$ 可取任何值，则最优解等价于梯度为 $0$ 
## Saddlepoint Problems
![[Pasted image 20240517144958.png]]![[Pasted image 20240517145006.png]]
可用saddle point来求解IP [[Kuhn-Tucker Condition for Inequality-Constrained Optimization#Inequality-Constrained Problems]]，为global minimizer
![[Pasted image 20240618165050.png]]
## Remark
![[Pasted image 20240517145024.png]]
### Example: Nonexistence of a Saddlepoint
![[Pasted image 20240618165232.png]]
![[Pasted image 20240618165241.png]]
但是最优解不一定就是saddle point
![[Pasted image 20240517145036.png]]
对于凸问题，KKT点等价于saddle point
