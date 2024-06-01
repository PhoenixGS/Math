![[Pasted image 20240601121718.png]]![[Pasted image 20240601121731.png]]![[Pasted image 20240601121747.png]]![[Pasted image 20240601121757.png]]
## 隐马尔可夫模型的形式
![[Pasted image 20240601121825.png]]![[Pasted image 20240601121833.png]]
## 三个假设
![[Pasted image 20240601121935.png]]
## 与[[Markov Model]]的区别
![[Pasted image 20240601122001.png]]
## 三个基本问题
![[Pasted image 20240601122416.png]]
### 问题1 评估问题
![[Pasted image 20240601122457.png]]
#### 解答方法1
![[Pasted image 20240601150610.png]]![[Pasted image 20240601150650.png]]![[Pasted image 20240601150712.png]]
#### 解答方法2 前向算法
简单的动态规划
![[Pasted image 20240601150734.png]]
![[Pasted image 20240601151050.png]]![[Pasted image 20240601151151.png]]
#### 解答方法3 后向算法
![[Pasted image 20240601151407.png]]![[Pasted image 20240601151606.png]]![[Pasted image 20240601151614.png]]
### 问题2 解码问题
![[Pasted image 20240601151732.png]]
![[Pasted image 20240601152001.png]]
#### Viterbi Algorithm
![[Pasted image 20240601152028.png]]![[Pasted image 20240601153048.png]]![[Pasted image 20240601153115.png]]![[Pasted image 20240601153200.png]]
应该也只是简单的动态规划
### 问题3 学习问题
![[Pasted image 20240601153559.png]]
![[Pasted image 20240601153618.png]]![[Pasted image 20240601153706.png]]
前向-后向算法
![[Pasted image 20240601153712.png]]
![[Pasted image 20240601153720.png]]
EM
![[Pasted image 20240601153728.png]]
## 应用
- 病情转化
	![[Pasted image 20240601153910.png]]
- 词性标注
	![[Pasted image 20240601153935.png]]
## 总结
![[Pasted image 20240601154015.png]]
![[Pasted image 20240601154023.png]]