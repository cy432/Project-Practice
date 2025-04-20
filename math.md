## Least-Squares Estimation 公式推导

### 1. 线性模型
$$ y = X\beta + \epsilon $$
其中：
- $y \in \mathbb{R}^n$ 
- $X \in \mathbb{R}^{n \times p}$ 
- $\beta \in \mathbb{R}^p$ 
- $\epsilon \in \mathbb{R}^n$ 

### 2. 目标函数
$$ \min_{\beta} S(\beta) = \| y - X\beta \|_2^2 = (y-X\beta)^T(y-X\beta) $$

### 3. 正规方程
$$ \frac{\partial S}{\partial \beta} = -2X^T(y - X\beta) = 0 $$
$$ \Rightarrow X^TX\beta = X^Ty $$

### 4. 参数解
$$ \hat{\beta} = (X^TX)^{-1}X^Ty $$

### 5. 方差估计
$$ \hat{\sigma}^2 = \frac{1}{n-p} \sum_{i=1}^n (y_i - x_i^T\hat{\beta})^2 $$

### 6. 协方差矩阵
$$ \text{Cov}(\hat{\beta}) = \sigma^2(X^TX)^{-1} $$