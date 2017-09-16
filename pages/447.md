# Idea #

_Geometric_ realization denotes usually the special case of [[nerve and realization]] induced from the standard [[simplicial set|cosimplicial]] topological space that in degree $n$ is the standard topological $n$-simplex $\Delta^n_{Top}$.

In this case geometric realization is the operation that reads in a [[simplicial set]] $X$ and spits out the [[topological space]] that is obtained by interpreting each 
element in $X_n$ -- each abstract $n$-simplex in $X$ -- as one copy of $\Delta^n_{Top}$ and then guing together all these along their boundaries to a big topological space, using the information encoded in the face and degeneracy maps of $X$ on how these simplices are supposed to be stuck together.

# Details #

Let $S$ be one of the categories of [[geometric shapes for higher structures]], such as the [[globe category]] or the [[simplex category]] or the [[cube category]].

There is an obvious functor

 $ st : S \to $ [[Top]]

which sends the standard _cellular_ shape $[n]$ (the standard cellular [[globe]], [[simplex]] or [[cube]], respectively) to the corresponding standard _topological_ shape (for instance  the standard $n$-simplex $ st([n]) := \{ (x_1, \cdots, x_n) | x_i \leq x_{i+1}  \} \subset \mathbb{R}^{n}$ ) with the obvious induced face and boundary maps.

Using this, in cases where $Top$ can be regarded as [[enriched category|enriched]] over and [[copower|tensored]] over a base category $V$, the **geometric realization** of a [[presheaf]] $K^\bullet : S^{op} \to V$ on $S$ -- e.g., of a [[globular set]], a [[simplicial set]] or a [[cubical set]], respectively  (when $V= Set$) -- is the [[topological space]] given by the [[end|coend]] or [[weighted limit|weighted colimit]]

$$
  |K^\bullet| = \int^{[n] \in S} st([n]) \cdot K^n
  \,.
$$

# Examples #

* For $G$ a [[group]], $\mathbf{B}G$ its one-object [[groupoid]] obtained by [[delooping]], $N(\mathbf{B}G)$ the corresponding simplicial [[nerve]] [[Kan complex]], we have that the geometric realization
  $$
    \mathcal{B}G = |N\mathbf{B}G|
  $$
  is the [[topological space]] that is the [[classifying space]] for $G$-[[principal bundle]]s ([[cover space]]s), as long as we give $G$ the [[discrete topology]].