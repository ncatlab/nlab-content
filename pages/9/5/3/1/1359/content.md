

#Definition#

Let $C$ be a [[differential graded category]].

A **twisted complex** $E$ in $C$ is

* a graded set $\{E_i\}_{i \in \mathbb{Z}}$ of [[object]]s of $C$, such that only finitly many $E_i$ are not the [[zero object]];

* a set of [[morphism]]s $\{q_{i j} : E_i \to E_j \}_{i,j \in \mathbb{Z}}$ such that

  * $deg(q_{i j}) = i-j+1$;

  * $\forall i,j : \; d q_{i j} + \sum_{k} q_{k j}\circ q_{i k} = 0$.

The [[differential graded category]] $PreTr(C)$ of twisted complexes in $C$ has as objects twisted complexes and

$$
  PreTr(C)((E_\bullet, q), (E'_\bullet, q'))^k
  =
  \coprod_{l + j - i = k} C(E_i, E'_j)^l
$$

with differential given on $f \in C(E_i, E'_j)^l$ given by

$$
  d f = d_C f + \sum_m (q_{j m}\circ  f + (-1)^{l(i-m+1)} f \circ q_{m i})
  \,.
$$

The construction of categories of twisted complexes is functorial in that for $F : C \to C'$ a dg-functor, there is a dg-functor

$$
  PreTr(F) : PreTr(C) \to PreTr(C')
  \,.
$$

etc.

for more see [[pretriangulated dg-category]].