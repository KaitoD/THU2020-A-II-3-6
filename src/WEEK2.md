# 第二周知识点回顾
## 二元函数的连续与偏导数
### 二元函数的连续性
#### 二元函数在一点处连续
$ def.\ 二元函数连续:\\
f(x,y)定义在D\subset R^2上,P_0(x_0,y_0)\in D,若\forall\epsilon\gt 0,\exists\delta\gt 0,\forall P(x,y)\in B(P_0,\delta)\cap D,有|f(x,y)-f(x_0,y_0)|\lt\epsilon\\
\Rightarrow f在P_0(x_0,y_0)连续,P_0为f连续点\\
即：\lim\limits_{(x,y)\to(x_0,y_0)}f(x,y)=f(x_0,y_0)$
几个注解：
> 情形1. $ P_0为聚点 \Leftrightarrow 与点列极限的联系$
> 情形2. $P_0为非聚点 \Rightarrow 是孤立点$

$ def.\ 间断点:不连续的点$
- 可去间断点：极限存在
- 本性间断点：极限不存在
#### 二元函数在点集上连续
$ def.\ 在点集上连续：\\
f在D中每个点都连续\Leftrightarrow f\in C(D)$
### 二元函数对变量分别连续
$ def.\ 对变量连续：\\
固定一个变量，考虑另一个变量构成的一元函数的连续性$
* 注意，【对两个变量连续】与【函数连续】互不蕴含

### 连续函数的几个性质
- 有界性
- 最值性
- 介值性

## 二元函数的偏导数
$ def.\ 偏导数：\\
f(x,y)在P_0(x_0,y_0)的\delta内连续,固定一个变量，得到的一元函数在邻域内可导，导数为f关于这一变量的偏导数\\
记作\frac{\partial f}{\partial x}(x_0,y_0),\frac{\partial f}{\partial y}(x_0,y_0)$
* 注意：二元函数在一点的偏导数存在性与函数连续性互不蕴含

### 偏导数几何意义
二元函数：$ R^3$中的曲面
固定一个变量：确定在一个切面
求导：曲面与切面交线在该点的切线斜率

## 可微
与一元函数类似，对于函数一点微扰的线性近似拟合。
$ def.\ 全微分\\
z=f(x,y),P_0(x_0,y_0),\Delta z=f(x_0+\Delta x,y_0+\Delta y)-f(x_0,y_0)=A\Delta x+B\Delta y+o(\sqrt{\Delta x^2+\Delta y^2})\\
则称f在P_0处可微，dz=A\Delta x+B\Delta y$
### 可微的几个定理
- $ A=\frac{\partial z}{\partial x},B=\frac{\partial z}{\partial y}$
- $f(x,y)在P_0处连续$
- $两个偏导数在P_0处均连续\Rightarrow f在P_0处可微（逆定理不成立！）$
### 可微的条件
- 充要条件：$ f(x,y)在P_0(x_0,y_0)可微\Leftrightarrow f在P_0处全改变量\Delta f=f'_x(P_0)\Delta x+f'_y(P_0)\Delta y+\epsilon_1\Delta x+\epsilon_2\Delta y,\ 其中：\lim\limits_{(\Delta x,\Delta y)\to(0,0)}\epsilon_i=0$
- 证明可微：充分条件，定义；证明不可微：必要条件
### 全微分应用——近似计算
$ 设f(x,y)在P_0(x_0,y_0)处可微，则\\
\Delta f=f(x_0+\Delta x,y_0+\Delta y)-f(x_0,y_0\\
=f'_x(P_0)\Delta x+ f'_y(P_0)\Delta y+o(\sqrt{\Delta x^2+\Delta y^2})\\
当\Delta x\to 0,\Delta y\to 0:\\
f(x_0+\Delta x,y_0+\Delta y)=f(x_0,y_0)+f'_x(P_0)\Delta x+ f'_y(P_0)\Delta y$

## 复合函数微分
链式法则
### 二元函数套一元函数
$ z=f(x,y)可微,x=x(t),y=y(t)可导,则\\
z=f(x(t),y(t))可导且\frac{dz}{dt}=\frac{\partial f}{\partial x}x'(t)+\frac{\partial f}{\partial y}y'(t)$
### 推广：n元函数套一元函数
$ z=f(x_1,x_2,...,x_n)可微,x_i=x_i(t)可导,则\\
z=f(x_1(t),x_2(t),...,x_n(t))可导且\frac{dz}{dt}=\sum\limits_{i=1}\limits^n\frac{\partial f}{\partial x_i}x_i'(t)$
### 推广：n元函数套m元函数
$ z=f(x_1,x_2,...,x_n)可微,x_i=x_i(t_1,t_2,...,t_m)存在偏导,则\\
z=f(x_1(t_1,...,t_n),...,x_n(t_1,...,t_n))可导且\frac{\partial z}{\partial t_i}=\sum\limits_{j=1}\limits^n(\frac{\partial f}{\partial x_j}\frac {x_j}{t_i})$
## 高阶偏导数
$ 设f(x,y)定义在D\subset R^2,\ \forall (x,y)\in D,有f'_x(x,y),f'_y(x,y)\\
\forall P_0(x_0,y_0)\in D,f'_x(x,y)在P_0关于x偏导数，fix y=y_0,若\lim\limits_{ x \to x_0}\frac{f'_x(x,y_0)-f'_x(x_0,y_0)}{x-x_0}存在，\\
称之为f在P_0处的二阶偏导，记作\frac{\partial^2 f}{\partial x^2}(x_0,y_0),y同理;若f'_x(x,y)对y求偏导——混合偏导数\frac{\partial^2 f}{\partial y\partial x}(x_0,y_0)$
> $一般来讲，\frac{\partial^2 f}{\partial x\partial y}\neq\frac{\partial^2 f}{\partial y\partial x}$
> $但当混合偏导数在P_0(x_0,y_0)附近连续，则混合偏导数相等$