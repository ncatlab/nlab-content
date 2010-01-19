<div class="rightHandSide toc">
[[!include stable homotopy theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

If in the context of [[stable homotopy theory]] the [[topological space]]s and [[spectra]] are equipped with the [[action]] of a [[topological group]] $G$ the theory refines to a _$G$-equivariant_ version.

## Basic definitions

The definition of _$G$-spectrum_ is typically given in generalization of the definition of [[coordinate-free spectrum]].

A **$G$-universe** in this context is a infinite dimensional real [[inner product space]] equipped with a linear $G$-[[action]] that is the [[direct sum]] of countably many copies of a given [[set]] of [[representation]]s of $G$, at least containing the trivial representation on $\mathbb{R}$ (so that $U$ contains at least a copy of $\mathbb{R}^\infty$).

Each such subspace of $U$ is called an _indexing space_ . For $V \subset W$ indexing spaces, write $W-V$ for the orhtogonal complement of $V$ in $W$. Write $S^V$ for the [[one-point compactification]] of $V$ and for $X$ any (pointed) [[topological space]] write $\Omega^V := [S^V,X]$ for the corresponding (based) sphere space.

A **$G$-space** in the following means a [[pointed object|pointed]] [[topological space]] equipped with a continuous [[action]] of the [[topological group]] $G$ that fixes the base point. A  morphism of $G$-spaces is a continuous map that fixes the basepoints and is $G$-equivariant.

A weak equivalence of $G$-spaces is a morphism that induces isomorphism on all $H$-fixed homtopy groups (...)

A **$G$-spectrum** $E$ (indexed on the chosen universe $U$) is

* for each indesxing space $V \subset U$ a $G$-space $E V$;

* for each pair $V \subset W$ of indexing spaces a $G$-equivariant [[homeomorphism]]

  $$
    E V \stackrel{\simeq}{\to} \Omega^{W-V} E 
    \,.
  $$

A [[morphism]] $f : E \to E'$ of $G$-spectra is for each indexing space $V$ a morphism of $G$-spaces $f_V : E V \to E' V$, such that this makes the obvious diagrams commute.

This becomes a [[category with weak equivalences]] by setting:

a morphism $f$ of $G$-spectra is a **weak equivalence of $G$-spectra** if for every indexing space $V$ the component $f_V$ is a weak equivalence of $G$-spaces (as defined above).

This may be expressed directly in terms of the notion of **homotopy group of a $G$-spectrum**: this is ...



## References

* [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

