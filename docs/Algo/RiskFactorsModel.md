在多因子模型中，股票$j$的收益可以被分解为：
$$\tilde{r}_j = \sum_{k=1}^K X_{jk} \tilde{f}_k + \tilde{u}_j$$

* $\tilde{r}_j$：股票$j$的超额收益
* $X_{jk}$：股票$j$对因子 $k$ 的暴露
* $\tilde{f}_k$：因子$k$的收益

假设一个投资组合$P$，组成该资产的股票的权重分别为 $h_{P1}, h_{P2},\cdots, h_{PN}$，则该投资组合$P$的收益可以分解为：
$$\tilde{r}_P = \sum_{k=1}^K X_{Pk} \tilde{f}_k + \sum_{j=1}^N h_{Pj} \tilde{u}_j$$
其中：
$$X_{Pk} = \sum_{j=1}^N h_{Pj} X_{jk}$$
将上述式子使用矩阵形式，我们可以得到：
$$\tilde{r}_i = X \tilde{f} + \tilde{u}$$
所以股票的方差可以表示为：
$$var(r)=B\sum B^T + \Delta^2$$

## 风险因子的协方差矩阵估计
### 普通最小二乘估计
$$f_{ols} = (B^TB)^{-1}B^Tr$$

### 加权最小二乘估计
$$f_{wls} = (B^TWB)^{-1}B^TWr$$

### 稳健回归估计

## 统计因子的协方差矩阵估计

### 为什么需要统计因子
Gregory Connor. The three types of factor models: A comparison of their explanatory power
统计因子和风险因子同时使用的作用

## 风险因子
### 行业因子

### 风格因子
