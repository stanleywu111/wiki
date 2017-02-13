## 指数分布
$$f(x)=\lambda e^{-\lambda x}$$

$$
F(x)=P(X \leq x) = 1-e^{-\lambda x}
$$

$$
\bar{F}(x) = P(X \geq x) = e^{-\lambda x}
$$

![exp dist](../img/dis.PNG)


### 无记忆性1(Hazard Function)
$$
h(x)=\frac{f(x)}{\bar{F}(x)}=\lambda
$$
$h(x) \Delta x$表示在接下来$\Delta x$时间内对象消失的概率，所以$h(x)$表示对象
在接下来单位时间内消失的概率，由上式可知为常数$\lambda$

### 无记忆性2
$$
\begin{aligned}
P(X \geq x+y |X \geq y) &= \frac{P(X \geq x+y)}{P(X \geq y)}\\ 
 &=\frac{e^{-\lambda (x+y)}}{e^{-\lambda y}} \\ 
 &=e^{-\lambda x} \\ 
 &=P(X \geq x)
\end{aligned}
$$

### 无记忆性3？？
$$
\frac{f(x)}{\bar{F}(y)} = f(x-y)
$$

### 最小指数分布
假设$X$和$Y$是独立的指数分布，令$Z=\min\left \{ X,Y \right \}$，
且定义变量$I$，$I=0$如果$X \leq Y$，$I=1$如果$X > Y$，则

1. $f(z) =  (\lambda+\mu)e^{-(\lambda+\mu)z}$
2. $P(I=0)=\frac{\lambda }{\lambda +\mu}=1-P(I=1)$

## Erlang分布
$X_i$为独立指数分布，则$\sum_{i=1}^n X_i$称为Erlang分布：
$$
f_{\sum_{i=1}^n X_i}(x)=\frac{\lambda (\lambda x)^{n-1} e^{-\lambda x}}{(n-1)!}
$$

$$
\bar{F}_{\sum_{i=1}^n X_i}(x)=P(\sum_{i=1}^n X_i \geq x)=\sum_{k=0}^{n-1} e^{-\lambda x}\frac{(\lambda x)^k}{k!}
$$

## 超指数分布
如果对于一个随机变量$X$，服从参数为$\lambda_i$的指数分布的概率为$p_i$，则
称为超指数分布：
 $$
   f(x) = \sum_n p_n \lambda_n e^{-\lambda_n x}
 $$
## 泊松分布
假设有一堆对象符合指数分布，则在时间$[0,x]$内到达的对象个数为$N(x)$
$$
\begin{aligned}
P(N(x)=n) &= P(N(x) < n+1) - P(N(x) < n)\\ 
 &= P(\sum_{i=1}^{n+1} X_i >x) - P(\sum_{i=1}^{n} X_i >x)\\ 
 &= e^{-\lambda x} \frac{(\lambda x)^n}{n!}
\end{aligned}
$$
以上$N(x)$为泊松分布

令$X$以指定顺序$Y_1 \leq Y_2 \leq \cdots \leq Y_N$到达，则
$$
f_{Y_1,\cdots,Y_N|N(x)=n}(y_1,y_2,\cdots,y_n) = \frac{n!}{x^n}
$$
若不指定到达顺序，则
$$
f_{X_1,\cdots,X_N}(x_1,x_2,\cdots,x_n) = \frac{1}{x^n}
$$

泊松过程Thinning
$$
\lambda p
$$
泊松过程superpositioning
$$
\lambda + \mu
$$

