- [GeoGebra 应用案例](#geogebra-%e5%ba%94%e7%94%a8%e6%a1%88%e4%be%8b)
  - [光滑曲面实例](#%e5%85%89%e6%bb%91%e6%9b%b2%e9%9d%a2%e5%ae%9e%e4%be%8b)
  - [分段函数 Piecewise Function](#%e5%88%86%e6%ae%b5%e5%87%bd%e6%95%b0-piecewise-function)
  - [圆到椭圆方法](#%e5%9c%86%e5%88%b0%e6%a4%ad%e5%9c%86%e6%96%b9%e6%b3%95)
    - [伸缩变换：Stretch(圆，向量)](#%e4%bc%b8%e7%bc%a9%e5%8f%98%e6%8d%a2stretch%e5%9c%86%e5%90%91%e9%87%8f)
  - [牛顿迭代法 Newton's Iteration](#%e7%89%9b%e9%a1%bf%e8%bf%ad%e4%bb%a3%e6%b3%95-newtons-iteration)
    - [方法描述](#%e6%96%b9%e6%b3%95%e6%8f%8f%e8%bf%b0)
    - [GeoGebra中演示步骤](#geogebra%e4%b8%ad%e6%bc%94%e7%a4%ba%e6%ad%a5%e9%aa%a4)
    - [Cubic iteration 三次迭代](#cubic-iteration-%e4%b8%89%e6%ac%a1%e8%bf%ad%e4%bb%a3)
    - [举例 - 黄金分割比率 Golden Ratio](#%e4%b8%be%e4%be%8b---%e9%bb%84%e9%87%91%e5%88%86%e5%89%b2%e6%af%94%e7%8e%87-golden-ratio)
  - [点阵和向量阵](#%e7%82%b9%e9%98%b5%e5%92%8c%e5%90%91%e9%87%8f%e9%98%b5)
    - [通项公式](#%e9%80%9a%e9%a1%b9%e5%85%ac%e5%bc%8f)
      - [等比数列 $\{a,ar,ar^2,ar^3,...\}$](#%e7%ad%89%e6%af%94%e6%95%b0%e5%88%97-math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmo-stretchy%22false%22momiamimo-separator%22true%22momiamimirmimo-separator%22true%22momiamimsupmirmimn2mnmsupmo-separator%22true%22momiamimsupmirmimn3mnmsupmo-separator%22true%22momi-mathvariant%22normal%22mimi-mathvariant%22normal%22mimi-mathvariant%22normal%22mimo-stretchy%22false%22momrowannotation-encoding%22applicationx-tex%22aarar2ar3annotationsemanticsmathaarar2ar3)
      - [给点序列生成标签序列](#%e7%bb%99%e7%82%b9%e5%ba%8f%e5%88%97%e7%94%9f%e6%88%90%e6%a0%87%e7%ad%be%e5%ba%8f%e5%88%97)
      - [生成奇数点列 $\{(i, 2i-1),i,1,n\}$](#%e7%94%9f%e6%88%90%e5%a5%87%e6%95%b0%e7%82%b9%e5%88%97-math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmo-stretchy%22false%22momo-stretchy%22false%22momiimimo-separator%22true%22momn2mnmiimimo%e2%88%92momn1mnmo-stretchy%22false%22momo-separator%22true%22momiimimo-separator%22true%22momn1mnmo-separator%22true%22mominmimo-stretchy%22false%22momrowannotation-encoding%22applicationx-tex%22i-2i-1i1nannotationsemanticsmathi2i%e2%88%921i1n)
      - [生成向量列表](#%e7%94%9f%e6%88%90%e5%90%91%e9%87%8f%e5%88%97%e8%a1%a8)
  - [迭代](#%e8%bf%ad%e4%bb%a3)
    - [1. 阶乘的迭代实现 $x_{n+1} \leftarrow  f(x_n)$](#1-%e9%98%b6%e4%b9%98%e7%9a%84%e8%bf%ad%e4%bb%a3%e5%ae%9e%e7%8e%b0-math-xmlns%22httpwwww3org1998mathmathml%22semanticsmrowmsubmixmimrowminmimomomn1mnmrowmsubmo%e2%86%90momifmimo-stretchy%22false%22momsubmixmiminmimsubmo-stretchy%22false%22momrowannotation-encoding%22applicationx-tex%22xn1-leftarrow-fxnannotationsemanticsmathxn1%e2%80%8b%e2%86%90fxn%e2%80%8b)
    - [2. Fibonacci数列的迭代生成](#2-fibonacci%e6%95%b0%e5%88%97%e7%9a%84%e8%bf%ad%e4%bb%a3%e7%94%9f%e6%88%90)
  - [如何制作一根弹簧？](#%e5%a6%82%e4%bd%95%e5%88%b6%e4%bd%9c%e4%b8%80%e6%a0%b9%e5%bc%b9%e7%b0%a7)
  - [优秀共享资源分享](#%e4%bc%98%e7%a7%80%e5%85%b1%e4%ba%ab%e8%b5%84%e6%ba%90%e5%88%86%e4%ba%ab)


# GeoGebra 应用案例

## 光滑曲面实例

$s1: z(x,y)=xy$
![z(x,y)=xy](images\xy.png)

$s2: z(x,y)=sin(x) sin(y)$
![z(x,y)=sin(x)sin(y)](images\sin(x)sin(y).png)

$s3: z(x,y)=cos(x) cos(y)$
![z(x,y)=cos(x)cos(y)](images\cos(x)cos(y).png)

$s4: z(x,y)=cos(x-y) \iff s2(x,y) + s3(x,y)$
![z(x,y)=cos(x-y)](images\cos(x-y).png)

$s5: z(x,y)=cos(x+y) \iff -s2(x,y) + s3(x,y)$
![z(x,y)=cos(x+y)](images\cos(x+y).png)

$s6: z(x,y)=sin(x-y) \iff sin(x) cos(y)- cos(x) sin(y)$
![z(x,y)=sin(x-y)](images\sin(x-y).png)

$s7: z(x,y)=sin(x+y) \iff sin(x) cos(y) + cos(x) sin(y)$
![z(x,y)=sin(x+y)](images\sin(x+y).png)


## 分段函数 Piecewise Function

绘制分段函数图像：

$$f(x) = \begin{cases}
    e^x & x<0 \\
    x^2 & 0 \leq x \leq 1 \\
    1   & x > 1
\end{cases}$$

输入命令：`if(x < 0, ℯ^x, if(x ≤ 1, x², 1))`

利用“逻辑变量”，还可以输入：

`f(x) = ℯ^x (x < 0) + x² (0 ≤ x ≤ 1) + (x > 1)`

解释：逻辑值 False = 0, True = 1. 所以 上述 `e^x (x < 0 )` 表示 $e^x$ 乘以 逻辑值 $(x<0)$.   

![分段函数输入命令](images\piecewise-function.png)

## 圆到椭圆方法

如何将一个圆变成一个椭圆？

### 伸缩变换：Stretch(圆，向量)

输入命令： $Stretch(circle, r \vec u), r$ 为伸缩比例。中文指令：`伸缩(d, r 向量(u))`， 此处 $\vec{u}=(1,0)$ 在 $x$ 轴方向上缩放，如 $\vec{v}=(0,1)$, 则在 $y$ 轴方向上缩放。向量$\vec u$和$\vec v$组合起来，就可以构成斜椭圆。参见下图

![伸缩变换-圆到椭圆](images\圆到椭圆.gif)


## 牛顿迭代法 Newton's Iteration

### 方法描述
Let $f: \Reals \to \Reals, x \mapsto f(x)$ be a differentiable function where $f'(x) \neq 0$ for all $x$ and $x_0$ be an initial (not necessarily good) guess for $f(x)=0$ then the recursive application of  
$$x_{n+1}=x_n-\dfrac{f(x_n)}{f'(x_n)}   \qquad  (1)$$
yields a better approximation for a zero crossing.

主要用来解决方程 $f(x)=0$ 的精确求根，假设 $f(x)$ 是给定区间的 $C^2 \; Function$ 函数，即两阶连续函数，根据Taylor展开得到 $x$ 附近的展开式：

$$f(x+\delta)=f(x)+\delta f'(x)+O(\delta ^2)$$

当 $\delta$ 很小时，即 $|\delta|<\varepsilon$, 有 $f(x+\delta) =0 \approx f(x)+\delta f'(x)$

$$\delta=-\dfrac{f(x)}{f'(x)} \\[2ex]
x+\delta = x-\dfrac{f(x)}{f'(x)}$$

从而 Newton 迭代就是寻找 $(1)$式中的数列 $\{x_n\}$的极限值。

注意：上述迭代方法，在很多情况下不收敛(not converge,we say chaotic sometimes)，即极限不存在。

### GeoGebra中演示步骤
1. 建立函数 `f: x^2-ln(x)-2` | $f: x^2-ln(x)-2$
2. 根据牛顿迭代法，求出迭代函数 `g: x - f(x)/f'(x)` | $g: x - f(x)/f'(x)$
3. 为了控制迭代次数，建立一个滑动条 `n=Slider(0,10,1)`
4. 给定迭代初始值 $x_0 = 3$, 根据不同函数，应取靠近可能的根附近的任意数
5. 为了保留迭代过程，创建一个迭代列表 `xn=IterationList(g(x), x_0, n)`
6. 根据上述迭代列表，创建$x$轴上的点列 `px=Zip((t,0),t,xn)`, 注意，这里的 $t$ 不能用 $x$ 变量代替，因为 $x$ 在GeoGebra中有特殊含义
7. 同样，通过 `xn` 创建函数f(x)上的点列 `pf=Zip((t,f(t)),t,xn)`
8. $f(x)$ 在 $(x_i,f(x_i)), i \in [0,n]$ 处切线列表 `tang=Zip(tangent(p,f), p, pf)`
9. 得到$x$轴上的分点$(x_i,0), i \in [0,n]$到函数$f(x)$上的点$(x_i,f(x_i)), i \in [0,n]$之间的线段 `seg=Zip(Segment(p,q),p,px, q,pf)`
10. 建立一个按钮 `Button("开始动画")`， 在属性-脚本-单击时，添加代码 `StartAnimation(n)`
11. 为了显示结果，建立文本`text1:"方程\;" + (公式文本(f))+ "= 0 的根为 \; \color {red}"+(公式文本(a))+""`

![newton's iteration](images\newton_iteration.gif)

### Cubic iteration 三次迭代
比上述多取一项，成为二次多项式：
$$f(x+\delta)=f(x)+\delta f'(x)+ \frac{\delta ^2}{2}f''(x)+ O(\delta ^3)$$

当 $\delta$ 很小时，有 $f(x+\delta) =0 \approx f(x)+\delta f'(x)+\frac{\delta ^2}{2} f''(x)$

解上述关于 $\delta$ 的一元二次方程，假定 $f'(x) \cdot f''(x) \neq 0$, 得到：

$$\delta=-\dfrac{f'(x)}{f''(x)} \Bigg(1-\sqrt{1-\frac{2f(x)f''(x)}{f'(x)^2}} \Bigg)$$

这里没有必要计算平方根，因为当 $f(x)$ 很小时，可以用展开式 $1-\sqrt{1-a}=\dfrac{a}{2}-\dfrac{a^2}{8}+O(a^3)$

从而 
$$ \delta = -\frac{f(x)}{f'(x)}\Big(1+\frac{f(x) \cdot f''(x)}{2f'(x)^2}+\cdots \Big)\\[2ex]
x+\delta = x-\dfrac{f(x)}{f'(x)}\Big(1+\frac{f(x) \cdot f''(x)}{2f'(x)^2}\Big)$$

**Househoulder's iteration**

给定初值 $x_0$, 迭代序列如下：
$$x_{n+1}=x_n-\dfrac{f(x_n)}{f'(x_n)}\Big(1+\frac{f(x_n) \cdot f''(x_n)}{2f'(x_n)^2}\Big)$$

还可以推广到 Higher order iteration 更高阶的迭代

### 举例 - 黄金分割比率 Golden Ratio

如何计算黄金分割数 $\varphi = \dfrac{1+\sqrt 5}{2}$?

首先，$\varphi =\frac{1}{2}+x, x=\sqrt{5}/2, x$ 是方程 $\frac{1}{x^2}-\frac{4}{5}=0$ 的根。

取 $f(x)=1-\frac{4}{5} x^2$, 求 $f(x)=0$ 的根.

## 点阵和向量阵

### 通项公式

点阵中点的坐标可用含点序号的关系式直接表示出来，如同数列的通项公式，已知点的序号，就可求得该点的坐标。  
通项法从实现上来看，似乎很简单，实际上制作点阵的所有方法中，通项法是最难的，是需要很深的数学功底。

通用指令有两种情况：
- Sequence(含有变量 i 的通项,i,1,n)
- Flatten(Sequence(Sequence(含有i和j的通项,i,i最小值,i最大值),j,j最小值,j最大值))

#### 等比数列 $\{a,ar,ar^2,ar^3,...\}$

通项公式为 $x_n = a r^{n}, n \in N$

`序列(a r^n, n, 0, 10)`, `Sequence(a r^n, n, 0, 10)`: 生成等比数列的前11项，结果为列表 $\{a, ar, ar^2, ..., ar^{10}\}$。

#### 给点序列生成标签序列
- 随机生成点序列 `L_{P} = Sequence(RandomPointIn(0, 4, 0, 4), k, 1, 11)`
- 用 `Tex` t命令生成点序列的标签序列 `L_{L} = Sequence(Text("P_{" + (k) + "}", Element(L_{P}, k), true, true), k, 1, Length(L_{P}))`

![text label](images\text_label.png)

#### 生成奇数点列 $\{(i, 2i-1),i,1,n\}$
- 生成滑动条 n = Slider(1,20)
- 产生奇数点列 Sequence((i,2 i-1),i,1,n)：{(1,1),(2,3),{3,5},(4,7),(5,9)}

#### 生成向量列表
- 起点在x轴上的向量列表 `Sequence(Vector((k, 0), (k+1, 2)), k, -3, 3, 0.5)`
- 向量矩阵 `Sequence(Sequence(Vector((k, j), (k +1, j+0.5)), k, -3, 3), j, 0, 4)`

## 迭代

### 1. 阶乘的迭代实现 $x_{n+1} \leftarrow  f(x_n)$
形如 $a_{k+1}=f(k,a_k), k>s$, 给定初始值为 $(s,a_s)$, 得到 列表$\{a_s, a_{s+1}, \cdots, a_{s+n} \}$

如：定义 $f(k,a)=(k+1)*a$，输入 $factorial = IterationList(f, {2, 2},5)$ 可以得到 $factorial = \{2,6,24,120,720\}$，这就是 **阶乘** 的迭代实现方法。这里的初值也可以为{1，1} 或 {0，1}

### 2. Fibonacci数列的迭代生成
`{0，1，1，2，3，5，8，13，21，...}`为斐波拉契数列，有很多非常好的性质。

特点：
- 首项为 0，1
- 通项公式为 $x_{n+2} = x_{n+1}+x_n, x_0=0, x_1=1, n \in N$
- 假设初始值为 f0,f1, 常规设置 f0=0, f1=1, 或者 f0=f1=1
- 迭代列表 fibonacci=`IterationList(a+b, a,b,{f0,f1},n)`, 其中 $n$ 为迭代次数，可以用滑块条定义 `n=Slider(5,30,1)`
- 斐波那契点列 `fp=Sequence((k, Element(fibonacci, k)), k, 1, Length(fibonacci))`
- 指数拟合上述点列，`指数拟合(fp)` `FitExp(fp)` | $h(x)=0.46 e^{0.48x}$
- 生长曲线拟合, `生长曲线拟合(fp)`  `FitGrowth(fp)` | $0.46 \cdot 1.62^x$

注意：由此可见，指数函数 $b^x$, 可以用 自然数指数函数代替 $e^{ax}$, 这里 $a=ln(b)$, 所以数学上讨论比较多的是 $e^x$ 函数， 可以模拟自然界很多自然现象，如人口模型。

![Fit Fibonacci Points](images\FitFibonacci.png)


## 如何制作一根弹簧？
弹簧可以看作空间螺线，投影到 $xOy$ 平面是一个圆，故可以通过圆的参数方程来完成。以下就是 圆柱螺线的参数方程表示：

- n = Slider(1,10,1)
- r = Slider(1,5,0.2)
- k = Slider(0,1,0.1)
- **c = Curve(r cos(t), r sin(t), k t, t, -2nπ, 2nπ)**

![弹簧实例](images\tanhuang.png)


## 优秀共享资源分享

1. [Thijs](https://www.geogebra.org/u/thijs): 3D Surfaces such as Klein Bottle, Crossing Twisted Rings, Nuzzle, Inverse Stereographic, Hohenwarter Delaunay, Escher Conformal Grid, Torus knot, Clifford Torus, Split Torus, Hilbert Curve, Times Tables, Butterfly Curve, Plant Growing, Arc Hex Fractal, Pythagoras Tree, Dragon Turtle, Blow up, Celtic pattern,etc
2. [Diego Lieban](https://www.geogebra.org/u/diegolieban): Books for 3D Printing, 4DFrame soccer ball,