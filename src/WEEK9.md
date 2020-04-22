# 第九周知识总结
## 曲线积分
### 第一型曲线积分
$L\subset R^3可求长曲线段 f定义在L上$
$对L的任意划分T,\Delta l_i为弧长$
$ 若I=\lim\limits_{|T|\to0} \sum\limits_{i=1}^n f(P_i)\Delta l_i存在且与划分、取点无关，称之为f在L上第一型曲线积分$
$ 记作\int_L f(x,y,z)dl(环路：\oint_L)$
#### 计算
$L:参数方程x=x(t),y=y(t),z=z(t),t\in[\alpha,\beta],x,y,z\in C^1[\alpha,\beta]$
$dl=\sqrt(x'(t)^2+y'(t)^2+z'(t)^2)dt$
$\int_L f(x,y,z)dl=\int_\alpha^\beta f(x(t),y(t),z(t))\sqrt(x'(t)^2+y'(t)^2+z'(t)^2)dt$
#### 性质
- 线性
- 积分曲线可加性
- 无方向性
- 绝对可积性
- 对称性（曲线对称+函数对称）
- 轮换对称性
#### 积分中值定理
$ f\in C(L),L光滑\Rightarrow \exist P_0(x_0,y_0,z_0)\in L,\int_L f(x,y,z)dl=f(P_0)l$
#### 应用
$柱面侧面积：S=\int_L|f(x,y)|dl$
### 第二型曲线积分
$L可求长,\vec F(x,y,z)=(P,Q,R),d\vec l=(dx,dy,dz)$
$ I=\int_L \vec F(x,y,z)d\vec l=\int_L Pdx+Qdy+Rdz$
#### 计算
$ L:参数方程x=x(t),y=y(t),z=z(t),t\in[\alpha,\beta],x,y,z\in C^1[\alpha,\beta],\alpha\to\beta$
$ d\vec l=\vec \tau dt=(x'(t),y'(t),z'(t))dt$
#### 性质
- 线性
- 积分曲线可加性
- 有向性（正向=-反向）