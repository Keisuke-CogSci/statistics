> [!NOTE]
> 各群が正規分布に従うとの仮定の上で、全群の分散が等しいかどうかの検定

群数を $k$、各群の不偏分散を $s_j^2$、各群の標本数を $n_j$ とする。

統計量 $\chi^2 = \dfrac{\left[\sum_{j = 1}^k (n_j - 1) \ln\left[\dfrac{\sum_{j = 1}^k (n_j - 1) s_j^2}{\sum_{j = 1}^k (n_j - 1)}\right] - \sum_{j = 1}^k (n_j - 1)\ln s_j^2\right]^2}{1 + \dfrac{1}{3(k - 1)} \left(\sum_{j = 1}^k \dfrac{1}{n_j - 1} - \dfrac{1}{\sum_{j = 1}^k (n_j - 1)} \right)}$ が、自由度$\color{crimson}{k-1}$の[[χ²分布]]に従うとして両側検定を行う。

