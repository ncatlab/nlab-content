
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given a [[well-generated triangular category|well-generated]] [[monoidal category|tensor]] [[triangulated category]] $(T,\otimes, 1)$, let the _Bousfield class_ of an object $X$, denoted $\langle X\rangle$, be the class $\{ Y\in obj(T): X\otimes Y=0\}$.  It was proven by Ohkawa that if $T$ is the [[stable homotopy category]], $(\mathcal{S},\wedge,S)$, then the collection of all Bousfield classes is a [[set]] of [[cardinality]] at most $\beth_2$.  It was proven more generally by Iyengar and Krause that such a collection is always a set and not a [[proper class]] when $T$ is well-generated. This set has a partial ordering on it and the structure of a complete lattice. This lattice is called the _Bousfield lattice_ of $T$, denoted $B_T$. 

Note that, perhaps by some abuse of notation, $B_T\subseteq\mathbf{Loc}(T)$, the collection of [[localizing subcategories]], since every Bousfield class is a localizing subcategory. However, the question of whether or not every localizing subcategory is a Bousfield class is still open in general.

## The Distributive Lattice of the Bousfield Lattice

Within $B_T$, there is a [[distributive lattice]] $DL_T$ that is precisely all _Bousfield idempotent_ objects of $T$.  That is, $DL_T$ is precisely the objects $X$ such that $\langle X\otimes X\rangle=\langle X\rangle$.  Because $B_T$ is an affine [[quantale]], it follows that $DL_T$ is a [[frame]].  In particular, $DL_T$ is a [[distributive lattice]], so by the work of Stone, it corresponds to a coherent space.  For more on this, see [[Stone duality]].




##References

* S. B. Iyengar and H. Krause, _The Bousfield Lattice of a Triangulated Category and Stratification_ ([arXiv:1105.1799](http://arxiv.org/abs/1105.1799))

[[!redirects Bousfield Lattice]]
[[!redirects bousfield lattice]]
