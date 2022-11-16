\tableofcontents

## Definition

The functor $\mathcal{O}:OLoc^\op \to Frm$ from the [[opposite category]] of [[overt locales]] to the [[category]] of [[frames]] is a [[regular hyperdoctrine]]. This means that it has an [[internal logic]], where given an overt locale $L$, we can define the composition of open relations $E, F \in \mathcal{O}(L \times L)$ as

$$F \circ E \coloneqq \{(x, z):L \times L \vert \exists y:L.(x, y) \in E \wedge (y, z) \in F\}$$

A **preuniform locale** is a [[overt locale]] $L$ equipped with a [[filter]] $\mathcal{E}$ on the frame of opens $\mathcal{O}(L \times L)$ such that for each $E \in \mathcal{E}$, 

* $(x, x) \in E$

* there exists an $E^o \in \mathcal{E}$ such that $(x, y) \in E$ entails and is entailed by $(y, x) \in E^o$ 

* there exists an $F \in \mathcal{E}$ such that $F \circ F \leq E$

## See also

* [[locale]]

* [[overt locale]]

* [[preuniform locale]], [[uniform locale]]

* [[premetric locale]], [[metric locale]]

## References

* Graham Manuell, *Uniform locales and their constructive aspects*, ([arXiv:2106.00678](https://arxiv.org/abs/2106.00678))