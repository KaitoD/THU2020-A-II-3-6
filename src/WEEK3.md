# 第三周知识总结
## 混合偏导数
- $定义$
- $邻域内均连续，则f^{''}_{xy} = f^{''}_{yx}$
- $f^{'}_x, f^{'}_y 在\delta邻域内存在，且f^{''}_{xy}在P_0连续，则f^{''}_{yx}(P_0)存在，且f^{''}_{xy}(P_0) = f^{''}_{yx}(P_0)$
## 方向导数
$def.\ 方向向量:
z=f(x,y)在B(P_0,\delta)有定义，\vec v = (v_1,v_2)^T为直线l方向单位向量(\|\vec v\|=1)
若\lim\limits_{t \to 0^+}\frac{f(x_0+tv_1,y_0+tv_2)-f(x_0,y_0)}{t}存在，则称之为f(x,y)在P_0沿\vec v方向导数，记作\frac{\partial f}{\partial \vec v}$
- $几何意义：f(x,y)在P_0沿\vec v 变化率$
- $理解：一条相切射线$
- $任意方向导数存在\neq函数连续，反例:
y=x^2时f(x,y)=1(x>0),else:f(x,y)=0$
### 梯度
$ def.\ 梯度gradf(P_0)=(f'_x(P_0),f'_(P_0))^T$
$ 表示：梯度算子\nabla=(\frac{\partial}{\partial x},\frac{\partial}{\partial y})$
性质：
> 最大(小)方向导数=(-)梯度的长度（与梯度方向相同(反)）
> 方向导数=0 —— 与梯度方向垂直
## 向量值函数
### 映射
一个对一个（确定的左元有唯一右元）
### 向量值函数
$映射F: R^n \to R^m, Y=F(X)$
$ 等价于一个数值函数组$
> 连续性
> 极限
> ......
### 一些简单的线性代数知识（相信大家都会）
线性映射与矩阵、矩阵的范数
### 向量值函数微分
$ X_0,\Delta \in R^n, F: R^n \to R^m$
$ 若\Delta F=A\Delta X+\alpha (\Delta X)$
$ 其中A\in M_{m\times n},\lim\limits_{\|\Delta X\|\in 0}\frac{\|\alpha (\Delta X)\|}{\Delta X}=0$
$ 则称F在X_0可微 \Leftrightarrow 坐标函数均可微$
$ A为Jacobi矩阵：JF(X_0),\frac{\partial (f_1,...,f_m)}{\partial (x_1,...,x_n)}$
$ 微分映射dF(X_0)=JF(X_0)dX$
### 复合映射微分
$ f:R^n \to R^m g:R^m \to R^k 均可微$
$ 则g\circ f可微，J(g\circ f)(X_0)=Jg(U_0)\times Jf(X_0)$