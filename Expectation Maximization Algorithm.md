![[Pasted image 20240601000917.png]]
![[Pasted image 20240601000926.png]]![[Pasted image 20240601000933.png]]
### Example
![[Pasted image 20240601000951.png]]![[Pasted image 20240601001002.png]]
## EM算法
![[Pasted image 20240601001129.png]]![[Pasted image 20240601001716.png]]
这部分可以参考《统计学习方法》
完全数据的对数似然函数 $\log P(Y,Z|\theta)$ 关于在给定观测数据 $Y$ 和当前参数 $\theta^{(i)}$ 下对未观测数据 $Z$ 的条件概率分布 $P(Z|Y,\theta^{(i)})$ 的期望称为 $Q$ 函数，即
$$Q(\theta,\theta^{(i)})=E_Z[\log P(Y,Z|\theta)|Y,\theta^{(i)}]$$
### 应用举例
- 投硬币问题
- 直线拟合(line fitting)
- 混合高斯模型 (Gaussian Mixture Models, GMM)