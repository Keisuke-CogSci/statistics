
<aside> 💡

Wilcoxonの順位和検定 ($\neq$ Wilcoxonの符号順位検定) とも呼ぶ。

</aside>


> [!NOTE]
> 2つの独立した群のデータの**中央値**に統計的に有意な差があるかどうかを評価するために用いられるノンパラメトリック検定


Mann-WhitneyのU検定は、データの実際の値ではなく、その順位に基づいて比較を行う。具体的には、2群のデータ全体を統合し、小さい方から順に順位を割り当て、それぞれのグループの順位和を比較する。

$$
\textsf{帰無仮説}\,H_0: \tilde\mu_X = \tilde\mu_Y, \quad
\textsf{対立仮説}\,H_1: \tilde\mu_X \neq \tilde\mu_Y
$$

サンプルサイズがそれぞれ $n_X, n_Y$ である2群 $X, Y$ のデータを合わせて昇順に並べ、順位を振る。$X_i$ に振られた順位を $R_{X_i}$ とする。また、順位和を次のように定める:

$$
\left\{\begin{matrix} R_X= \sum_{i=1}^{n_X} R_{X_i}\\ R_Y= \sum_{i=1}^{n_Y} R_{Y_i}& \end{matrix}\right.
$$

このとき，統計量 $U_X, U_Y$ を次のように計算する。
$$
\left\{\begin{matrix} U_X= n_Xn_Y+\dfrac{n_X(n_X+1)}{2}-R_X\\ U_Y= n_Xn_Y+\dfrac{n_Y(n_Y+1)}{2}-R_Y & \end{matrix}\right.
$$

このとき、統計量 $U = \min ({U_X, U_Y})$ に対し、$n_X, n_Y > 20$ 程度であれば、$U$値が[[正規分布]]に近似できるとして、$Z$値を以下で定める。
$$
Z=\dfrac{U-\mathbb{E}[U]}{\sigma_U}
$$

ただし、$\mathbb{E}[U] = \dfrac{n_Xn_Y}{2}$, $\sigma_U^2 = \dfrac{n_Xn_Y(n_X+n_Y+1)}{12}$ である。

サンプル数が小さい場合には、サンプル数が小さい方の群を1、もう一方を2として、群1の各観察について、群2の中でそれよりも小さい値が得られた観察の度数を数える。これらの度数をすべて総和したものが$U$となる。U値の分布表を見て検定する。