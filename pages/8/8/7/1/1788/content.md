We first consider the case of cohomology with coefficients in a sheaf of abelian groups. This is a special case of the construction below with coefficients in a chain complex of abelian sheaves.

Let

* $X$ be a [[topological space]]
* $A$ be an [[abelian sheaves]] on $X$.
* $\{U_i \to X\}$ be an [[open cover]] of $X$.

We write
$$
 U_{i_0,\cdots i_k} \coloneqq U_{i_0} \underset{X}{\times} U_{i_1} \underset{X}{\times} \cdots \underset{X}{\times} U_{i_k}
$$
for the $k$-fold intersection of these open subsets. Given an inclusion of open subsets $U_1 \to U_2$ and given any group element $a \in A(U_2)$, we write $a|_{U_1}$ for its restriction along this map.

+-- {: .num_defn}
###### Definition
**(&#268;ech complex)**

The **&#268;ech cochain complex** $C^\bullet((X,\{U_i\}),A)$ 
of $X$ with respect to the cover $\{U_i \to X\}$ and with [[coefficients]] in $A$ is in degree $k \in \mathbb{N}$ given by the [[abelian group]]
$$
  C^k((X,\{U_i\}),A)
  \coloneqq
  \bigoplus_{i_0, i_1, \cdots, i_k}
  A(U_{i_0, \cdots, i_k})
$$
=--

The [[differential]]
$$
 d \colon C^{k}((X,\{U_i\}),A) \longrightarrow C^{k+1}((X,\{U_i\}),A)
$$
is defined componentwise by
$$
  (da)_{i_0, ..., i_{k + 1}} \coloneqq (-1)^k \sum_{0 \leq j \leq k + 1} (-1)^j a_{i_0, ..., \bar{i_{j}}, ..., i_{k + 1}}|_{U_{i_0, ..., i_{k + 1}}}
$$