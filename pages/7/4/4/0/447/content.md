Let $S$ be one of the categories of [[geometric shapes for higher structures]], such as the [[globe category]] or the [[simplex category]] or the [[cube category]].

There is an obvious functor

 $ st : S \to $ [[Top]]

which sends the standard _cellular_ shape $[n]$ (the standard cellular [[globe]], [[simplex]] or [[cube]], respectively) to the corresponding standard _topological_ shape (for instance  the standard $n$-simplex $ st([n]) := \{ (x_1, \cdots, x_n) | x_i \leq x_{i+1}  \} \subset \mathbb{R}^{n}$ ) with the obvious induced face and boundary maps.

Using this, the **geometric realization** of a [[presheaf]] $K^\bullet : S^{op} \to V$ on $S$ for [[Top]] [[power]]ed over $V$ -- i.e. of a [[globular set]], a [[simplicial set]] or a [[cubical set]], respectively  (when $V= Set$) -- is the [[topological space]] given by the [[end|coend]]

$$
  |K^\bullet| = \int^{[n] \in S} st([n]) \cdot K^n
  \,.
$$