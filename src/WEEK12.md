# 第12周知识回顾
## 第二型曲面积分
### 物理来源——流体流量问题
$流体流量：\vec F(M)=(P(M),Q(M),R(M)),双侧曲面S\\
求单位时间流体从S一侧流向另一侧的流量$
$对S分割T(S_1,S_2,...,S_N), 单位法向量\vec n_i\\
V=\lim\limits_{|T|\to 0}\sum\limits_{i=1}^n\vec F(M_i)\cdot \vec n_i \varDelta S_i$
### 定义
$\vec F(M)=(P(M),Q(M),R(M)) 定义在双侧曲面S上\\
若上述极限存在且与划分方式和选点方式无\\
则称这个极限为\vec F沿S一侧的第二型曲面积分，记作:$
$\iint\limits_{S^+}Pdy\Lambda dz+Qdz\Lambda dx + Rdx\Lambda dy\\
\iint\limits_{S^+}\vec F\cdot\vec n dS=\iint\limits_{S^+}\vec F\cdot d\vec S\\
\iint\limits_{S^+}(P\cos\alpha+Q\cos\beta+R\cos\gamma)dS$
### 计算
- $ S:\ z=f(x,y)\in C^1(D),D\subset R^2有界闭区域\\
\iint\limits_{S^+}Pdy\Lambda dz+Qdz\Lambda dx + Rdx\Lambda dy\\=\iint\limits_{S^+}(P\cos\alpha+Q\cos\beta+R\cos\gamma)dS\\=\pm\iint\limits_{D}(P(x,y,f(x,y))f'_x +Q(x,y,f(x,y))f'_y -R(x,y,f(x,y)))dxdy$
- $ S:(x,y,z)=(x(u,v),y(u,v),z(u,v)),x,y,z\in C^(D),(u,v)\in D有界闭区域\\
\iint\limits_{S^+}Pdy\Lambda dz+Qdz\Lambda dx + Rdx\Lambda dy\\=\iint\limits_{S^+}(P\cos\alpha+Q\cos\beta+R\cos\gamma)dS\\=\pm\iint\limits_{D}(P(x,y,z)A +Q(x,y,z)B +R(x,y,z)C)dudv$
## Gauss公式
$Thm.V\subset R^3 有界闭域，由可求面积的封闭曲面S围成\\
若P,Q,R\in C^1(V),则：\\
\oiint\limits_{S^+}Pdy\Lambda dz+Qdz\Lambda dx + Rdx\Lambda dy=\iiint\limits_V (\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z})dxdydz$
证明类似于Green公式（三维延拓）
### 应用
- P,Q,R在V内有奇点——切除奇点
- 计算开口曲面积分——补上一块易于计算的部分变为封闭曲面
- 计算空间区域的体积——Gauss公式逆向使用
## Stokes公式
$曲面S\to边界曲线L，通过右手定则给定方向（在曲面方向规定的前提下）\\
Thm.S光滑双侧曲面，边界L是可求长封闭曲线\\
P,Q,R\in C^1(S),C^1(L),则:\\
\oint_{L^+}Pdx+Qdy+Rdz=\iint\limits_{S^+}(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z})dy\Lambda dz+(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x})dz\Lambda dx + (\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})dx\Lambda dy\\
Stokes公式与曲面形状无关$