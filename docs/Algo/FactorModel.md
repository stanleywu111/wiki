# 风险因子和阿尔法因子
## 定义
阿尔法因子决定投资哪只股票，风险因子决定投资该股票的权重。
## 风险因子
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

### 风险因子协方差矩阵的估计

### 股票特质风险的估计

### 风险因子对收益的解释程度检验
Gregory Connor, “The Three Types of Factor Models: A Comparison
of Their Explanatory Power,” Financial Analysts Journal, May/June
1995.

> Barra因子构建过程
> * Data acquisition and cleaning
> * Descriptor selection and testing  
> To determine which descriptors partition risk in the most effective
> and effcient way, the descriptors are tested for statistical
> signifcance. Useful descriptors often signifcantly explain > cross-sectional
returns. Selected descriptors must have a sound theoretical justifcation for inclusion in the model. They must be useful in predicting risk and
based on timely, accurate, and available data. In other words, each
descriptor must add value to the model. If the testing process shows
that they do not add predictive power, they are rejected.
> * Descriptor standardization
> * Risk index formulation  
We regress asset returns against industries and descriptors, one
descriptor at a time, after the normalization step. Each descriptor is
tested for statistical signifcance. Based on the results of these calculations and tests, descriptors for the model are selected and assigned
to risk indices.
> * Industry allocation
> * Factor return estimation
> * Covariance matrix calculation: Exponential weighting and Market volatility: GARCH
> * Specific risk forecasting
> *Model updating



## 阿尔法因子
传统多因子模型多使用因子截面序列与截面超额收益率序列的向量相关系数 IC 来检验因子的有效程度，并通常认定该 IC 序列的绝对值均值大于某一阈值则将因子认定为阿尔法源。



## factor alignment

# 因子回测
因子回测的过程当中，虽然数据不是样本外的，但是选择的因子却是“样本外”的，因为测试的时候都是用表现好的因子去测试的。
## Hedge Portfolio

## Person信息系数
$$IR = IC * \sqrt{Breadth}$$

# 多因子模型
