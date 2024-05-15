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