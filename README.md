[toc]

# 第五章 定积分与反常积分

## （一）、定积分

### 一、定积分的概念

#### 1、定积分的定义

**定义** 设f(x)在[a,b]上有定义且有界，作下面4步：
$$
(1)分割:&在[a,b]中插入n-1个分点a=x_0\lt x_0\lt x_1\lt x_2\lt...\lt x_{n-1}\\&\lt x_n=b。将区间[a,b]分成n个小区间[x_{i-1},x_i],i=1,2,...,n记\Delta x_i=x_i-x_{i-1}表示第i个小区间的长度\\
(2)近似:&在每个小区间[x_{i-1},x_i]上任取一点\xi_i,作以f(\xi_i)为高,[x_{i-1},x_i]为底的小矩形\\
(3)求和:&S_n=\sum_{i=1}^{n}f(\xi_i)\Delta x_i\\
(4)取极限:&记\lambda=\max_{1\le i\le n}\{\Delta x_i\},\lim_{\lambda\to0}\sum_{i=1}^{n}f(\xi_i)\Delta x_i
$$
如果上述极限存在(与分法无关、与ξ~i~的取法无关)，则称f(x)在[a,b]上可积，并称上述极限为f(x)在[a,b]上的定积分，记为
$$
\int_{a}^{b}f(x)dx=\lim_{\lambda\to0}\sum_{i=1}^{n}f(\xi_i)\Delta x_i
$$
【1】:定积分是积分和的极限，它的值只与被积函数f(x)和积分区间[a,b]有关，而与积分变量所用的记号无关，即$\int_{a}^{b}f(x)dx = \int_{a}^{b}f(\theta)d\theta =\int_{a}^{b}f(t)dt $

【2】:如果积分$\int_0^1f(x)dx$存在，就可将[0,1]区间分为n等分，此时$\Delta x_i=\frac{1}{n}，取\xi_i=\frac{i}{n}，由定积分的定义得$
$$
\int _1^0f(x)dx=\lim_{\lambda\to0}\sum_{i=1}^nf(\xi_i)\Delta x_i=\lim_{n\to\infty}\frac{1}{n}\sum_{i=1}^nf(\frac{i}{n})
$$

【3】：λ→0与n→∞不等价



#### 2、定积分的充分条件

**定理（定积分存在定理）**

（1）设f(x)在[a,b]上连续，则$\int _a^bf(x)dx$存在

（2）设f(x)在[a,b]上有界，且只有有限个间断点，则$\int_a^bf(x)dx$必定存在

（3）设f(x)在[a,b]上只有有限个第一类间断点，则$\int_a^bf(x)dx$必定存在

#### 3、定积分的几何意义

定积分的几何意义，对于[a,b]上连续的函数f(x)，当f(x)≥0，x∈[a,b]，定积分的几何意义是由曲线y=f(x)与直线y=0，x=a，x=b所围成的曲边梯形的面积；当f(x)≤0，x∈[a,b]，定积分值是位于x轴下方的曲边梯形面积的相反数，一般非定号的f(x)而言，定积分值则是曲边梯形正、负面积的代数和

### 二、定积分的性质

**定理（定积分的性质）**以下除特别声明者外，均设f(x)与g(x)在所讨论的区间上可积，则
$$
\begin{aligned}
(1)&\int_a^bf(x)dx=-\int_b^af(x)dx\\
(2)&\int_a^bf(x)dx=0\\
(3)&\int_a^b[f(x)\pm g(x)]dx=\int_a^bf(x)dx\pm\int_a^bg(x)dx\\
(4)&\int_a^bkf(x)dx=k\int_a^bf(x)dx,k为常数\\
(5)&\int_a^bf(x)dx=\int_a^cf(x)dx+\int_c^bf(x)dx\\
\\(3)&若f(x)与g(x)的区间[a,b]上连续,则至少存在点x_1,a\le x_1\le b,\\&使f(x_1)\lt g(x_1),则\int_a^bf(x)dx\lt\int_a^bg(x)dx\\
\end{aligned}
$$

#### 1、不等式性质

$$
\begin{aligned}
(1)&若f(x)\le g(x),a\le b,则\int_a^bf(x)dx\le\int_a^bg(x)dx\\
(2)&若f(x)在[a,b]上连续，则m(b-a)\le\int_a^bf(x)dx\le M(b-a)\\
(3)&|\int ^b_af(x)dx|\le\int^b_a|f(x)|dx\\
\end{aligned}
$$

#### 2、中值定理

$$
\begin{aligned}
(1)&加强的积分中值定理:设f(x)在[a,b]上连续,则至少存在一点\xi\in(a,b)\\
&使\int_a^bf(x)dx=f(\xi)(b-a)\\
(2)&若f(x),g(x)在[a,b]上连续，g(x)不变号，则\\
&\int_a^bf(x)g(x)dx = f(\xi)\int_a^bg(x)dx,a\le \xi \le b
\end{aligned}
$$

### 三、积分上限函数

**定理（变限积分）**

设f(x)在[a,b]上可积，对x∈[a,b]，f(x)在[a,x]上可积，于是
$$
\Phi(x)=\int_a^xf(t)dt,x\in[a,b]
$$
定义了一个以x为自变量的函数，称为变上限的定积分

