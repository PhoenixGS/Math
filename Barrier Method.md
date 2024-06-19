![[Pasted image 20240605140603.png]]
- Example
	![[Pasted image 20240605140731.png]]
![[Pasted image 20240605142805.png]]
尽管转化后的问题还是一个有约束问题，不过在计算过程中，可以不用考虑限制，因为算法会自动避免趋于边界
![[Pasted image 20240605142950.png]]
当 $\frac{B(x^k)}{c_k}$ 足够小时，停止
假定任意 $k$ ， $\min r(\textbf{x},c_k)$ 都有解
结合Barrier Methods和[[Penalty Method]]
- Example
	![[Pasted image 20240605143907.png]]
## Convergence of Barrier Method
![[Pasted image 20240605143958.png]]
与[[Penalty Method#Convergence of Penalty Method]] 方向不同
![[Pasted image 20240605144015.png]]
这个顺序也有些不同
![[Pasted image 20240605144131.png]]
但都收敛
