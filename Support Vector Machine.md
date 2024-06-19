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
	则拉格朗日对偶问题为$$\begin{array}{ll}\max_\alpha \min_{w,b}& L(w,b,\alpha)\\s.t. &\alpha \geq 0\\& y_i\left(wx_i+b\right)\geq 1 ,\forall i\end{array}$$利用KKT条件，对 $w,b$ 偏导取 $0$ 并代入，得如下问题：$$\begin{array}{ll}\max _{\alpha} & -\frac{1}{2} \sum_{i=1}^{N} \sum_{j=1}^{N} \alpha_{i} \alpha_{j} y_{i} y_{j}\left(x_{i}\cdot x_{j}\right)+\sum_{i=1}^{N} \alpha_{i} \\ \text { s.t. } & \sum_{i=1}^{N} \alpha_{i} y_{i}=0 \\ & \alpha_{i} \geq 0,\forall i\end{array}$$等价于：$$\begin{array}{ll}\min _{\alpha} & \frac{1}{2} \sum_{i=1}^{N} \sum_{j=1}^{N} \alpha_{i} \alpha_{j} y_{i} y_{j}\left(x_{i}\cdot  x_{j}\right)-\sum_{i=1}^{N} \alpha_{i} \\ \text { s.t. } & \sum_{i=1}^{N} \alpha_{i} y_{i}=0 \\ & \alpha_{i} \geq 0, \forall i\end{array}$$得到最优解 $\alpha^*$ ，再代入原始对偶问题的KKT条件中，可得$$\begin{matrix}w^{*}=\sum_{i=1}^{N} \alpha_{i}^{*} y_{i} x_{i}\\ b^{*}=y_{j}-\sum_{i=1}^{N} \alpha_{i}^{*} y_{i}\left(x_{i}\cdot x_{j}\right)\end{matrix}$$其中 $\alpha_j>0$
	则分类超平面为 $w^*x+b^*=0$ ，分类决策函数为 $f(x)=sign(w^*x+b^*)$
## 线性支持向量机
某些点线性不可分，意味着这些点不满足函数间隔大于等于 $1$ 的条件。
为此引入松弛变量 $\xi_i$  ，使得:$$y_i(wx_i+b)\geq 1-\xi_i,i=1,\cdots,N,\xi_i\geq 0$$
要使 $\xi_i$ 尽可能小，优化目标增加惩罚项，变为$$\min_{w,b,\xi}(\frac{1}{2}\Vert w\Vert^2+C\sum_{i=1}^N\xi_i)$$称为软间隔最大化，其中 $C>0$ 为惩罚参数
则问题转化为：$$\begin{array}{ll}\min_{w,b,\xi}&\frac{1}{2}\Vert w\Vert^2+C\sum_{i=1}^N\xi_i\\s.t.&y_i(wx_i+b)\geq 1-\xi_i,\quad i=1,\cdots,N\\&\xi_i\geq 0,\quad i=1,\cdots,N\end{array}$$该问题的对偶可化为：$$\begin{array}{ll}\min _{\alpha} & \frac{1}{2} \sum_{i=1}^{N} \sum_{j=1}^{N} \alpha_{i} \alpha_{j} y_{i} y_{j}\left(x_{i}\cdot  x_{j}\right)-\sum_{i=1}^{N} \alpha_{i} \\ \text { s.t. } & \sum_{i=1}^{N} \alpha_{i} y_{i}=0 \\ & 0\leq \alpha_{i} \leq C, \forall i\end{array}$$得到最优解 $\alpha^*$ 后，可求得$$\begin{matrix}w^{*}=\sum_{i=1}^{N} \alpha_{i}^{*} y_{i} x_{i}\\ b^{*}=y_{j}-\sum_{i=1}^{N} \alpha_{i}^{*} y_{i}\left(x_{i}\cdot x_{j}\right)\end{matrix}$$其中 $\alpha_i^*>0$ 对应的样本称为支持向量。
- 若 $\alpha_i^*<C$ ，则 $\xi_i=0$ ， $x_i$ 在间隔边界上
- 若 $\alpha_i^*=C,0<\xi_i<1$ ，则分类正确， $x_i$ 在间隔边界与分离超平面之间 
- 若 $\alpha_i^*=C,\xi_i=1$ ，则 $x_i$ 在超平面上
- 若 $\alpha_i^*=C,\xi_i>1$ ，则 $x_i$ 位于误分一侧
![[Pasted image 20240619150802.png]]
![[Pasted image 20240619150826.png]]
## 非线性支持向量机
### Example:
![[Pasted image 20240619152452.png]]
![[Pasted image 20240619152506.png]]
![[Pasted image 20240619152517.png]]
![[Pasted image 20240619152528.png]]
![[Pasted image 20240619152603.png]]
### 核函数
设 $\mathcal{X}$ 是输入空间（欧氏空间 $\mathbb{R}^{n}$ 的子集或离散集合)，设 $\mathcal{H}$为特征空间，如果存在一个从 $\mathcal{X}$ 到 $\mathcal{H}$ 的映射
$$
\phi(x): \mathcal{X} \rightarrow \mathcal{H}
$$
使得对所有 $x, z \in \mathcal{X}$，函数 $K(x, z)$ 满足条件
$$
K(x, z)=\phi(x) \cdot \phi(z)
$$
（其中 $\cdot$ 表示内积）则称 $K(x, z)$ 为核函数, $\phi(x)$ 为映射函数
#### Example
![[Pasted image 20240619153007.png]]
将核函数应用于之前的优化对偶问题，则有：$$\begin{array}{ll}\min _{\alpha} & \frac{1}{2} \sum_{i=1}^{N} \sum_{j=1}^{N} \alpha_{i} \alpha_{j} y_{i} y_{j} K\left(x_{i}, x_{j}\right)-\sum_{i=1}^{N} \alpha_{i} \\ \text { s.t. } & \sum_{i=1}^{N} \alpha_{i} y_{i}=0 \\ & 0\leq \alpha_{i} \leq C, \forall i\end{array}$$求得最优解 $\alpha^*$ 后，选择某个 $0<\alpha_j^*<C$ 计算：$$\begin{matrix}w^{*}=\sum_{i=1}^{N} \alpha_{i}^{*} y_{i} \phi (x_{i})\\ b^{*}=y_{j}-\sum_{i=1}^{N} \alpha_{i}^{*} y_{i}K(x_{i}, x_{j})\end{matrix}$$决策函数为：$$f(x)=sign\left(w^*\cdot\phi(x)+b^{*}\right)=sign\left(\sum_{i=1}^{N_{1}} a_{i}^{*} y_{i} K\left(x_{i}, x\right)+b^{*}\right)$$
#### 常用的核函数
- 多项式核函数$$K(x,z)=(x\cdot z+1)^p$$
- 高斯核函数$$K(x,z)=\exp\left(-\frac{\Vert x-z\Vert^2}{2\sigma^2}\right)$$
- 不同 $\sigma$ 值下的分界面示意图
	- ![[Pasted image 20240619153849.png]]
	- ![[Pasted image 20240619153901.png]]
	- ![[Pasted image 20240619153926.png]]