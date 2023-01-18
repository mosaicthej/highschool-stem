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
