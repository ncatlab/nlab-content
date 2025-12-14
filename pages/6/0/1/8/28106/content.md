+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Pontrjagin numbers_ are [[integer]] [[topological invariants]] for real [[vector bundles]] over [[orientable]] [[smooth manifolds]], which are computed from their [[Pontrjagin classes]]. In particular, they exist for [[orientable]] [[smooth manifolds]] when considering their [[tangent bundle]]. According to the Pontrjagin-Thom theorem, two orientable smooth manifolds are orientable bordant if and only if all their [[Stiefel-Whitney numbers]] and Pontrjagin numbers are identical.

## Definition

Let $E\twoheadrightarrow M$ be a real [[vector bundle]] over a $4n$-dimensional [[orientable]] [[smooth manifold]] $M$ with a [[fundamental class]] $[M]\in H_{4n}(M,\mathbb{Z})\cong\mathbb{Z}$ and $i_1+\ldots+i_r=n$ be a partition. Using the [[Kronecker pairing]] and the [[cup product]], the _Pontrjagin number_ of $E$ corresponding to this partition is given by:
$$
p_{i_1}\ldots p_{i_r}[E]
\coloneqq\langle p_{i_1}(E)\smile\ldots\smile p_{i_r}(E),[M]\rangle
\in\mathbb{Z}.
$$
Pontrjagin numbers are usually considered for its [[tangent bundle]] with the short notation $p_{i_1}\ldots p_{i_r}[M]\coloneqq p_{i_1}\ldots p_{i_r}[TM]$.

([Milnor & Stasheff 74, p. 185](#MilnorStasheff74)) 

## Examples

The Pontrjagin numbers of the [[complex projective space]] $\mathbb{C}P^{2n}$ (whose underlying real manifold is $4n$-dimensional) are given by:
$$
p_{i_1}\ldots p_{i_r}[\mathbb{C}P^{2n}]
=\binom{2n+1}{i_1}\ldots\binom{2n+1}{i_r}.
$$

([Milnor & Stasheff 74, p. 185](#MilnorStasheff74)) 

## Related concepts

* [[Stiefel-Whitney number]]
* [[Chern number]]

## References

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf)) 

[[!redirects Pontrjagin numbers]]
[[!redirects Pontryagin number]] 
[[!redirects Pontryagin numbers]]