类似，变下限的定积分$\Phi(x)=\int_b^xf(t)dt,x\in[a,b]$

变上限的定积分和变下限的定积分统称为变限积分

**定理（变上限函数对上限变量求导，或称不定积分与定积分的关系）**

设f(x)在[a,b]上连续，则$(\int_a^xf(t)dt)'_x=f(x),x\in[a,b]$

由此可知，$\int_a^xf(t)dt$是f(x)的一个原函数，从而$\int f(x)dx=\int_a^xf(t)dt+C$
$$
(\int_{\varphi(x)}^{\psi(x)}f(t)dt)'=f(\psi(x))\psi'(x)-f(\varphi(x))\varphi'(x)
$$
若f(x)是奇函数，则$\int_0^x f(t)dt$是偶函数

若f(x)是偶函数，则$\int_0^x f(t)dt$是奇函数

【注】：如果f(x)在[a,b]上除点x=x~0~∈(a,b)外均连续，而在x=x~0~处f(x)有跳跃间断点：
$$
&\lim_{x\to x_0^-}f(x)=f(x_0^-),\lim_{x\to x_0^+}f(x)=f(x_0^+),f(x_0^-)\ne f(x_0^+)\\
记&F(x)=\int_c^xf(t)dt\\
&不论c是否等于x_0,均有结论:\\
①&F(x)在[a,b]上连续\\
②&F'(x)=f(x),当x\in[a,b],但x\ne x_0\\
③&F'_-({x_0})=f(x_0^-),F'_+(x_0)=f(x_0^+)
$$
### 四、定积分的计算

#### 1、牛顿—莱布尼兹公式

**定理（牛顿-莱布尼兹定理）**设f(x)在[a,b]上连续，F(x)是f(x)的一个原函数，则
$$
\int_a^bf(x)dx=F(x)\vert_a^b=F(b)-F(a)
$$

#### 2、换元积分法

设f(x)在区间I上连续，函数x=φ(t)满足以下条件：

1. φ(α)=a，φ(β)=b
2. φ(t)在[α,β]上有连续导数，且R~φ~$\subseteq$I，则

$$
\int_a^bf(x)dx = \int_{\alpha}^{\beta}f[\varphi(t)]\varphi'(t) dt
$$

#### 3、分部积分法

$$
\int_a^budv= uv\vert_a^b-\int_a^bvdu
$$

#### 4、利用奇偶性和周期性

1. 设f(x)为[-a,a]上的连续函数(a>0)，则
   $$
   \int _{-a}^af(x)dx = \begin{cases}0, &f(x)为奇函数时\\2,&f(x)为偶函数时 \end{cases}
   $$

2. 设f(x)是以T为周期的连续函数，则对任给数a，总有
   $$
   \int _a^{a+T}f(x)dx = \int_0^Tf(x)dx
   $$

#### 5、利用已有公式

$$
\begin{aligned}
(1)&\int _{0}^{\frac{\pi}{2}}\sin^nxdx = \int_0^{\frac{\pi}{2}}\cos^n xdx = \begin{cases}\frac{n-1}{n}·\frac{n-3}{n-2}·…·\frac12·\frac{\pi}{2},&n为正偶数 \\ \frac{n-1}{n}·\frac{n-3}{n-2}·…·\frac23,&n
为大于1的奇数\end{cases}\\
(2)&\int_0^\pi xf(\sin x)dx=\frac\pi2\int_0^\pi f(\sin x)dx(其中f(x)连续)
\end{aligned}
$$

## （二）、反常积分

### 一、无穷区间上的反常积分

**定义**
$$
\begin{aligned}
\\(1)&设f(x)为[a,+\infty)上的连续函数，如果极限\lim_{t\to+\infty}f(x)dx存在，则称此极限
\\&为函数f(x)在无穷区间[a,+\infty)上的反常积分，记\int_a^{+\infty}f(x)dx，即
\\&\int_0^{+\infty}f(x)dx=\lim_{t\to+\infty}\int_a^tf(x)dx
\\&这时也称反常积分\int_a^{+\infty}f(x)dx收敛，
\\&如果上述极限不存在，则称反常积分\int_a^{+\infty}f(x)dx发散\\
(2)&设f(x)为(-\infty,a]上的连续函数，则可类似的定义函数f(x)在无穷区间(-\infty,b]
\\&上的反常积分
\\&\int^b_{-\infty}f(x)dx=\lim_{t\to-\infty}\int_t^bf(x)dx
\\(3)&设f(x)为上的连续函数，如果反常积分\int_{-\infty}^0f(x)dx和\int_0^{+\infty}f(x)dx
\\&都收敛，则称反常积分\int_{-\infty}^{+\infty}f(x)dx收敛，且
\\&\int_{-\infty}^{+\infty}f(x)dx=\int_{-\infty}^0f(x)dx+\int_0^{+\infty}f(x)dx
\\&如果\int_{-\infty}^0f(x)dx与\int_0^{+\infty}f(x)dx至少有一个发散，则称\int_{-\infty}^{+\infty}f(x)dx发散
\end{aligned}
$$
**定理1(比较判别法)**

设f(x),g(x)在[a,+∞)上连续，且0≤f(x)≤g(x)，则
$$
(1)当\int_a^{+\infty}g(x)dx收敛时,则\int_a^{+\infty}f(x)dx收敛
\\
(2)当