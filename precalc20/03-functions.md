# Functions 函数

## Function Definition 函数定义

函数是一个数学概念，它将一个集合中的元素映射（map）到另一个集合中的元素的关系（relation）。

函数有两部分，输入和输出。来自 Domain 的输入 x 经过函数 f 转换后得到输出 y，我们用 $y = f(x)$ 来表示。

### Domain of a Function 函数的定义域

函数的定义域是一个集合，它包含了所有函数的输入。

### Codomain of a Function 函数的陪域

函数的陪域是一个集合，它包含了所有**可能的**函数的输出。

### Range of a Function 函数的值域

函数的值域是一个集合，它包含了所有**实际的**函数的输出。

如果用 C 表示函数的codomain，用 R 表示函数的range，那么 R ⊆ C。

### Function Notation 函数表示法

我们用 $f(x)$ 表示函数 $f$ 的值，其中 $x$ 是函数 $f$ 的输入。

如果用 $D$ 表示函数 $f$ 的定义域，用 $C$ 表示函数 $f$ 的陪域：

$$
f: D \rightarrow C
$$

一个函数的输入必须只有一个对应的输出，但是一个输出可以对应多个输入。

例如下图所示的关系

![func](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Injection_keine_Injektion_2a.svg/220px-Injection_keine_Injektion_2a.svg.png)

这个关系的 *Domain* 是 $\{1, 2, 3\}$，*Codomain* 是 $\{A, B, C, D\}$。这段关系的定义规则是：

$$
\begin{align}\begin{cases}
1 &\rightarrow D \\
2 &\rightarrow C \\
3 &\rightarrow C \\
\end{cases}\end{align}
$$

那么这个关系的 *Range* 是 $\{C, D\}$。

这段关系是一个函数，因为对于任何一个输入，它只有一个输出。

它的输出 $C$ 对应了两个输入 $2$ 和 $3$，所以它不是一个单射（injective）函数。

下面这个关系：

![non-func](https://upload.wikimedia.org/wikipedia/commons/thumb/b/bd/Injection_keine_Injektion_1.svg/220px-Injection_keine_Injektion_1.svg.png)

它的 *Domain* 是 $\{1, 2, 3, 4\}$，*Codomain* 是 $\{A, B, C, D\}$。这段关系的定义规则是：

$$
\begin{align}
1 &\rightarrow D \\
2 &\rightarrow B \\
2 &\rightarrow C \\
\end{align}
$$

这个关系不是一个函数，因为它的输出 $2$ 对应了两个输入 $B$ 和 $C$。
