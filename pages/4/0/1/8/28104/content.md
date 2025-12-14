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

_Stiefel-Whitney numbers_ are binary [[topological invariants]] for real [[vector bundles]] over [[smooth manifolds]], which are computed from their [[Stiefel-Whitney classes]]. In particular, they exist for [[smooth manifolds]] when considering their [[tangent bundle]]. According to the Pontrjagin-Thom theorem, two smooth manifolds are bordant if and only if all their Stiefel-Whitney numbers are identical. Two orientable smooth 5-manifolds are furthermore bordant if and only if their respective de Rham invariant, a particular Stiefel-Whitney number, is identical.

## Definition

Let $E\twoheadrightarrow M$ be a real [[vector bundle]] over a $n$-dimensional manifold $M$ with a unique [[fundamental class]] $[M]\in H_n(M,\mathbb{Z}_2)\cong\mathbb{Z}_2$ and $i_1+\ldots+i_r=n$ be a partition. Using the [[Kronecker pairing]] and the [[cup product]], the _Stiefel-Whitney number_ of $E$ corresponding to this partition is given by:
$$
w_{i_1}\ldots w_{i_r}[E]
\coloneqq\langle w_{i_1}(E)\smile\ldots\smile w_{i_r}(E),[M]\rangle
\in\mathbb{Z}_2.
$$
Stiefel-Whitney numbers are usually considered for its [[tangent bundle]] with the short notation $w_{i_1}\ldots w_{i_r}[M]\coloneqq w_{i_1}\ldots w_{i_r}[TM]$.

([Milnor & Stasheff 74, p. 51](#MilnorStasheff74)) 

## Properties

\begin{proposition}
All Stiefel-Whitney numbers of a [[3-manifold]] vanish.
\end{proposition}

([Milnor & Stasheff 74, Problem 11-D](#MilnorStasheff74))

\begin{theorem}
(**Pontrjagin theorem**)
All Stiefel-Whitney numbers of the boundary of a compact smooth manifold vanish.
\end{theorem}

([Milnor & Stasheff 74, Thrm. 4.9](#MilnorStasheff74)) 

\begin{theorem}
(**Thom theorem**)
If all Stiefel-Whitney numbers of a smooth manifold vanish, it is the boundary of a compact smooth manifold.
\end{theorem}

([Milnor & Stasheff 74, Thrm. 4.10](#MilnorStasheff74))

## Stiefel-Whitney numbers of a 4-manifold

A [[4-manifold]] $M$ has five Stiefel-Whitney numbers, which are $w_1^4[M]$, $w_1^2w_2[M]$, $w_1w_3[M]$, $w_2^2[M]$ and $w_4[M]$. If $M$ is orientable, if and only if $w_1(M)=0$, then the former three vanish automatically. 

## Stiefel-Whitney numbers of a 5-manifold

A [[5-manifold]] $M$ has seven Stiefel-Whitney numbers, which are $w_1^5[M]$, $w_1^3w_2[M]$, $w_1^2w_3[M]$, $w_1w_2^2[M]$, $w_1w_4[M]$, $w_2w_3[M]$ and $w_5[M]$. According to the upper properties, the last always vanishes. If $M$ is orientable, if and only if $w_1(M)=0$, then the former five vanish additionally. In this case, only the Stiefel-Whitney number $w_2w_3[M]$ can potentially be non-trivial and due to this special role, it is called de Rham-invariant.

## Examples

The Stiefel-Whitney numbers of the [[real projective space]] $\mathbb{R}P^n$ are given by:
$$
w_{i_1}\ldots w_{i_r}[\mathbb{R}P^n]
=\binom{n+1}{i_1}\ldots\binom{n+1}{i_r}\mod 2.
$$ 

## Related concepts

* [[Chern number]]
* [[Pontrjagin number]]

## References

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))

[[!redirects Stiefel-Whitney numbers]] 
[[!redirects SW number]]
[[!redirects SW numbers]]