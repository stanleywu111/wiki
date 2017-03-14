## 随机过程
### Filtration
考虑定义在测度空间$\Omega$上的$\sigma$代数$F$，如果对于$s \leq t$，存在$F_s \subset F_t \subset F$，则$F_t$称为filtration
## 布朗运动
定义在概率空间$(\Omega, F,P)$上的过程$B(t)$是布朗运动如果该过程满足

* $B(t_0), B(t_1)-B(t_0),\cdots,B(t_n)-B(t_{n-1})$之间相互独立
* 对于$t>s\geq0$, $B(t)-B(s) \sim N(0,(t-s)I)$，即
    $$E[B(t_{i+1})-B(t_i)]=0$$
    $$Var[B(t_{i+1})-B(t_i)]=t_{i+1}-t_i$$
* $B(t)$是一个连续过程