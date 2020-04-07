# 第七周知识回顾
## 二重积分
### 积分定义
$ 设D \subset R^2 为有界区域，f(x,y)定义在D上$
$ 对D的任意分割T，|T|=max{d(\Delta D_i)|i=1,2...n}$
$ \lim\limits_{|T|\to 0}\sum\limits_{i=1}^n f(x_i,y_i)\Delta \sigma_i=\iint\limits_D f(x,y)d\sigma$
$ f\in R(D)——可积函数族全体$
$ \iint\limits_D d\sigma=S(D)——面积$
### 可积必要条件
$ f\in R(D)\Rightarrow f在D上有界$
### 可积充分条件
$ D有界闭域,f\in C(D) \Rightarrow f\in R(D)$
### 可积充要条件
$ 达布上和=达布下和\Leftrightarrow f\in R(D)$
$ D有界闭域,f有界且间断点集是一个零面积集 \Leftrightarrow f\in R(D)$
### 性质
- 线性
- 积分区域可加性
- 保序性
- 绝对可积性
- 积分中值定理
- 对称性（计算常用）
### 计算
#### 直角坐标系
$ d\sigma=dxdy$
- 矩形区域$ D=[a,b]\times[c,d], \iint\limits_D f(x,y)dxdy=\int_c^d dy\int_a^b f(x,y)dx$
- $ D=\{(x,y)|a\leq x\leq b, y_1(x)\leq y \leq y_2(x)\}, \iint\limits_D f(x,y)dxdy=\int_a^b dy\int_{y_1(x)}^{y_2(x)} f(x,y)dx$
- 参数方程$D\in xoy,\Omega \in uov,x=x(u,v),y=y(u,v)为可逆双射，则\iint\limits_D f(x,y)dxdy=\iint\limits_{\Omega} f(x(u,v),y(u,v))|det\frac{\partial(x,y)}{\partial(u,v)}|dudv$