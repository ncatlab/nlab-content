
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


+-- {: .num_defn #NRing}
###### Definition

A _unital $\mathbb{N}$-ring_ is a [[ring]] such that 

1. the underlying [[abelian group]] is [[free abelian group]];

1. there exists a finite $\mathbb{N}$-[[basis]]: a [[finite set]] $I$ of elements $X_i \in R$, $i \in I$, such that 

   $$
     X_i X_j = \sum_{k \in I} c_{i j}^k X_k
   $$

   for $c_{i j}^k \in \mathbb{N}$

1. the ring unit 1 is among these basis elements.

=--

Let $\mathcal{C}$ be a [[fusion category]], i.e. a [[tensor category]] which is [[finite abelian category|finite]] and [[semisimple category]] (i.e. it has a [[finite number]] of [[isomorphism classes]] $[X_i]$ of [[simple objects]], all finite [[direct sums]] of these exist, and every object is isomorphic to such).

+-- {: .num_defn #FusionRing}
###### Definition

The [[isomorphism classes]] $[X]$ of objects of $\mathcal{C}$ form an $\mathbb{N}$-ring (def. \ref{NRing}) under [[tensor product]]. This is the _fusion ring_ of $\mathcal{C}$.

=--

## Related concepts

* [[Frobenius-Perron dimension]]

* [[Clebsch-Gordan coefficient]]

* [[Verlinde algebra]]

[[!redirects fusion rings]]
