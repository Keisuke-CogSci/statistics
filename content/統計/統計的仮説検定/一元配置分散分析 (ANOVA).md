
※ 執筆中

3群以上の各群の平均値のどれかに差があるかどうかを検定する手法

### 基本的な考え方

ANOVAでは、観測データが「全体の平均」「群ごとの効果」「誤差」で構成されると考える。つまり、$y_{ij}$を$i$番目の群に属する$j$番目の観測値、$\mu$を全体の平均(母平均)、$\alpha_i$を$i$番目の群の効果 (母平均からのズレ)、$\varepsilon_{ij}$を誤差したとき、次が成り立つとする:

$$
y_{ij} = \mu + \alpha_i+\varepsilon_{ij}
$$

ANOVAでは、$\alpha_i=0$であるかどうかを検定する。

そのために、データ全体のばらつきを「**群間のばらつき**」と「**群内のばらつき**」に分解する。ばらつきは、平均からの差を二乗して合計した**平方和**で表される。


**全体の平方和 (SST)** は次のように定義される:

$$
\text{SST}=\sum_{i=1}^{m}\sum_{j=1}^{n_i} (y_{ij}-\bar y)^2
$$
ただし、$m$は群の数、$n_i$は$i$番目の群のデータ数、$\bar y$は全データの平均を表す。

**群間の平方和 (SSA)** は次のように定義される:

$$
\text{SSA} = \sum_{i=1}^m n_i(\bar y_i - \bar y)^2
$$

ただし、$\bar y_i$は$i$番目の群の平均を表す。SSAは、各群の平均値が、全体の平均値からどれだけばらついているかを表している。

さらに、**群内の平方和 (SSE)** は次のように定義される:

$$
\text{SSE} = \sum_{i=1}^{m}\sum_{j=1}^{n_i} (y_{ij}-\bar y_i)^2
$$
SSEは、各群内のデータが、その群の平均からどれだけばらついているかを表す (誤差を反映している)。

このとき、以下が成り立つ:

$$
\text{SST} = \text{SSA} + \text{SSE}
$$

> [!note]- **証明**
>  $$
> \begin{aligned}\text{SST} &= \sum_{i=1}^{m}\sum_{j=1}^{n_i} (y_{ij}-\bar y)^2 \\ &= \sum_{i=1}^{m}\sum_{j=1}^{n_i} ((y_{ij}-\bar y_i)+(\bar y_i -\bar y))^2 \\ &= \sum_{i=1}^{m}\sum_{j=1}^{n_i} (y_{ij}-\bar y_i)^2 + \sum_{i=1}^{m}\sum_{j=1}^{n_i} (\bar y_i -\bar y)^2 + 2\sum_{i=1}^{m}\sum_{j=1}^{n_i}(y_{ij}-\bar y_i)(\bar y_i -\bar y) \\ &= \text{SSE} + \sum_{i=1}^{m} n_i(\bar y_i -\bar y)^2 +0\\ &= \text{SSA} + \text{SSE}\end{aligned}
> $$
> ただし、次が成り立つことを用いた:
> $$
> \sum_{j=1}^{n_i}(y_{ij}-\bar y_i) = \sum_{j=1}^{n_i} y_{ij} - \sum_{j=1}^{n_i} \bar y_i = \sum_{j=1}^{n_i} y_{ij} - n_i \bar y_i = \sum_{j=1}^{n_i} y_{ij} -n_i\dfrac{1}{n_i}\sum_{j=1}^{n_i} y_{ij} =0
> $$


このとき、次の統計量$F$を考える:

$$
F = \dfrac{\text{SSA}/df_A}{SSE/df_E}
$$
$\text{SSA}$は自由度$df_A$の[[χ²分布]]に，$\text{SSE}$は自由度$df_E$の[[χ²分布]]に，それぞれ独立に従っているため，この統計量$F$は[[F分布]]$F(df_A,df_E)$に従う。


> [!note]- **SSAとSSEが従う分布**
> 

