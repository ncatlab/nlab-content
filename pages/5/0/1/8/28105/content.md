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

_Chern numbers_ are [[integer]] [[topological invariants]] for complex [[vector bundles]] over [[orientable]] [[smooth manifolds]], which are computed from their [[Chern classes]]. In particular, they exist for [[complex manifolds]] (which are always [[orientable]]) when considering their [[tangent bundle]]. An important Chern number is the [[Seiberg-Witten invariant]].

## Definition

Let $E\twoheadrightarrow M$ be a complex [[vector bundle]] over a $2n$-dimensional [[orientable]] [[smooth manifold]] $M$ with a [[fundamental class]] $[M]\in H_n(M,\mathbb{Z})\cong\mathbb{Z}$ and $i_1+\ldots+i_r=n$ be a partition. Using the [[Kronecker pairing]] and the [[cup product]], the _Chern number_ of $E$ corresponding to this partition is given by:
$$
c_{i_1}\ldots c_{i_r}[E]
\coloneqq\langle c_{i_1}(E)\smile\ldots\smile c_{i_r}(E),[M]\rangle
\in\mathbb{Z}.
$$
Chern numbers are usually considered for [[tangent bundles]] of [[complex manifolds]] with the short notation $c_{i_1}\ldots c_{i_r}[M]\coloneqq c_{i_1}\ldots c_{i_r}[TM]$.

([Milnor & Stasheff 74, p. 184](#MilnorStasheff74)) 

## Examples

The Chern numbers of the [[complex projective space]] $\mathbb{C}P^n$ are given by:
$$
c_{i_1}\ldots c_{i_r}[\mathbb{C}P^n]
=\binom{n+1}{i_1}\ldots\binom{n+1}{i_r}.
$$

([Milnor & Stasheff 74, p. 184](#MilnorStasheff74))  

## Related concepts

* [[Stiefel-Whitney number]]
* [[Pontrjagin number]]

## References

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf)) 

[[!redirects Chern numbers]] 