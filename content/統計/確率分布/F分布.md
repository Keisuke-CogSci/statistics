
# 定義

互いに独立な確率変数 $X_1, X_2$ が、それぞれ自由度 $\nu_1, \nu_2$ の [[χ²分布]]に従っているとする。

$$
X_1 \sim \chi^2(\nu_1), X_2 \sim \chi^2(\nu_2)
$$

このとき、次の統計量 $F$ は、自由度 $(\nu_1, \nu_2)$ の $F$分布に従う。
$$
F=\dfrac{X_1/\nu_1}{X_2/\nu_2} \sim F(\nu_1,\nu_2)
$$
# 導出

$X_1 \sim \chi^2(\nu_1), X_2 \sim \chi^2(\nu_2)$ が独立であるとき、同時分布 $f_{X_1, X_2}(x_1, x_2)$ は
$$
f_{X_1,X_2}(x_1,x_2) = \dfrac{1}{2^{\nu_1/2}\Gamma(\nu_1/2)}x_1^{\nu_1/2-1}e^{-x_1/2}\dfrac{1}{2^{\nu_2/2}\Gamma(\nu_2/2)}x_2^{\nu_2/2-1}e^{-x_2/2}
$$
となる。ここで、$z= \dfrac{x_1/\nu_1}{x_2/\nu_2}, w=x_2$ と[[変数変換の公式|変数変換]]すると、ヤコビアンは
$$
\begin{aligned} J\{(x_1, x_2)\rightarrow (z,w)\} &=\det \begin{bmatrix}\dfrac{\partial x_1}{\partial z} & \dfrac{\partial x_1}{\partial w} \\ \\ \dfrac{\partial x_2}{\partial z} & \dfrac{\partial x_2}{\partial w} \end{bmatrix} \\ &= \det \begin{bmatrix} \dfrac{\nu_1}{\nu_2}x_2 & 0 \\ \dfrac{\nu_2}{\nu_1}x_1 & 1\end{bmatrix} \\ &= \dfrac{\nu_1}{\nu_2}x_2.\end{aligned}
$$
ここから先の計算が大変に面倒.