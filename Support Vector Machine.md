二类分类器
特征空间上的间隔最大化线性分类器
通过核技巧可实现非线性分类
根据模型的复杂程度可划分为:
- 线性可分支持向量机
- 线性支持向量机
- 非线性支持向量机
## 线性可分支持向量机
- 训练集$$T=\{(x_1,y_1),\cdots,(x_N,y_N)\},x_i\in X=\mathbb{R}^n,y_i\in Y=\{+1,-1\},i=1,\cdots,N$$
- 超平面$$\boldsymbol{w}^{\mathrm{T}} \boldsymbol{x}+b=0$$
- 决策函数（线性可分支持器）$$f(x)=sign(\boldsymbol{w}^{\mathrm{T}} \boldsymbol{x}+b)$$
- 函数间隔
	- 超平面关于样本点的函数间隔$$\gamma_i=y_i\left(\frac{w}{\Vert w\Vert_2}x_i+\frac{b}{\Vert w\Vert_2}\right)$$
	- 超平面关于 $T$ 的函数间隔$$\gamma=\min_i\gamma_i$$
- 最优化
	问题转变为以下最优化问题：$$\begin{array}{ll}\max_{w,b} &\gamma\\s.t.&y_i\left(\frac{w}{\Vert w\Vert}x_i+\frac{b}{\Vert w\Vert}\right)\geq \gamma ,\forall i\end{array}$$
	等价于$$\begin{array}{ll}\max_{w,b} &\frac{\hat\gamma}{\Vert w\Vert}\\s.t.&y_i\left(wx_i+b\right)\geq \hat\gamma ,\forall i\end{array}$$
	由于函数间隔可缩放，可直接取 $\hat\gamma=1$ 。同时最大化 $\frac{1}{\Vert w\Vert}$ 等价于最小化 $\frac{1}{2}\Vert w\Vert^2$ ，故问题转化为$$\begin{array}{ll}\min_{w,b} &\frac{1}{2}\Vert w\Vert^2 \\s.t.&y_i\left(wx_i+b\right)\geq 1 ,\forall i\end{array}$$
- 拉格朗日对偶[[Lagrange Duality Theory and Saddle-Point Theorem#Lagrangian Duality]]
	拉格朗日函数$$L(w,b,\alpha)=\frac{1}{2}\Vert w\Vert^2+\sum_i\alpha_i[1-y_i(wx_i+b)]$$其中 $\alpha_i\geq 0$ ， $\alpha=(\alpha_1,\cdots,\alpha_N)^T$ **为拉格朗日乘子向量**
	则拉格朗日对偶问题为$$\begin{array}{ll}\max_\alpha \min_{w,b}& L(w,b,\alpha)\\s.t. &\alpha \geq 0\\& y_i\left(wx_i+b\right)\geq 1 ,\forall i\end{array}$$利用KKT条件，对 $w,b$ 偏导取 $0$ 并代入，得如下问题：$$\begin{array}{ll}\max _{\alpha} & -\frac{1}{2} \sum_{i=1}^{N} \sum_{j=1}^{N} \alpha_{i} \alpha_{j} y_{i} y_{j}\left(x_{i}x_{j}\right)+\sum_{i=1}^{N} \alpha_{i} \\ \text { s.t. } & \sum_{i=1}^{N} \alpha_{i} y_{i}=0 \\ & \alpha_{i} \geq 0,\forall i\end{array}$$等价于：$$\begin{array}{ll}\min _{\alpha} & \frac{1}{2} \sum_{i=1}^{N} \sum_{j=1}^{N} \alpha_{i} \alpha_{j} y_{i} y_{j}\left(x_{i}x_{j}\right)-\sum_{i=1}^{N} \alpha_{i} \\ \text { s.t. } & \sum_{i=1}^{N} \alpha_{i} y_{i}=0 \\ & \alpha_{i} \geq 0, \forall i\end{array}$$得到最优解 $\alpha^*$ ，再代入原始对偶问题的KKT条件中，可得$$w^{*}=\sum_{i=1}^{N} \alpha_{i}^{*} y_{i} x_{i}\\b^{*}=y_{j}-\sum_{i=1}^{N} \alpha_{i}^{*} y_{i}\left(x_{i}x_{j}\right)$$