# CLARA
![[Pasted image 20240531180945.png]]
- 抽取一小部分进行[[K-medoids Clustering#Partitioning Around Medoids(PAM)]] 聚类
- 剩余的样本按照最小中心距离进行归类
- 多次重复抽样进行PAM聚类，选取误差最小的结果作为最终结果