
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential-graded objects
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

## Definition

Let $G$ be an [[abelian group]]. Often one takes by default $G = \mathbb{Z}$ the additive group of [[integer]]s.

A **graded ring** is a [[ring]] $R$ equipped with a decomposition of the underlying [[abelian group]] as a [[direct sum]] $R = \oplus_{g \in G} R_g$ such that the product takes $R_{g} \times R_{g'} \to R_{g g'}$.

Analogously there is the notion of graded $k$-[[associative algebra]] over any commutative ring $k$.

Specifically for $k$ a [[field]] a **graded algebra** is a [[monoid]] internal to [[graded vector space]]s.

A [[differential graded algebra]] is a graded algebra $A$ equipped with a [[derivation]] $d : A\to A$ of degree +1 (or -1, dependig on conventions) and such that $d \circ d = 0$. This is the same as a [[monoid]] in the category of [[chain complex]]es.


## Properties


+-- {: .un_prop}
###### Proposition

For $R$ a commutative ring write $Spec R \in Ring^{op}$ for the corresponding object in the [[opposite category]]. Write $\mathbb{G}_m$ for the multiplicative group underlying the [[affine line]]. 

There is a [[natural isomorphism]] between

* $\mathbb{Z}$-gradings on $R$;

* $\mathbb{G}_m$-[[action]]s on $Spec R$.

=--

The proof is speled out at [[affine line]] in the section <a href="http://nlab.mathforge.org/nlab/show/affine+line#Properties">Properties</a>.

[[!redirects graded algebras]]

[[!redirects graded ring]]
[[!redirects graded rings]]