## Problem
数据点 $(t_i,f_i),(i=1,\cdots,m)$ ，用含参数的函数 $S(t)$ 来拟合，要求 $\sum_{i=1}^m [S(t_i)-f_i]^2$ 最小
## Linear Least Squares
若 $S(t)\in \Phi, S(t)=\sum_{j=1}^nx_j\phi_j(t)$ ，求系数 $x_j$ ，则为线性最小二乘
### 法方程法
![[Pasted image 20240523000323.png]]
![[Pasted image 20240523000341.png]]
缺点：当 $n$ 较大时, 病态性 (类似于连续函数)。计算 $𝑨^T𝑨$ , 数值误差也较显著
### 正交变换法
![[Pasted image 20240523000532.png]]
![[Pasted image 20240523000555.png]]