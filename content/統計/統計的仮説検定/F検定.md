

> [!NOTE]
> 2群の分散が等しいかどうかの検定

> [!question] **問題例**
> ある試験に関して，A組のうち$n_A$人の平均点が$\bar x_A$，不偏分散が$s_A^2$，B組のうち$n_B$人の平均点が$\bar x_B$，不偏分散が$s_B^2$だった。A組とB組の点数の母分散$\sigma_A^2 ,\sigma_B^2$は等しいか？

$$
\textsf{帰無仮説}\,H_0: \sigma_A^2 = \sigma_B^2, \quad \textsf{対立仮説}\,H_1: \sigma_A^2 \neq \sigma_B^2
$$

$s_A^2 > s_B^2$とする。帰無仮説が正しいとき，統計量$F=\dfrac{s_A^2}{s_B^2}$は，自由度$\color{crimson}(n_A-1, n_B-1)$の$F$分布に従う。

**証明**

    

有意水準$\alpha$のとき，両側検定の棄却域は

$$
\left\{F_{(n_A-1, n_B-1)}\left(\dfrac{\alpha}{2}\right)> F \right\}
$$
となる。

なお，$s_A^2,s_B^2$のうち大きい方を$F$値の分子に持ってくることにより，$F$は常に$1$以上となるため，$\left\{F_{(n_A-1, n_B-1)}\left(1-\dfrac{\alpha}{2}\right) = \dfrac{1}{F_{(n_A-1, n_B-1)}(\alpha/2)} < F \right\}$は確かめなくて良い。