
> [!NOTE]
> 各群が正規分布に従わない場合に，全群の分散が等しいかどうかの検定

群の数を $k$，全データ数を $N$，$n_i$ を各群のデータ数，$Y_{ij}$ を $i$ 群の $j$ 番目の変数の値，$\bar{Y}_{i\cdot}$ を第 $i$ 群の平均値，$\tilde{Y}_{i\cdot}$ を第 $i$ 群の中央値とする。

さらに，$Z_{ij} = \left\{\begin{matrix}|Y_{ij} - \bar{Y}_{i\cdot}|\\|Y_{ij}-\tilde{Y}_{i\cdot}| & \end{matrix}\right.$*とし，$Z_{\cdot\cdot} = \dfrac{1}{N} \sum_{i=1}^{k} \sum_{j=1}^{n_i} Z_{ij}$*，$Z_{i\cdot} = \dfrac{1}{n_i} \sum_{j=1}^{n_i} Z_{ij}$とする。

統計量 $W = \dfrac{N-k}{k-1} \dfrac{\sum_{i=1}^k n_i (Z_{i\cdot}-Z_{\cdot\cdot})^2} {\sum_{i=1}^k \sum_{j=1}^{n_i} (Z_{ij}-Z_{i\cdot})^2}$ は自由度$\color{crimson}{(k-1, N-k)}$の [[F分布]]に従うので，両側検定を行う。

$Z_{ij}$ の定義に平均値ではなく中央値を用いる場合はBrown–Forsythe検定と呼ばれる。
