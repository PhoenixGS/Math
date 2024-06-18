![[Pasted image 20240618192009.png]]
无约束local minimizer，满足 $\nabla f=0$ 
对于单变量标量函数，即为 $f'(x)=0$ ，若 $f$ 满足二阶连续可微，则可用Newton Method来求解
## Newton method for solving the equation $g(x)=0$
![[Pasted image 20240525150920.png]]
![[Pasted image 20240525150931.png]]
![[Pasted image 20240618192357.png]]
![[Pasted image 20240525151017.png]]
不一定能够收敛![[Pasted image 20240618192508.png]]
## Locally Quadratic Convergence of Newton Method
![[Pasted image 20240525151222.png]]
收敛速度为Q-quadratic convergence[[Algorithms for Unconstrained Optimization#Q-convergence]]
## Remark
![[Pasted image 20240525151334.png]]
正二次型函数使用Newton法，则一步收敛
## Newton method for solving a system of equations $\textbf{g}(\textbf{x}) = 0$ 
![[Pasted image 20240525151609.png]]
## Some computational issues
![[Pasted image 20240525153848.png]]
Newton法需要计算一阶、二阶导，开销可能较大
在优化场景下 $\textbf{g}(\textbf{x})=\nabla f(\textbf{x}),\nabla\textbf{g}(\textbf{x})=\nabla^2 f(\textbf{x})$ 为Hessian矩阵，在minimizer处半正定
当Hessian矩阵非奇异时，Hessian矩阵正定，则可使用 $LDL^T$ 来计算方向 $\textbf{p}$ 
## Storage
![[Pasted image 20240525153940.png]]
[[Quasi-Newton Method]]
## Descent
![[Pasted image 20240525154302.png]]![[Pasted image 20240525154328.png]]
$\nabla^2 f(\bar x)$ 正定是能够保持下降的充分条件
## Modified Newton Algorithm with Line Search
给 $\nabla^2f$ 加上正定对角阵 $E$ 使其正定
![[Pasted image 20240525183613.png]]![[Pasted image 20240525183623.png]]