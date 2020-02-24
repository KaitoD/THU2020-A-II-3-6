# 第一周知识点回顾
## 点集拓扑与多元函数
### 点集拓扑
#### 距离概念引入
$ 线性空间 R^n中:$ 
 $\qquad def.\ 内积: \forall X(x_1,x_2,...,x_n),Y(y_1,y_2,...,y_n) \in R^n,{<}X,Y{>}=\sum\limits_{i=1}^n x_iy_i$
>  性质:
[1] 非负性
[2] 对称性
[3] 线性

$ 进一步地$
$ \qquad def.\ n维欧氏空间: 定义了内积的R^n空间$
$ \qquad def.\ 欧式范数: \forall X \in R^n, \|X\|=\sqrt{<X,X>}$
> 性质：
[1] 非负性
[2] 数乘线性
[3] 三角不等式 （以及Cauchy-Schwarz 不等式）

推广
$ \qquad def.\ 范数:定义在R^n上的，满足上述三条性质的函数$

基于范数，有
1. 距离：
- 点与点$\forall X(x_1,x_2,...,x_n),Y(y_1,y_2,...,y_n):\\
d(X,Y)=\|X-Y\|$
- 点与点集
$ X\in R^n,\Omega \subset R^n:\\
d(X,\Omega)=inf\{\|X-Y\||\forall Y\in \Omega\}$
- 点集与点集
$ \Omega , \Lambda \subset R^n:\\
d(\Omega,\Lambda)=inf\{\|X-Y\||\forall X\in \Omega,\forall Y \in \Lambda\}$
2. 点集的直径
$ \Omega \subset R^n:
diam(\Omega)=sup\{\|X-Y\||\forall X,Y \in \Omega\}$

#### 邻域
$ 对于X_0 \in R^n, \forall \delta > 0$
$def.\ \delta-邻域:\\
B(X_0,\delta)=\{X\in R^n|\|X-X_0\|<\delta\}$
$ def.\ 去心\delta-邻域：\\
B_0(X_0,\delta)=\{X\in R^n|0<\|X-X_0\|<\delta\}$

#### 点与点集关系
- 点的位置
$ def.\ 内点:\\
\exist\delta>0,s.t.\ B(X,\delta) \subset \Omega\\
\Rightarrow \Omega内点集合构成内部(\mathring{\Omega})$
$ def.\ 外点:\\
\exists\delta>0,s.t.\ B(X,\delta)\cap\Omega=\emptyset\\
\Rightarrow\Omega外点集合构成外部$
$ 余集 \Omega^c=R^n \backslash \Omega$
$ \diamond余集中的点不一定是外点，外点是余集中的点$
$ def.\ 边界点:\\
任意邻域内同时含有内点与外点$
- 稠密性
$ def.\ 聚点:\\
\forall \delta >0,B_0(X,\delta)\cap\Omega≠\empty\\
\Rightarrow \Omega聚点集合构成\Omega导集(\Omega')\\
\Rightarrow cl(\Omega)=\bar\Omega=\Omega\cup\Omega'为闭包$
$ def.\ 孤立点:\\
\exists\delta>0,s.t.B(X,\delta)\cap\Omega=\{X\}$
#### 开集&闭集
$对于\Omega\subset R^n\\
\mathring{\Omega}=\Omega \rightarrow开集\\
\bar\Omega=\Omega\rightarrow闭集\\
约定R^n,\empty既开又闭$
任意多开集的并是开集
有限个开集的交是开集
任意多闭集的交是闭集
有限个闭集的并是闭集（迪摩根律）
#### 有界集
$\Omega\subset R^n,\exist r>0,s.t.\Omega\subset B(0,r),称\Omega是有界集$
#### 点列收敛
$n\to \infty, \|X_n-X_0\|\to0\\
\Rightarrow收敛于X_0$
按各个坐标分量收敛
收敛点集有界
#### 完备性
基本列：高维柯西列
定理：
- Cauchy收敛定理：基本列等价于收敛列
- 闭集$ \Omega$的收敛子点列的极限属于$\Omega$
- $R^n$是完备的：$R^n$中基本列收敛到$R^n$
- 七个等价结论（与一元函数类似）
#### 连通集
道路连通：两点可由一条内部折线联结
连通集：任意两点道路连通
#### 区域
- $R^n$中连通非空开集称为开区域
- 开区域的闭包就是闭区域
### 多元函数
$def.\ 多元数值函数：\\
\Omega \subset R^n,映射\Omega\stackrel{f}\to u,称f为定义在\Omega上的n元函数$
掌握几个典型二元函数例子
## 二元函数极限
### 在一点处极限（二重极限）
$def.\ 二重极限：聚点P_0(x_0,y_0)\in\Omega\subset R^2,f(x,y)在B_0(P_0,\delta_0)\cap\Omega上有定义, a(const)\in R\\
若\forall \epsilon>0, \exist \delta>0(\delta_0>\delta), s.t.\forall P(x,y)\in B_0(P_0,\delta)\cap\Omega:\\
|f(P)-a|<\epsilon\\
称P\to P_0时,f(P)有极限a$

计算：换元、夹逼（很常用，正负想不明白时可以加绝对值）
推论：两条路径极限不同，则极限不存在
### 累次极限
- 定义略（先取x/y的极限,后取y/x的极限，另一个作为参数）
- 前提是第一重极限（关于参数的函数）存在
### 累次极限与二重极限关系
1. $\lim\limits_{(x,y)\to(x_0,y_0)}f(x,y)=A\\
且\lim\limits_{x\to x_0}\lim\limits_{y\to y_0}f(x,y)=B, 则A=B$
2. 进一步地，若二重极限和两个累次极限都存在，则三者相等
3. 若两个累次极限存在但不相等，则二重极限不存在
* 注意，累次极限、二重极限的存在性之间没有直接依赖关系