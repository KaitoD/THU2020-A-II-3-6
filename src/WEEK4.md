# 第四周知识回顾
## 逆映射微分
$ def.\ k阶连续可微:$
$ D \subset R^n,C^k(D)\Leftrightarrow D上k阶偏导连续，又称为k阶连续可微$
$ 设\Omega \subset R^n, y=f(x):\Omega\rightarrow R^n 连续可微映射，X_0\in \Omega$
$ 若Jf(X_0)可逆,则\exist y_0 = f(X_0)的邻域U及y=f(X)的逆映射X=f^{-1}(y):U\rightarrow R^n$
$ \forall y\in U, X=f^{-1}(y),Jf^{-1}(y)=(Jf(X))^{-1}$
## 多元函数微分学几何应用
### 空间直线方程
#### 参数方程
$ l:过M_0(x_0,y_0,z_0), 方向向量\vec v=(v_1,v_2,v_3)^T$
$ \forall M(x,y,z)\in l,\vec {M_0M} // \vec v即\vec {M_0M} = t\vec v,\forall t \in R,l参数方程:$
$\left\{
    \begin{aligned}
    x=x_0+tv_1 & \\
    y=y_0+tv_2 & \\
    z=z_0+tv_3 &
    \end{aligned}
\right.$
#### 点向式方程
$ \frac{x-x_0}{v_1}=\frac{y-y_0}{v_2}=\frac{z-z_0}{v_3}$
#### 空间曲线的切线
$\left\{
    \begin{aligned}
    x=x(t) & \\
    y=y(t) & \\
    z=z(t) &
    \end{aligned}
\right.$
$ P_0(x_0,y_0,z_0),x,y,z可导$
$ 切线:$
$ \frac{x-x_0}{x'(t_0)}=\frac{y-y_0}{y'(t_0)}=\frac{z-z_0}{z'(t_0)}$
$ 切向量:$
$ \vec v=(x'(t_0),y'(t_0),z'(t_0))^T$
### 空间曲面切平面与法线
#### 曲面S一般方程
$ F(x,y,z)=0,F在M_0(x_0,y_0,z_0)可微，梯度不为0$
$ S上过M_0任取光滑L，则有$
$ F'_x(M_0)x'(t_0)+F'_y(M_0)y'(t_0)+F'_z(M_0)z'(t_0)=0$
$ 切面方程F'_x(M_0)(x-x_0)+F'_y(M_0)(y-y_0)+F'_z(M_0)(z-z_0)=0$
$ 法线\frac{x-x_0}{F'_x(M_0)}=\frac{y-y_0}{F'_y(M_0)}=\frac{z-z_0}{F'_z(M_0)}$
$ 法向量\vec n=gradF(M_0)$
#### 函数方程
$ z=f(x,y)\in C^{1},可转化为上述方程\Rightarrow f(x,y)-z=0$
#### 参数方程
$\left\{
    \begin{aligned}
    x=x(u,v) & \\
    y=y(u,v) & \\
    z=z(u,v) &
    \end{aligned}
\right.$
##### 切平面一般方程
$ fix:u=u_0\ or\ v=v_0,得到切向量:$
$ \vec a =(x'_u,y'_u,z'_u)^T,\vec b =(x'_v,y'_v,z'_v)^T$
$ 法向量\vec n=\vec a \times \vec b=(A,B,C)$
$ 切平面: A(x-x_0)+B(y-y_0)+C(z-z_0)=0$
$ 法向量: \frac{x-x_0}{A}=\frac{y-y_0}{B}=\frac{z-z_0}{C}$
### 空间曲线切线与法平面
#### 参数方程
$\left\{
    \begin{aligned}
    x=x(t) & \\
    y=y(t) & \\
    z=z(t) &
    \end{aligned}
\right.$
上文已有例子
#### 一般方程
$\left\{
    \begin{aligned}
    F(x,y,z)=0 & S_1\\
    G(x,y,z)=0 & S_2
    \end{aligned}
\right.$
$ S_i切平面法向量\vec n_i=gradF/G(P_0)$
$ 切向量\vec \tau = \vec n_1 \times \vec n_2 = (A,B,C)^T$
$ 切线: \frac{x-x_0}{A}=\frac{y-y_0}{B}=\frac{z-z_0}{C}$
$ 法平面: A(x-x_0)+B(y-y_0)+C(z-z_0)=0$
## 二元函数Taylor公式
### 二元函数高阶全微分
$ d^n f(x,y)=\sum\limits_{i=0}^{n}=\frac{n!}{i!(n-i)!}\frac{\partial^n f}{\partial x^i \partial y^{n-i}}h^i k^{n-i}=(\frac{\partial}{\partial x}h+\frac{\partial}{\partial y}k)^n f(x,y)$
### Lagrange余项型
$ f(x,y)\in C^{n+1}(D),P_0(x_0,y_0),h=x-x_0,k=y-y_0,\theta \in (0,1)$
$ f(x,y)=\sum\limits_{i=0}^n \frac{d^i f(x_0,y_0)}{i!}+\frac{d^{n+1} f(x_0+\theta h,y_0+\theta k)}{(n+1)!}$
$ 最后一项即Lagrange余项$
### Taylor多项式
$ T_f=\sum\limits_{i=0}^n \frac{d^i f(x_0,y_0)}{i!}$
### Peano余项型
$ f(x,y)=T_f(x,y)+o((\sqrt{(x-x_0)^2+(y-y_0)^2})^n)$
## 多元函数极值
$ def.\ 极值点：$
$ f在B(P_0,\delta)有定义,P_0(x_0,y_0)\in R^2$
$ \forall P\in B(P_0,\delta)有f(x,y)\leq f(P_0)or\ f(P_0)\leq f(x,y)\Rightarrow f在P_0取极大(小)值，P_0称为极大(小)值点$
> 一定是内点，局部性质
$ def.\ 驻点or临界点：$
$ f在P_0处存在偏导数，且f'_x(P_0)=f'_y(P_0)=0$
$\Rightarrow P_0为驻点$
> 极值点且可微则必为驻点