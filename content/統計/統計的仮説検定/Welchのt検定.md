> [!NOTE]
> 2群が正規分布に従うとの仮定の上で、平均が等しいかどうかの検定

> [!question] **問題例**
> ある試験に関して、A組のうち$n_A$人の平均点が$\bar x_A$、不偏分散が$s_A^2$、B組のうち$n_B$人の平均点が$\bar x_B$、不偏分散が$s_B^2$だった。A組とB組の点数の母分散が等しいかどうかが分からないとき、A組とB組の点数の母平均$\mu_A, \mu_B$は等しいと言えるか？

統計量$t=\dfrac{\bar x_A-\bar x_B}{\sqrt{\dfrac{s_A^2}{n_A}+\dfrac{s_B^2}{n_B}}}$は、自由度 $\color{crimson}{\nu\approx \dfrac{\left(\dfrac{s_A^2}{n_A}+\dfrac{s_B^2}{n_B}\right)^2}{\dfrac{s_A^4}{n_A^2(n_A-1)}+\dfrac{s_B^4}{n_B^2(n_B-1)}}}$の[[t分布]]に従う。有意水準$\alpha$のとき、両側検定の棄却域は

$$ \left\{t\left(\dfrac{\alpha}{2};\nu\right) < |t| \right\} $$

となる。