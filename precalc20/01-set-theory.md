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
