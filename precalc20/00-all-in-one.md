# Set Theory 集合论

## Introduction

集合(*set*)可以放任何东西，比如说 *a set of two apples, a set of a table and a chair*，或者 *a set of all the numbers between 1 and 100*。集合可以是无限的，比如说 *a set of all the numbers*。集合可以是空的，比如说 *a set of nothing*。

## Set Notation and Set Builder Notation

### Set Notation 集合表示法

通常我们使用 Set Notation 来表示集合，比如说 `{苹果，梨}` ， `{1, 2, 3}`，或者 `{1, 2, 3, ..., 100}`。我们可以用 $\emptyset$ 来表示空集合。集合里的元素不能重复，比如说 `{1, 2, 3, 1}` 就不是一个集合。（我们称这种为 *multiset*，多重集合，也可以叫做 *bag*。）

### Set Builder Notation 集合生成法

当一个set中的元素都是由某个公式生成的时候，我们可以用 Set Builder Notation 来表示这个集合。比如说，我们可以用 $\{x \mid x \in \mathbb{N}\}$ 来表示所有自然数的集合。这里的 $\mathbb{N}$ 是自然数的集合，$\mathbb{N} = \{1, 2, 3, ...\}$。我们可以用 $\{x \mid x \in \mathbb{N}, x \leq 100\}$ 来表示所有小于等于100的自然数的集合

| 的左边是集合的元素，右边是集合的条件。我们可以用 $\{x \mid x \in \mathbb{N}, x \leq 100, x \text{ is even}\}$ 来表示所有小于等于100的自然数中的偶数的集合。$\{x^2 | x \in \mathbb{N}, x \leq 100\}$ 表示所有小于等于100的自然数的平方的集合 = {1, 4, 9, 16, 25, 36, 49, 64, 81, 100}。

### Membership and Subsets 成员关系和子集

当 x 属于集合 A 的时候，我们用 $x \in A$ 来表示这种关系, `x is a member of A` 或 `x in A`。当 x 不属于集合 A 的时候，我们用 $x \notin A$, `x not in A` 来表示。比如说，$1 \in \{1, 2, 3\}$，$1 \notin \{2, 3, 4\}$，$0.2 \notin \mathbb{Z}$

当集合B中的每一个元素都属于集合A的时候，我们用 $B \subseteq A$, `B is a subset of A` 来表示（B被包含在A中）。比如说，$\{1, 2, 3\} \subseteq \{1, 2, 3, 4\}$，$\{1, 2, 3\} \subseteq \{1, 2, 3\}$，空集合 $\emptyset$ 是所有集合的子集（每一个 set 都至少会包含 "空"）。如果集合中有一个元素不属于另一个集合，那么我们就说这个集合不是另一个集合的子集。比如说，$\{1, 2, 3\} \not\subseteq \{1, 2\}$，$\{1, 2, 3\} \not\subseteq \{1, 2, 4\}$。

因为一个集合的元素可以是任何东西，所以集合里面的元素也可以是一个数字、桌子、苹果、或者*另一个集合*。比如 $\{1, 2, 3, \{4, 5, 6\}\}$ 就是一个集合，它包含了 <u>**4**</u> 个元素：1, 2, 3, 和 $\{4, 5, 6\}$。

## Set Operations 集合运算

### Union 并集

已知集合 $A$ 和集合 $B$，并集 $A \cup B$ 是一个集合 `A union B`，它包含了所有属于 $A$ **或** $B$ 的元素。

比如
$$
\begin{align}
\{1, 2, 3\} \cup \{2, 3, 4\} &= \{1, 2, 3, 4\} \\
\{1, 2, 3\} \cup \{4, 5, 6\} &= \{1, 2, 3, 4, 5, 6\} \\
\{1, 2, 3\} \cup \{1, 2, 3\} &= \{1, 2, 3\} \\
\{1, 2, 3\} \cup \emptyset &= \{1, 2, 3\} \\
\emptyset \cup \emptyset &= \emptyset
\end{align}
$$

我们用 $\bigcup_{i=0}^n A_i = A_0 \cup A_1 \cup \cdots \cup A_n$ 来表示多个集合的并集。比如说，
$$
\begin{align}
\bigcup_{i=0}^3 \{i\} &= \{0\} \cup \{1\} \cup \{2\} \cup \{3\} = \{0, 1, 2, 3\} \\
\end{align}
$$

### Intersection 交集

已知集合 $A$ 和集合 $B$，交集 $A \cap B$ 是一个集合 `A intersection B`，它包含了所有属于 $A$ **且** $B$ 的元素。(*这个元素必须同时属于 $A$ **和** $B$*)

比如
$$
\begin{align}
\{1, 2, 3\} \cap \{2, 3, 4\} &= \{2, 3\} \\
\{1, 2, 3\} \cap \{4, 5, 6\} &= \emptyset \\
\{1, 2, 3\} \cap \{1, 2, 3\} &= \{1, 2, 3\} \\
\{1, 2, 3\} \cap \emptyset &= \emptyset \\
\emptyset \cap \emptyset &= \emptyset
\end{align}
$$

当然，我们也可以用 $\bigcap_{i=0}^n A_i = A_0 \cap A_1 \cap \cdots \cap A_n$ 来表示多个集合的交集。比如说，
$$
\begin{aligned}
\bigcap {\{1,2,3,4\}, {\{1, 4, 9, 16\}, {\{1, 8, 27, 64\}}} }\\
= \{1, 2, 3, 4\} \cap \{1, 4, 9, 16\} \cap \{1, 8, 27, 64\} \\
= \{1, 4\} \cap \{1, 8, 27, 64\} \\
= \{1\}
\end{aligned}
$$

### Difference 差集

