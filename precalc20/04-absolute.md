# Absolute Value 绝对值

## Absolute Value Definition 绝对值定义

绝对值是一个把实数映射到非负实数的函数。

$$
abs: \mathbb{R} \rightarrow \mathbb{R_{\geq0}}\\
abs(x) = \begin{cases}
x & x \geq 0 \\
-x & x < 0
\end{cases}
$$

通常我们用 $|x|$ 来表示绝对值。
$$
|x| = \begin{cases}
x & x \geq 0 \\
-x & x < 0
\end{cases}
$$

我们也可以使用根号平方的方式来表示绝对值。
$$
|x| = \sqrt{x^2}
$$

绝对值永远是非负的。

$$
|x| \geq 0
$$

## Absoulte Value, Number Line and Distance 绝对值，数轴和距离

如果把一个实数 $x$ 画在数轴上，那么它的绝对值 $|x|$ 就是 $x$ 到原点($0$)的距离。

![abs](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f1/AbsoluteValueDiagram.svg/220px-AbsoluteValueDiagram.svg.png)

对于任意两个实数 $x$ 和 $y$，它们的绝对值之差 $|x - y|$ 就是 $x$ 和 $y$ 之间的距离。比如

$$
|-3 - 5| = |-8| = 8
$$

## Calculation and Order 计算和排序

计算一个带绝对值的式子的时候，比如 $|-3 + 2| + 5$，我们可以先计算绝对值里面的部分，然后再计算绝对值外面的部分。

$$
\begin{align}
|-3 + 2| + 5&= |-1| + 5\\
&= 1 + 5\\
&= 6
\end{align}
$$

当比较两个带绝对值的式子的大小的时候，先计算出这个式子的值，然后再比较这个值的大小。

例如下列式子
|绝对值式子|值|
|:-:|:-:|
|$\|-3 + 2\| + 5$|$6$|
|$\|-2 + 1\| + -3$|$-2$|

### Product Quotient Rule 乘除法规则

$$
\begin{align}
|a| \cdot |b| &= |ab|\\
|a| \div |b| &= |\frac{a}{b}|
\end{align}
$$


## Piecewise Function 分段函数

分段函数是把一个函数分成几个区间，然后在每个区间里面定义一个函数。例如

$$
f(x) = \begin{cases}
x & x \geq 0 \\
-x & x < 0
\end{cases}
$$

给一个绝对值，要求用 piecewise function (分段函数) 来表示它。例如

$$
|x+3| = \begin{cases}
x+3 & x \geq -3 \\
-(x+3) & x \lt -3
\end{cases}
$$

$$
|2x+5|-3 = \begin{cases}
2x+2 & x \geq -2.5 \\
-2x-8 & x \lt -2.5
\end{cases}
$$
计算时，先计算绝对值里面的部分，找到使绝对值内值为 0 的点，然后再计算绝对值外面的部分。

$$
\begin{align}
|2x+5|-3 \\
\end{align}
$$
首先寻找使 $2x+5 =0$ 的点，即 $x=-2.5$

那么这个 $x=2.5$ 就是分段函数的分界点，使用分段函数重写这个式子，得到:
$$
\begin{align}
|2x+5|-3 = \begin{cases}
(2x+5)-3 & x \geq -2.5 \\
-(2x+5)+3 & x \lt -2.5
\end{cases} \\
\end{align}
$$
化简，得到
$$
\begin{align}
|2x+5|-3 = \begin{cases}
2x+2 & x \geq -2.5 \\
-2x-8 & x \lt -2.5
\end{cases}
\end{align}
$$
