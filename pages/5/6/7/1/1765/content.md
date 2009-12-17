
## Definition

Let $f : R\to S$ be the extension of $k$-[[algebra]]s (where $k$ is a commutative unital [[ring]]). 

The corresponding __canonical coring__ or __Sweedler coring__ is the $R$-[[coring]] 

$$
  C = S\otimes_R S
$$ 

with coproduct 

$$
  \Delta : C\to C\otimes_R C \cong S\otimes_R S\otimes_R S
$$ 

given by

$$
  \Delta: s_1\otimes s_2 \mapsto s_1\otimes 1 \otimes s_2
$$ 

and counit 

$$
  \epsilon : C\to R
$$ 

given by 

$$
 \epsilon: s_1 \otimes s_2 \mapsto s_1 s_2
 \,.
$$  

## Relation to descent

The category of [[descent]] data $\mathrm{Desc}(S/R)$ for the categories of right modules along $k$-algebra extension $R\to S$ can be expressed solely in terms of the canonical coring $(C,\Delta,\epsilon)$ as the category of right $C$-[[comodule]]s.

In other words, the objects of $\mathrm{Desc}(S/R)$ are the pairs $(M,\alpha)$ where $M$ is a right $S$-module, and $\alpha: M\to M\otimes_R S$ is a right $A$-module morphism and if we write $\alpha(m) = \sum_i m_i \otimes s_i$ then

* $\sum_i \alpha(m_i)\otimes s_i = \sum_i m_i\otimes 1\otimes s_i$,

* $\sum_i m_i s_i = m$.

## Relation to ring extensions

Various properties of canonical coring correspond to adequate properties of the ring extension. For example, [[coseparable coring|coseparable]] Sweedler corings correspond to [[split extension]]s (the $k$-algebra extension $R\to S$ is split if there is an $R$-bimodule map $h: S\to R$ with $h(1_S) = 1_R$).
