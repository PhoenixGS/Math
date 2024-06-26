## Concepts
* 什么是机器学习？
	* 学习 = 在某种任务上基于经验不断改进
	* T (Task)  
	* P (Performance)  
	* E (Experience)
* 机器学习系统
	![[Pasted image 20240527170340.png]]
* 错误率与一致学习器
	![[Pasted image 20240527170657.png]]
* 偏差与方差
	![[Pasted image 20240529214042.png]]
## Algorithms 
* 有监督和无监督学习
	![[Pasted image 20240529214320.png]]
### 有监督学习
![[Pasted image 20240531115242.png]]
[[Linear Regression]]
[[Decision Tree]]
[[Bayesian Inference]]
[[K-Nearest Neighbor]]
[[Locally Weighted Regression]]
### 无监督学习
![[Pasted image 20240531115206.png]]
![[Pasted image 20240531115218.png]]
![[Pasted image 20240531115251.png]]
[[K-means Clustering]]
[[K-medoids Clustering]]
[[Clustering LARge Applications]]
[[Agglomerative Hierarchical Clustering]]
[[Divisive Hierarchical Clustering]]
### 半监督学习
![[Pasted image 20240531115308.png]]
### 集成学习
![[Pasted image 20240531201601.png]]
![[Pasted image 20240531201627.png]]![[Pasted image 20240531201647.png]]
#### 学习器
![[Pasted image 20240531201709.png]]
我们能否把弱学习器增强成一个强学习器?
#### 基本想法
![[Pasted image 20240531201749.png]]
#### 集成策略
![[Pasted image 20240531201804.png]]
#### 算法
[[Weighted Majority Algorithm]]
[[Bootstrap Aggregating]]
[[Boosting]]
[[Gradient Boosting Decision Tree]]
#### Bagging vs. Boosting
![[Pasted image 20240531232536.png]]![[Pasted image 20240531232554.png]]
#### 重新调权 vs. 重新采样
![[Pasted image 20240531232622.png]]
### 缺失数据的参数估计问题 Parameter estimation with missing data
[[Expectation Maximization Algorithm]]
### 序列学习方法 Sequential Models
[[Markov Model]]
[[Hidden Markov Model]]
### 深度学习与大语言模型
![[Pasted image 20240601154112.png]]
#### 神经网络序列模型 Neural Sequential Models
##### RNN
![[Pasted image 20240601160843.png]]
##### LSTM
![[Pasted image 20240601160927.png]]![[Pasted image 20240601160938.png]]
缺点: 参数太多，可能导致过拟合
## Experiments
[[Overfitting]]
[[Cross-validation]]
[[Bootstrap Aggregating#Bootstrap Sampling]]
![[Pasted image 20240601161623.png]]
## Theories
[[Hypothesis Evaluation]]
[[Probably Approximately Correct Learning]]
[[Sample Complexity]]
[[Sample Complexity#Vapnik-Chervonenkis Dimension]]



## 评价指标
### 回归任务
![[Pasted image 20240529223959.png]]
### 分类任务
![[Pasted image 20240529224028.png]]
![[Pasted image 20240529224036.png]]
[[Receiver Operating Characteristic]]
![[Pasted image 20240529224603.png]]

参考：张敏老师的课件


[[Support Vector Machine]]