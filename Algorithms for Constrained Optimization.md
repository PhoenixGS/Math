![[Pasted image 20240605105339.png]]
Penalty和Barrier方法是用无约束问题近似约束优化问题的方法。在Penalty方法中，近似是通过在目标函数中添加一个规定约束变化成本高的项来实现的；在Penalty方法中，近似是通过添加一个有利于可行域内部点而不是边界附近点的项来实现的。与这些方法相关的是一个参数 c，它决定了惩罚或障碍的严重程度，从而决定了无约束问题近似原始约束问题的程度。
![[Pasted image 20240618203928.png]]
第一个问题与无约束问题与约束问题的逼近程度有关。这对于检查参数 $c$ 增加到无穷大时，无约束问题的解是否收敛到约束问题的解至关重要。
另一个问题从实际角度来看最为重要，即当给定无约束问题的目标函数包含惩罚项或障碍项时，如何解决该问题。
[[Penalty Method]]
[[Barrier Method]]
[[Augment Lagrangian Method]]
[[The Alternating Direction Method with Multipliers]]
### Primal Methods
[[Feasible Direction Methods]]
[[Frank-Wolfe Method]]
[[Simplified Zoutendijk Method]]
[[Gradient Projection Method]]
[[Active Set Method]]
[[Sequential Quadratic Programming Method]]