已知集合 $A$ 和集合 $B$，差集 $A \setminus B$ 是一个集合 `A difference B`，它包含了所有属于 $A$ **但不属于** $B$ 的元素。

比如
$$
\begin{align}
\{1, 2, 3\} \setminus \{2, 3, 4\} &= \{1\} \\
\{1, 2, 3\} \setminus \{4, 5, 6\} &= \{1, 2, 3\} \\
\{1, 2, 3\} \setminus \{1, 2, 3\} &= \emptyset \\
\{1, 2, 3\} \setminus \emptyset &= \{1, 2, 3\} \\
\emptyset \setminus \emptyset &= \emptyset
\end{align}
$$

### Complement 补集

已知集合 $A$，补集 $\overline{A}$，也可以写作 $A^c$，是一个集合 `A complement`，它包含了所有不属于 $A$ 的元素。

### Power Set 幂集

已知集合 $A$，幂集 $P(A)$ 是一个集合 `power set of A`，它包含了所有 $A$ 的子集。

比如
$$
\begin{align}
P(\{1, 2, 3\}) &= \{\emptyset, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{1, 3\}, \{2, 3\}, \{1, 2, 3\}\} \\
P(\emptyset) &= \{\emptyset\}
\end{align}
$$

### Cartesian Product 笛卡尔积

已知集合 $A$ 和集合 $B$，笛卡尔积 $A \times B$ 是一个集合 `A cartesian product B`，它包含了所有 $A$ 中的元素和 $B$ 中的元素的组合。

比如
$$
\begin{align}
\{1, 2\} \times \{3, 4\} &= \{(1, 3), (1, 4), (2, 3), (2, 4)\} \\
\{1, 2\} \times \{2\} &= \{(1, 2), (2, 2)\} \\
\{1, 2\} \times \{k\} &= \{(1, k), (2, k)\} \\
\{1, 2\} \times \emptyset &= \emptyset \\
\emptyset \times \emptyset &= \emptyset
\end{align}
$$

## Size of Set 集合的大小

### Cardinality 基数

已知集合 $A$，基数 $|A|$ 是一个自然数 `cardinality of A`，它表示集合 $A$ 中元素的个数。

比如
$$
\begin{align}
| \{1, 2, 3\} | &= 3 \\
| \{1, 2, 3\} \setminus \{2, 3, 4\} | &= 1 \\
| \emptyset | &= 0
\end{align}
$$

空集 $\emptyset$ 的基数为 $0$。
一个集合的幂集的基数是 $2^{|A|}$。
比如：
$$
\begin{align}
|P(\{1, 2, 3\})| &= | \{\emptyset, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{1, 3\}, \{2, 3\}, \{1, 2, 3\}\} | \\
&= 8 \\
&= 2^3\\
|P(\emptyset)| &= | \{\emptyset\} | \\
&= 1 \\
&= 2^0
\end{align}
$$

一个集合的基数不一定是有限的，比如说，自然数集 $\mathbb{N}$ 的基数是无限的。

# Number Theory 数论

## Peano Axioms 佩诺公理

佩诺公理是数学中的基本公理，它定义了自然数的基本性质。

### Natural Numbers 自然数

自然数是一个集合，它包含了所有正整数和零。

我们用 $\mathbb{N}$ 表示自然数集合。
$\mathbb{N}$ = $\{0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, \ldots\}$

两个自然数的和也是一个自然数，比如 $1 + 2 = 3$。
两个自然数的乘积也是一个自然数，比如 $2 \times 3 = 6$。

### Integer 整数

整数是一个集合，它包含了所有自然数和它们的负数。

我们用 $\mathbb{Z}$ 表示整数集合。
$\mathbb{Z}$ = $\{\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots\}$

整数的和也是一个整数，比如 $-1 + 2 = 1$。
整数的乘积也是一个整数，比如 $-2 \times 3 = -6$。

### Rational Number 有理数

有理数是一个集合，它包含了所有整数和它们的分数。

我们用 $\mathbb{Q}$ 表示有理数集合。

$$
\mathbb{Q} = \{\frac{a}{b} | a \in \mathbb{Z}, b \in \mathbb{Z}, b \neq 0\}
$$

所有的有理数都可以用两个整数的比值来表示，比如 $\frac{1}{2}$, 0.8 = $\frac{8}{10}$。

当两个有理数进行**加**、**减**、**乘**、**除** 运算时，结果仍然是一个有理数。我们称这种集合为**有理数域** （rational field）。

### Irrational Number 无理数

在实数范围内，如果一个数不是有理数，那么它就是无理数。

我们用 $\mathbb{I}$ 表示无理数集合。

$$
\mathbb{I} = \mathbb{R} \setminus \mathbb{Q}
$$

常见的无理数有 $\pi = 3.1415926\ldots$, $e = 2.7182818\ldots$ 和 $\sqrt{2} = 1.4142135\ldots$。

### Real Number 实数

实数是一个集合，它包含了所有有理数和无理数。

我们用 $\mathbb{R}$ 表示实数集合。

$$
\mathbb{R} = \mathbb{Q} \cup \mathbb{I}
$$

两个实数进行**加**、**减**、**乘**、**除** 运算时，结果仍然是一个实数。我们称这种集合为**实数域** （real field）。

### Imaginary Number 虚数

虚数单位 $i$ 是一个数，它满足 $i^2 = -1$。

### Complex Number 复数

复数是一个集合，它包含了所有实数、虚数单位 $i$ 以及任意实数和虚数单位 $i$ 的和。

我们用 $\mathbb{C}$ 表示复数集合。

$$
\mathbb{C} = \mathbb{R} \cup \{i\} \cup \{\mathbb{R} + i\}
$$

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
