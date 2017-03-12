# PDE方法求解动态规划问题
## 随机微分方程的强解性质
一个偏微分方程就是各阶偏导数满足的一个关系式，古典解就是函数本身的偏导数都存在并且满足那个关系式，
强解是函数的弱导数存在并且几乎处处满足那个关系式，用弱导数代替导数来验证那个关系式。  
对于随机微分方程：
$$dX_t=b(t,X_t)dt+\sigma(t,X_t)dW_t$$
其强解$X=(X^1,\cdots,X^n)$满足
$$\int^s_t|b(u,X_u)|du+\int^s_t|b(\sigma,X_u)|du < \infty$$
和
$$X_s = X_t + \int^s_tb(u,X_u)du+\int^s_tb(\sigma,X_u)du$$

## 动态规划原则（Dynamic Programming Principle）
有限区间：
$$
\begin{aligned}
 v(t,x)&= \sup_{\alpha \in A(t,x)} \sup_{\theta \in \tau_{t,T}}E[\int_t^\theta f(s,X_s^{t,x},\alpha_s)+v(\theta, X_\theta^{t,x})]\\ 
 &= \sup_{\alpha \in A(t,x)} \inf_{\theta \in \tau_{t,T}}E[\int_t^\theta f(s,X_s^{t,x},\alpha_s)+v(\theta, X_\theta^{t,x})]
\end{aligned}
$$
无限区间：
$$
\begin{aligned}
 v(x)&=\sup_{\alpha \in A(x)} \sup_{\theta \in \tau} E[\int_0 ^\theta e^{-\beta s}f(X_s^x,\alpha_s)ds+e^{-\beta \theta}v(X_\theta^x)] \\ 
 &= \sup_{\alpha \in A(x)} \inf_{\theta \in \tau} E[\int_0 ^\theta e^{-\beta s}f(X_s^x,\alpha_s)ds+e^{-\beta \theta}v(X_\theta^x)]
\end{aligned}
$$

## Hamilton-Jacobi-Bellman方程

## HJB方程粘性解
一个最优控制问题的值函数如果光滑，可以验证它是相应HJB方程的解。问题是一般只能得到值函数是连续的，所以后来发展了粘性解的概念。可以证明，在一定条件下，
值函数是HJB方程的唯一粘性解，这样就用一个PDE刻画了值函数。