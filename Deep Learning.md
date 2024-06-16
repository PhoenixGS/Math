## 激活函数
- Identity$$f(x)=x$$
- sigmoid$$f(x)=\sigma(x)=\frac{1}{1+e^{-x}}$$
- tanh$$f(x)=\tanh(x)=\frac{e^x-e^{-x}}{e^x+e^{-x}}$$
- ReLU$$f(x)=\textrm{ReLU}(x)=\max(0,x)=\begin{cases}\begin{matrix}x & x\geq 0\\0&x<0\end{matrix}\end{cases}$$
- softmax$$o_k=\frac{e^{x_k}}{\sum_i e^{x_i}}$$
## 损失函数
- 误差平方和
	- 对样本 $d$ 的误差$$E_d(w)=\frac{1}{2}\sum_{k=1}^m(t_{kd}-o_{kd})^2$$
	- 对所有样本的误差$$E(w)=\sum_{d=1}^nE_d(w)=\frac{1}{2}\sum_{d=1}^n\sum_{k=1}^m (t_{kd}-o_{kd})^2$$
- 交叉熵$$H_d(w)=-\sum_{k=1}^Mt_{kd}\log(o_{kd})$$$$H(w)=\sum_{d=1}^NH_d(w)=-\sum_{d=1}^N\sum_{k=1}^Mt_{kd}\log(o_{kd})$$
- 以上 $t_{kd}$ 为希望输出值， $o_{kd}$ 为实际输出值
- 一般交叉熵损失函数用于分类问题，误差平方和损失函数用于输出具体数值的问题
## 梯度下降法
$$\Delta w=-\eta\nabla_wE(w)$$
- 批量梯度下降算法：每次处理全部样本$$E(w)=\frac{1}{2}\sum_{d=1}^n\sum_{k=1}^m (t_{kd}-o_{kd})^2$$
- 随机梯度下降算法：每次处理一个样本$$E_d(w)=\frac{1}{2}\sum_{k=1}^m(t_{kd}-o_{kd})^2$$
- 小批量梯度下降算法：每次处理小批量的样本$$E(w)=\frac{1}{2}\sum_{d=k}^{k+b}\sum_{k=1}^m (t_{kd}-o_{kd})^2$$
## 反向传播算法 BP
## 卷积神经网络 CNN
- 卷积核
	- 两层 $3\times 3$ 卷积等效一个 $5\times 5$ 的卷积
- 填充
- 步长
- 多卷积核
- 多通道输入
- 池化
	- 最大池化
- 神经网络举例
	- LeNet
	- VGG-16
## 梯度消失问题
- 解决思路
	- 使用ReLU激活函数
	- GoogLeNet
		- Inception模块
		- 使用三个输出共同计算loss
	- ResNet
		- 残差模块
## 过拟合问题
- 方法
	- 使用验证集
	- 正则化项法
		- 误差平方和损失函数$$E_d(w)=\sum_{k=1}^M(t_{kd}-o_{kd})^2+\Vert w\Vert_2^2$$
		- 降低模型复杂性![[Pasted image 20240616202953.png]]
	- 舍弃法 dropout
		随机地临时舍弃一些神经元
	- 数据增强法
		数据越多，过拟合的风险就越小
## 词向量
- 独热编码 one-hot
	稀疏向量
- 分布式表示
	稠密向量
- 词向量
	词嵌入 word embedding
	![[Pasted image 20240616203246.png]]
	![[Pasted image 20240616203302.png]]
	问题：
	![[Pasted image 20240616203434.png]]
- word2vec
	一种简化的神经网络语言模型
	两种实现方式
	- 连续词袋模型(CBOW)
		![[Pasted image 20240616210936.png]]
		使用霍夫曼树
		![[Pasted image 20240616211112.png]]
		![[Pasted image 20240616211853.png]]
		![[Pasted image 20240616211903.png]]![[Pasted image 20240616211942.png]]
		![[Pasted image 20240616212002.png]]![[Pasted image 20240616212010.png]]
	- 跳词模型(Skip-Gram Model)
		![[Pasted image 20240616211022.png]]
- 应用
	- TextCNN：情感分类
		![[Pasted image 20240616212055.png]]
## 循环神经网络 RNN
- RNN$$\boldsymbol{H}_t = \phi(\boldsymbol{X}_t \boldsymbol{W}_{xh} + \boldsymbol{H}_{t-1} \boldsymbol{W}_{hh}  + \boldsymbol{b}_h)$$$$\boldsymbol{O}_t = \boldsymbol{H}_t \boldsymbol{W}_{hq} + \boldsymbol{b}_q$$
- 双向RNN
- GRU$$\boldsymbol{R}_t = \sigma(\boldsymbol{X}_t \boldsymbol{W}_{xr} + \boldsymbol{H}_{t-1} \boldsymbol{W}_{hr} + \boldsymbol{b}_r)$$$$\boldsymbol{Z}_t = \sigma(\boldsymbol{X}_t \boldsymbol{W}_{xz} + \boldsymbol{H}_{t-1} \boldsymbol{W}_{hz} + \boldsymbol{b}_z)$$$$\tilde{\boldsymbol{H}}_t = \text{tanh}(\boldsymbol{X}_t \boldsymbol{W}_{xh} + \left(\boldsymbol{R}_t \odot \boldsymbol{H}_{t-1}\right) \boldsymbol{W}_{hh} + \boldsymbol{b}_h)$$$$\boldsymbol{H}_t = \boldsymbol{Z}_t \odot \boldsymbol{H}_{t-1}  + (1 - \boldsymbol{Z}_t) \odot \tilde{\boldsymbol{H}}_t$$
- LSTM$$\boldsymbol{I}_t = \sigma(\boldsymbol{X}_t \boldsymbol{W}_{xi} + \boldsymbol{H}_{t-1} \boldsymbol{W}_{hi} + \boldsymbol{b}_i)$$$$\boldsymbol{F}_t = \sigma(\boldsymbol{X}_t \boldsymbol{W}_{xf} + \boldsymbol{H}_{t-1} \boldsymbol{W}_{hf} + \boldsymbol{b}_f)$$$$\boldsymbol{O}_t = \sigma(\boldsymbol{X}_t \boldsymbol{W}_{xo} + \boldsymbol{H}_{t-1} \boldsymbol{W}_{ho} + \boldsymbol{b}_o)$$$$\tilde{\boldsymbol{C}}_t = \text{tanh}(\boldsymbol{X}_t \boldsymbol{W}_{xc} + \boldsymbol{H}_{t-1} \boldsymbol{W}_{hc} + \boldsymbol{b}_c)$$$$\boldsymbol{C}_t = \boldsymbol{F}_t \odot \boldsymbol{C}_{t-1} + \boldsymbol{I}_t \odot \tilde{\boldsymbol{C}}_t$$$$\boldsymbol{H}_t = \boldsymbol{O}_t \odot \text{tanh}(\boldsymbol{C}_t)$$