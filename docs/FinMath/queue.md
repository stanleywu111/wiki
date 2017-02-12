## Single Server Queue
令$\lambda$为客户平均到达速率，$W$为平均处理时间，$L$为系统中处理的客户平均数量，则
$L = \lambda W$

**Utilization Level**：令$\lambda$为客户平均到达速率，$\bar{x}$为每个客户服务
平均处理时间，则$\rho = \lambda \bar{x}$为utilization level。$\rho$
表示工作站繁忙的时间比例，$1-\rho$表示工作站空闲的时间比例。

**Residual Waiting Time**：表示当前工作站需要处理当前客户的平均时间
$$
(1-\rho)0+\rho \frac{\bar{x^2}}{2 \bar{x}} = \lambda \frac{\bar{x^2}}{2}
$$

**VIrtual Waiting Time**：表示等待队列处理完所有请求的时间，等于当前客户的
residual waiting time再加上处理剩余客户的时间，令$\bar{r}=\frac{\bar{x^2}}{2 \bar{x}}$
$$
\begin{aligned}
V_q &= L_q \bar{x} + \frac{\lambda \bar{x^2}}{2}\\ 
 &= \lambda W_q \bar{x}+\frac{\lambda \bar{x^2}}{2} \\ 
 &= \rho(W_q+\bar{r})
\end{aligned}
$$