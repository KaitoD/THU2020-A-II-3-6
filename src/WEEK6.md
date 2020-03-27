# 第六周知识回顾
## 含参积分
### 二元函数一致连续性
$ 设f定义在\Omega\subset R^2上，若\forall \varepsilon >0,\exists \delta > 0, s.t. \forall X_1,X_2\in \Omega，只要\|X_1-X_2\|<\delta,|f(X_1)-f(X_2)|<\varepsilon\Rightarrow f在I上一致连续$
$ f\in C(D),D为有界闭集\Leftrightarrow f在D上一致连续$
### 含参定积分
$ I\subset R,D=[a,b]\times I,f(x,u)def on D$
$ \forall u\in I,f(x,u)\in R[a,b],称\phi(u)=\int_a^bf(x,u)dx为含参定积分$
$ 性质：积分与取极限运算可以交换$
$ 在D上连续则积分在I上连续$
$ 求导运算：f'_u(x,u)\in C(D)\Rightarrow\phi'(u)=\int_a^b f'_u(x,u)dx$
$ 积分运算：f(x,u)\in C(D)\Rightarrow \phi(u)=\int_a^b f(x,u)dx\in R[a,b],\int_{\alpha}^{\beta}\phi(u)du=\int_a^b(\int_{\alpha}^{\beta}f(x,u)du)dx(积分的可交换性)$
$ 变限求导：f'_u(x,u)\in C(D),a(u),b(u)在[\alpha,\beta]上可导，\forall u\in[\alpha,\beta],a(u),b(u)\in [a,b]\Rightarrow\phi'(u)=\int_{a(u)}^{b(u)}f'_u(x,u)dx+b'(u)f(b(u),u)-a'(u)f(a(u),u)$
### 含参广义积分
$ D=[a,+\infty)\times I,f def on D$
$ \forall u\in I,\int_a^{+\infty}f(x,u)dx收敛\Rightarrow \phi(u)=\int_a^{+\infty}f(x,u)dx为含参数u无穷积分$
#### 一致收敛
$ \forall \varepsilon >0,\exists M>a,\forall A>M,\forall u\in I,有|\int_a^Af(x,u)dx-\int_a^{+\infty}f(x,u)dx|<\varepsilon \Rightarrow \int_a^{+\infty}f(x,u)dx在I上一致连续$
$ Cauchy一致收敛原理:$
$ \forall \varepsilon >0,\exists M>a,\forall A_1,A_2>M,及\forall u\in I,有|\int_{A_1}^{A_2}f(x,u)dx|<\varepsilon$
$ \Rightarrow \int_a^{+\infty}f(x,u)dx在I上一致收敛$
判别：($D=[a,+\infty)\times I$)
- $Weirerstrass:f关于x在[a,+\infty)上连续，\exist F(x)\in C([a,+\infty)),F(x)\geq 0,s.t.int_a^{+\infty}F(x)dx,且\forall (x,u)\in D,|f(x,u)|\leq F(x)$
$ \Rightarrow \int_a^{+\infty}f(x,u)dx在I上一致连续$
- $Dirichlet:f,g def on D=[a,+\infty)\times I满足：\\对充分大的积分上界,f一致有界；\\\forall u\in I,g(x,u)关于x单调,\lim\limits_{x\to +\infty}g(x,u)=0关于u一致成立\\\Rightarrow fg一致收敛$
- $Abel:f,g def on D=[a,+\infty)\times I满足：\\\int_a^{+\infty}f(x,u)dx在I上一致收敛\\\forall fix u\in I,g(x,u)关于x单调，关于u\in I一致有界\\fg一致连续$
$ 局部一致收敛：$
$ \forall u_0\in I,在u_0的一个邻域内一致收敛$
- $ 连续性：f(x,u)\in C(D),局部一致收敛\Rightarrow \phi(u)=\int_a^{+\infty}f(x,u)dx \in C(I)$
- $ 可积性：f(x,u)\in C(D),\phi(u)=\int_a^{+\infty}f(x,u)dx在[\alpha,\beta]上一致收敛\Rightarrow \phi(u)\in R[\alpha,\beta],且积分号可交换$
- $ 可微性：f'_u(x,u)\in C(D)且\phi(u)=\int_a^{+\infty}f(x,u)dx在\forall u\in I收敛，\int_a^{+\infty}f'_u(x,u)dx关于u\in I局部一致收敛\Rightarrow \phi(u)\in C^1(I),\phi'(u)=\int_a^{+\infty}f'_u(x,u)dx$
$ \Gamma 函数\Gamma(\alpha)=\int_0^{+\infty}x^{\alpha-1}e^{-x}dx$
$ \Beta 函数\Beta(p,q)=\int_0^{+\infty}x^{p-1}(1-x)^{q-1}dx$