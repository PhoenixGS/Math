![[Pasted image 20240529234208.png]]
## ID3
![[Pasted image 20240529235935.png]]
## Impurity
节点混杂度
![[Pasted image 20240529234513.png]]
[[Entropy]]
![[Pasted image 20240529234610.png]]
## 属性选择
根据信息的增益来进行选择
![[Pasted image 20240529235712.png]]
## 何时返回
![[Pasted image 20240529235725.png]]
情形3并不好，可能未完全分裂
![[Pasted image 20240529235825.png]]
## ID3算法搜索的假设空间
![[Pasted image 20240530000007.png]]
## ID3中的归纳偏置
![[Pasted image 20240530000055.png]]
## 过拟合问题及剪枝
![[Pasted image 20240530000244.png]]
![[Pasted image 20240530000329.png]]
### 预剪枝: 何时停止分裂
- 基于样本数
	![[Pasted image 20240530000420.png]]
- 基于信息增益的阈值
	![[Pasted image 20240530000444.png]]
### 后剪枝
- 错误降低剪枝
	![[Pasted image 20240530000536.png]]
	在验证集上能提升则剪枝，提升泛化性
	- 剪枝后新的叶节点标签赋值策略
		![[Pasted image 20240530000643.png]]
- 规则后剪枝
	![[Pasted image 20240530000830.png]]![[Pasted image 20240530000913.png]]
## 其他决策树应用问题及处理方案
### 连续属性值
![[Pasted image 20240530001726.png]]
### 具有过多取值的属性
![[Pasted image 20240530001759.png]]
### 未知属性值
![[Pasted image 20240530001920.png]]
### 考虑属性的代价
![[Pasted image 20240530002004.png]]