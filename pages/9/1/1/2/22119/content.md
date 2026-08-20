## Idea

Given a $C$-coalgebra-Galois extension $U\hookrightarrow E$ of a $k$-algebra $U$, which is the appropriate generalization of a [[Hopf-Galois extension]], where $E$ is faithfully flat over the base $U$ as a left $E$-module, one constructs a coring, __Ehresmann coring__, out of these data. Its role is somewhat analogous to the gauge groupoid (see [[Atiyah Lie groupoid]]), and in Hopf-Galois case it is an intermediate stage in constructing another analogue, (Ehresmann-)[[Schauenburg bialgebroid]], see there.

## Definition

A right __$C$-coalgebra-Galois extension__ $U\hookrightarrow E$ is a $k$-algebra $E$ together with a right $C$-coaction $\rho:E\to E\otimes C$ where $U = \{ u\in E| \rho(u e) = (u\otimes 1)\rho(e),\forall e\in E\}$ is the subalgebra of coinvariants if the map
$$
can : E\otimes_U E\to E\otimes C,\,\,\,\,\,\,e\otimes e'\mapsto (e\otimes 1)\rho(e')
$$
is bijective. The map $\tau:C\to E\otimes E$, $c\mapsto can^{-1}(1\otimes c)$ is the __translation map__:

The underlying bimodule of the Ehresmann coring $D$ is the subbimodule $B\subset E\otimes_k E$
$$
B = \{\sum_i e_i\otimes e'_i \in E\otimes_k E |
\sum_i e_i \otimes e'_i\otimes_U 1 = \sum_i e_{i(0)}\otimes \tau(e_{i(1)}) e'_i
\in E\otimes_k (E\otimes_U E)
\}
$$
If $E$ is faithfully flat as a left $U$-module then $B$ is a $U$-coring via

$$
\Delta_B : \sum_i e_i\otimes e'_i \mapsto \sum_i
e_{i(0)}\otimes\tau(e_{i(1)})\otimes e'
$$
and comultiplication given by multiplication:
$\epsilon_B(\sum_i e_i\otimes e'_i) = \sum_i e_i\cdot_E e'_i$.

## Literature

* [[T. Brzeziński]], R. Wisbauer, _Corings and comodules_, London Math. Soc. Lec. Note Series __309__, Cambridge 2003.