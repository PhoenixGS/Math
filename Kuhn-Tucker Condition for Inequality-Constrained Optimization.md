## Inequality-Constrained Problems
![[Pasted image 20240516121402.png]]
![[Pasted image 20240516121421.png]]
## The KKT Theorem
![[Pasted image 20240516121451.png]]
满足local minimizer以及LICQ，则满足KKT条件
LICQ: 需要满足取等限制对应的 $\nabla c_i(\bar{x})$ 之间线性无关
其中，对于所有限制，要求 $\bar{y}_i\geq 0$ ，对于那些不取等的限制， $\bar{y}_i=0$ 
## The KKT Conditions
![[Pasted image 20240516121620.png]]
满足KKT条件的 $\bar{x}$ 称为KKT stationary point，满足KKT条件的 $(\bar{x},\bar{y})$ 称为KKT pair
## The KKT Conditions is not Sufficient
![[Pasted image 20240516122046.png]]
KKT条件并不是充分的
## The need for a CQ
![[Pasted image 20240516122129.png]]
local minimizer + CQ -> KKT
## Fritz John’s Theorem
![[Pasted image 20240516123040.png]]
转化了一下形式，就可以不需要CQ条件了
### Remark
![[Pasted image 20240516123418.png]]
即线性无关时，有 $\bar{y}_0>0$ 
## First-Order Optimality Condition for (IP) is Not Enough!
## Optimization with Mixed Constraints
![[Pasted image 20240516123542.png]]
![[Pasted image 20240516123611.png]]
## The KKT Theorem for (P)
![[Pasted image 20240516123657.png]]
满足local minimizer，且满足：
对于不等式取等限制条件相应的 $\nabla c_i(\bar{x})$ 以及等号限制条件相应的 $\nabla h_i(\bar{x})$ 之间线性无关，则满足KKT条件，其中所有限制的 $\lambda_i\geq 0$ ，对于不取等条件的 $\lambda_i=0$ 
## Second-Order Conditions for (P)
![[Pasted image 20240516131312.png]]
二阶必要条件： $\nabla^2 L(\bar{x},\lambda,\mu)$ 在active限制的tangent subspace上半正定
![[Pasted image 20240516131335.png]]
二阶充分条件
## Convex Optimization
![[Pasted image 20240516131704.png]]
$f$ 和 $-c_i$ 都是可微凸函数
stationary point
![[Pasted image 20240516131726.png]]
在闭凸集 $\Omega$ 上，$x^*$ 是最优解（最小）当且仅当 $\nabla f(x^*)(x-x^*)\geq 0,\forall x\in \Omega$ 。这个结论比较直观。但是感觉在实际应用中用不了，因为 $x\in \Omega$ 很难直接描述。
![[Pasted image 20240516131751.png]]
若 $f$ 和 $-c_i$ 都是可微凸函数，则一阶KKT条件是全局最优的充分条件
若 $f$ 是可微凸函数，且原问题是线性约束，则一阶KKT条件是全局最优的充要条件
### The KKT Condition for (CP) is Enough!
### Remark
![[Pasted image 20240516131824.png]]
### Slater CQ for (CP)
![[Pasted image 20240516132010.png]]
![[Pasted image 20240516132019.png]]
## Exercises
![[Pasted image 20240517143153.png]]
![[Pasted image 20240517143208.png]]