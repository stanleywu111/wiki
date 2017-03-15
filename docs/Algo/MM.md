# Dealing with the Inventory Risk
假设订单到达符合泊松点过程，bid和ask两边分别为$N_b$和$N_a$，
则做市商的的存货为
$$q_t = N_t^b - N_t^a $$
做市商报价为$S_t^b$和$S_t^a$，因为订单簿的到达过程和距离中间价的
距离有关，即$\delta_t^b = S_t - S_t^b$，$\delta_t^a = S_t^a - S_t$。
则点过程的参数$\lambda$为：
$$\lambda^b(\delta^b) = A e^{-k \delta^b}$$
$$\lambda^a(\delta^a) = A e^{-k \delta^a}$$
令做市商现金为$X$，则
$$dX_t = (S_t + \delta_t^a)dN_t^a - (S_t-\delta_t^b)dN_t^b$$
令做市商满足CARA效用函数，则做市商优化问题为：
$$\sup E[-\exp(-\gamma(X_T+q_TS_T))]$$