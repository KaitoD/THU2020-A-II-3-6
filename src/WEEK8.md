# 第八周知识回顾
## 三重积分
### 直角坐标系
$ 体积微元：dv = dxdydz$
$ V\subset R^3 有界闭区域\rightarrow I=\iiint\limits_V f(x,y,z)dxdydz$
计算：
- $先一后二：$
$ V=\{(x,y,z)|\forall(x,y)\in D,z_1(x,y)\leq z\leq z_2(x,y)\}$
$ \iiint\limits_V f(x,y,z)dxdydz=\iint\limits_D dxdy\int_{z_1(x,y)}^{z_2(x,y)} f(x,y,z)dz$
- $ 先二后一：$
$ V=\{(x,y,z)|z_1\leq z \leq z_2,(x,y)\in D_z\}$
$ \iiint\limits_V f(x,y,z)dxdydz=\int_{z_1}^{z_2}dz\iint\limits_{D_z}f(x,y,z)dxdy$
### 变量代换
$(x,y,z)\in D \rightarrow (u,v,w)\in \Omega 连续可微双射$
$ \iiint\limits_D f(x,y,z)dxdydz=\iiint\limits_\Omega f(x(u,v,w),y(u,v,w),z(u,v,w))|det\frac{\partial(x,y,z)}{\partial(u,v,w)}|dudvdw$
应用：柱坐标变换，球坐标变换
## 重积分应用
### 几何应用
#### 曲面面积
$ S=\iint\limits_D \sqrt{1+{f'_x}^2+{f'_y}^2}dxdy$
$ 参数方程下，法向量\vec n=(A,B,C),S=\iint\limits_\Omega \sqrt{A^2+{B}^2+{C}^2}dxdy$
### 物理应用
#### 质心计算
位矢关于密度的加权平均
$ 密度函数\rho(x,y,z)$
$ \vec r_c = \frac{\iiint\limits_V \vec r \rho(x,y,z)dv}{\iiint\limits_V \rho(x,y,z)dv}$
#### 转动惯量
$ 密度函数\rho(x,y,z),与转轴l的距离函数r(x,y,z)$
$ J_l=\iiint\limits_\Omega r^2(x,y,z)\rho(x,y,z)dxdydz$
#### 引力
$ 密度函数\rho(x,y,z),与体外一个质点距离函数\vec r(x,y,z)$
$ \vec F=\iiint\limits_\Omega G\frac{m\rho\vec r}{\|r\|^3}dxdydz$