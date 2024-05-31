## 问题
- ![[Pasted image 20240531184704.png]]
- ![[Pasted image 20240531184713.png]]
- ![[Pasted image 20240531184752.png]]
## 理论基础
![[Pasted image 20240531184807.png]]
### 二项分布的应用场景
![[Pasted image 20240531184830.png]]
### 估计假设准确率 Q1.1
$error_\mathcal{D}=\textrm{Pr}_{x\in\mathcal{D}}[c(x)\neq h(x)]$ ，即 $h$ 会误分类一个以分布 $\mathcal{D}$ 采样的实例的概率
![[Pasted image 20240531185850.png]]
## 估计(estimator)的两个重要性质
![[Pasted image 20240531185915.png]]
由于 $h$ 是在训练集 $S$ 上训练的，因此 $error_S(h)$ 是有偏的
### 估计假设准确率 Q1.2
![[Pasted image 20240531191343.png]]
![[Pasted image 20240531191528.png]]
#### 正态分布的置信区间
![[Pasted image 20240531191558.png]]
对于足够大的样本集合，二项分布近似为正态分布
![[Pasted image 20240531191649.png]]
## 单边与双边置信区间
![[Pasted image 20240531191839.png]]![[Pasted image 20240531191917.png]]
## 问题1
![[Pasted image 20240531192445.png]]
## 推导置信区间的一般方法
![[Pasted image 20240531192512.png]]
### 中心极限定理
确定 $Y$ 的分布 $\mathcal{D}$ （包括均值&方差）
![[Pasted image 20240531192653.png]]
![[Pasted image 20240531192718.png]]
## 问题2
### 假设间的错误率差异
![[Pasted image 20240531192814.png]]![[Pasted image 20240531194425.png]]![[Pasted image 20240531194654.png]]
### 统计有效性检验($z$检验)举例
![[Pasted image 20240531194749.png]]![[Pasted image 20240531194818.png]]
## 问题3
### 学习算法的比较
![[Pasted image 20240531200404.png]]
#### $k$ 折交叉验证 [[Cross-validation]]
![[Pasted image 20240531200551.png]]
![[Pasted image 20240531200650.png]]
#### 随机重复实验的统计有效性检验($t$ 检验)
![[Pasted image 20240531200907.png]]
## 统计有效性检验(总结)
![[Pasted image 20240531201136.png]]
# 假设评估的三个问题
![[Pasted image 20240531201243.png]]