- [GeoGebra 应用案例](#geogebra-%e5%ba%94%e7%94%a8%e6%a1%88%e4%be%8b)
  - [分段函数](#%e5%88%86%e6%ae%b5%e5%87%bd%e6%95%b0)
  - [圆到椭圆方法](#%e5%9c%86%e5%88%b0%e6%a4%ad%e5%9c%86%e6%96%b9%e6%b3%95)
    - [伸缩变换：Stretch(圆，向量)](#%e4%bc%b8%e7%bc%a9%e5%8f%98%e6%8d%a2stretch%e5%9c%86%e5%90%91%e9%87%8f)
  - [牛顿迭代法 Newton's Iteration](#%e7%89%9b%e9%a1%bf%e8%bf%ad%e4%bb%a3%e6%b3%95-newtons-iteration)
    - [方法描述](#%e6%96%b9%e6%b3%95%e6%8f%8f%e8%bf%b0)
    - [GeoGebra中演示步骤](#geogebra%e4%b8%ad%e6%bc%94%e7%a4%ba%e6%ad%a5%e9%aa%a4)
    - [Cubic iteration 三次迭代](#cubic-iteration-%e4%b8%89%e6%ac%a1%e8%bf%ad%e4%bb%a3)
    - [举例 - 黄金分割比率 Golden Ratio](#%e4%b8%be%e4%be%8b---%e9%bb%84%e9%87%91%e5%88%86%e5%89%b2%e6%af%94%e7%8e%87-golden-ratio)

# GeoGebra 应用案例


## 分段函数

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

输入命令： $Stretch(circle, r \vec u), r$ 为伸缩比例。中文指令：`伸缩(d, r 向量(u))`， 此处 $\vec{u}=(1,0)$ 在 x 轴方向上缩放，如 $\vec{v}=(0,1)$, 则在 y 轴方向上缩放。

![伸缩变换-圆到椭圆](images\圆到椭圆.gif)


## 牛顿迭代法 Newton's Iteration

### 方法描述
Let $f: \Reals \to \Reals, x \mapsto f(x)$ be a differentiable function where $f'(x) \neq 0$ for all $x$ and $x_0$ be an initial (not necessarily good) guess for $f(x)=0$ then the recursive application of  
$$x_{n+1}=x_n-\dfrac{f(x_n)}{f'(x_n)}   \qquad  (1)$$
yields a better approximation for a zero crossing.

主要用来解决方程 $f(x)=0$ 的精确求根，假设 $f(x)$ 是给定区间的 $C^2 \; Function$ 函数，即两阶连续函数，根据Taylor展开得到x附近的展开式：

$$f(x+\delta)=f(x)+\delta f'(x)+O(\delta ^2)$$

当 $\delta$ 很小时，有 $f(x+\delta) =0 \approx f(x)+\delta f'(x)$

$$\delta=-\dfrac{f(x)}{f'(x)} \\[2ex]
x+\delta = x-\dfrac{f(x)}{f'(x)}$$

从而 Newton 迭代就是寻找 $(1)$式中的数列 $\{x_n\}$的极限值。

注意：上述迭代方法，在很多情况下不收敛(not converge,we say chaotic sometimes)，即极限不存在。

### GeoGebra中演示步骤
1. 建立函数 `f: x^2-ln(x)-2`
2. 根据牛顿迭代法，求出迭代函数 `g: x - f(x)/f'(x)`
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

