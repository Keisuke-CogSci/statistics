
# 定義

[[正規分布#標準正規分布|標準正規分布]]に従う確率変数 $Z \sim \mathcal{N}(0,1)$ と，自由度 $\nu$ の [[χ²分布]]に従う確率変数 $V \sim \chi^2(\nu)$ に対し，$Z, V$ が独立であれば，以下に定める統計量 $T$ は自由度 $\nu$ の $t$分布に従う。
$$
T=\dfrac{Z}{\sqrt{V/\nu}} \sim t(\nu)
$$
自由度 $\nu$ の $t$分布の確率密度関数 $f(x;\nu)$ は，
$$
f(x;\nu)=\dfrac{\Gamma\left(\frac{\nu+1}{2}\right)}{\Gamma\left(\frac{\nu}{2}\right)}\dfrac{1}{\sqrt{\pi\nu}}\left(\dfrac{1}{\frac{x^2}{\nu}+1}\right)^{(\nu+1)/2}
$$
と書ける。

# 導出

[[正規分布#標準正規分布|標準正規分布]]に従う確率変数 $Z \sim \mathcal{N}(0,1)$ と，自由度 $\nu$ の[[χ²分布]]に従う確率変数 $V \sim \chi^2(\nu)$ が独立のとき，同時確率密度関数 $f_{Z,V}(z,v)$ は，
$$
f_{Z,V}(z,v)=\dfrac{1}{\sqrt{2\pi}}\exp\left[-\dfrac{z^2}{2}\right]\dfrac{1}{\Gamma(\frac{\nu}{2})}\dfrac{1}{2^{\nu/2}}v^{\nu/2-1}\exp\left[-\dfrac{v}{2}\right]
$$
と書ける。ここで，$t=\dfrac{z}{\sqrt{v/\nu}}, w=v$ と変数変換する。このときの[[ヤコビアン]]は
$$
\begin{aligned}J\{(z,v)\rightarrow (t,w)\} &= \det \begin{bmatrix} \dfrac{\partial z}{\partial t}& \dfrac{\partial z}{\partial w}\\ \dfrac{\partial v}{\partial t} & \dfrac{\partial v}{\partial w} \\\end{bmatrix} \\ &=\det \begin{bmatrix}\sqrt{w/\nu} & \dfrac{t}{2\sqrt{\nu w}} \\0 & 1 \\\end{bmatrix} \\ &= \sqrt{w/\nu}\end{aligned}
$$
である。[[変数変換の公式]]を用いると，変換後の確率密度関数 $f_{T,W}(t,w)$ は，
$$
\begin{aligned}f_{T,W}(t,w) &= \dfrac{1}{\sqrt{2\pi}}\exp\left[-\dfrac{t^2w}{2\nu}\right]\dfrac{1}{\Gamma(\frac{\nu}{2})}\dfrac{1}{2^{\nu/2}}w^{\nu/2-1}\exp\left[-\dfrac{w}{2}\right]\sqrt{\dfrac{w}{\nu}} \\ &= \dfrac{1}{\sqrt{\pi \nu}}\dfrac{1}{\Gamma(\frac{\nu}{2})}\dfrac{1}{2^{(\nu+1)/2}}w^{(\nu+1)/2-1}\exp\left[-\dfrac{(\frac{t^2}{\nu}+1)w}{2}\right]\end{aligned}
$$
となる。$w$ に関して周辺化すると，$W=V\sim \chi^2(\nu)$ であるから，積分範囲は正の範囲であり，
$$
f_T(t) = \dfrac{1}{\sqrt{\pi \nu}}\dfrac{1}{\Gamma(\frac{\nu}{2})}\dfrac{1}{2^{(\nu+1)/2}}\int_0^\infty w^{(\nu+1)/2-1}\exp\left[-\dfrac{(\frac{t^2}{\nu}+1)w}{2}\right]dw
$$
となる。ここで，$s = \dfrac{(\frac{t^2}{\nu}+1)}{2}w$と置くと，後半の積分は
$$
\left(\dfrac{2}{\frac{t^2}{\nu}+1}\right)^{(\nu+1)/2-1}\left(\frac{\frac{t^2}{\nu}+1}{2}\right)\int_0^\infty s^{(\nu+1)/2-1}\exp\left[-s\right]ds
$$

となるが，この後半の積分は[[ガンマ関数]]の定義 $\Gamma(z)=\int_0^\infty t^{z-1}e^{-t}dt$ から，$\Gamma\left(\frac{\nu+1}{2}\right)$ と等しいことがわかる。以上から，
$$
\begin{aligned}f_T(t) &= \dfrac{1}{\sqrt{\pi \nu}}\dfrac{1}{\Gamma(\frac{\nu}{2})}\dfrac{1}{2^{(\nu+1)/2}}\left(\dfrac{2}{\frac{t^2}{\nu}+1}\right)^{(\nu+1)/2-1}\left(\frac{\frac{t^2}{\nu}+1}{2}\right)\Gamma\left(\frac{\nu+1}{2}\right) \\ &= \dfrac{\Gamma\left(\frac{\nu+1}{2}\right)}{\Gamma(\frac{\nu}{2})}\dfrac{1}{\sqrt{\pi \nu}}\left(\dfrac{1}{\frac{t^2}{\nu}+1}\right)^{(\nu+1)/2}\end{aligned}
$$
となり，$t$分布が導出できた。