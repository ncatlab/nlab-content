
# Idea #

The cup product on [[cohomology]] is an operation on cocycles with coefficients in $A$ induced from a pairing morphism

$$
  A_1 \times A_2 \to A_3
$$

If $g_1 : X \to A_1$ and $g_2 : X \to A_2$ are two cocycles in $\mathbf{H}(X,A_1)$ and $\mathbf{H}(X,A_2)$, respectively, then their cup product with respect to this pairing is the cocycle

$$
  g_1 \cdot g_2 : X \stackrel{Id \times Id}{\to}
  X \times X
  \stackrel{g_1 \times g_2}{\to}
  A_1 \times A_2
  \to
  A_3
$$

in $\mathbf{H}(X,A_3)$.

# In abelian sheaf cohomology #

Traditionally the cup product is considered for 
abelian cohomology, such as [[generalized (Eilenberg-Steenrod) cohomology]] and more generally [[abelian sheaf cohomology]].

In that case all coefficient objects $A_i$ are complexes $(A_i)_\bullet$ of sheaves and the pairing that one usually considers is the [[tensor product]] of [[chain complex]]es

$$
  (A_1)_\bullet \times (A_2)_\bullet \to (A_1 \otimes A_2)_\bullet
$$

where

$$
  (A_1 \otimes A_2)_n = \oplus_p (A_1)_p \otimes (A_2)_{n-p}
  \,.
$$

with differential 

$$
  d (a_1 \otimes a_2) = (d a_1) \otimes a_2 + (-1)^{|a_1|} a_1 \otimes d a_2
  \,.
$$

## In abelian Cech cohomology ##

The cup product has a simple expression in abelian [[Cech cohomology]].

For $\alpha \in C(U,A_1)_\bullet$ and $\beta \in C(U,A_2)_\bullet$ two Cech cocycles with respect to the same cover $\{U_i \to X\}$ of $X$, their cup product is simply the cocycle in $C(U, A_1 \otimes A_2)$ given by

$$
  (\alpha \cdot \beta)_{i_0, \cdots , i_{p + q}}
  \;:=\;
  \alpha_{i_0, \cdots, i_p} \otimes \beta_{i_p, \cdots i_{p+q}}
  \,.
$$