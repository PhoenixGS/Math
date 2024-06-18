![[Pasted image 20240605111002.png]]
$P(x)$ 为惩罚函数，在全局非负，且当且仅当在可行域 $S$ 中取 $0$
- Example
	![[Pasted image 20240605111327.png]]
![[Pasted image 20240605134922.png]]
期望当 $c$ 趋于 $+\infty$ 时，最优解可以趋近原问题的最优解
当 $c_kP(x^k)$ 足够小时结束
假定对于任意的 $k$ ，penalty problem都有解
- Example
	![[Pasted image 20240605134940.png]]
## Convergence of Penalty Method
![[Pasted image 20240605135052.png]]
随着 $c_k$ 的增大，我们有：
- $q(x^k,c_k)$ 的最优值递增（trival）
- $P(x^k)$ 递减（因为惩罚系数变高了）
- $f(x^k)$ 递增（因为逐渐趋于可行域）
![[Pasted image 20240605135245.png]]
- Proof$$f(x^*)=f(x^*)+c_kP(x^*)\geq q(x^k,c_k)=f(x^k)+c_kP(x^k)\geq f(x^k)$$
The above two lemmas give global convergence of the penalty method.
![[Pasted image 20240605135347.png]]
Penalty法产生的点列为 $\{x^k\}$ ，则该点列的任何极限点均为原问题的最优解
### Remark
![[Pasted image 20240605135418.png]]
原问题有最优解，但penalty problem不一定有最优解
![[Pasted image 20240605135606.png]]