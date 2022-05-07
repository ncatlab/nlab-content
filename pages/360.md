
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

A _graded algebra_ is an [[associative algebra]] which is with a labelling on its elements by elements of some [[monoid]] or [[group]], and such that the multiplication in the algebra is reflected in the multiplication in the labelling group. 

## Definition

Let $G$ be a [[group]].  (Often $G$ will be abelian, and, in fact, one usually takes by default $G = \mathbb{Z}$ the additive group of [[integers]], in which case the actual group being used is omitted from the terminology and notation.)

A **graded ring** is a [[ring]] $R$ equipped with a decomposition of the underlying [[abelian group]] as a [[direct sum]] $R = \oplus_{g \in G} R_g$ such that the product takes $R_{g} \times R_{g'} \to R_{g g'}$.

Analogously there is the notion of graded $k$-[[associative algebra]] over any commutative ring $k$.

Specifically for $k$ a [[field]] a **graded algebra** is a [[monoid in a monoidal category|monoid in]] [[graded vector spaces]] over $k$.

An $\mathbb{N}$-graded algebra is called _connected_ if in degree-0 it is just the ground ring.

A [[differential graded algebra]] is a graded algebra $A$ equipped with a [[derivation]] $d : A\to A$ of degree +1 (or -1, depending on conventions) and such that $d \circ d = 0$. This is the same as a [[monoid]] in the category of [[chain complexes]].


## Properties


+-- {: .un_prop}
###### Proposition

For $R$ a commutative ring write $Spec R \in Ring^{op}$ for the corresponding object in the [[opposite category]]. Write $\mathbb{G}_m$ for the multiplicative group underlying the [[affine line]]. 

There is a [[natural isomorphism]] between

* $\mathbb{Z}$-gradings on $R$;

* $\mathbb{G}_m$-[[action]]s on $Spec R$.

=--

The proof is spelled out at [[affine line]] in the section <a href="http://nlab.mathforge.org/nlab/show/affine+line#Properties">Properties</a>.

## Examples 


### Group ring

Let $G$ be any (discrete) group and $k[G]$, its [[group algebra]]. This has a direct sum decomposition as a $k$-module,

$$k[G] = \bigoplus_{g\in G}L_g$$

where each $L_g$ is a one dimensional free $k$-module, for which it is convenient, here, to give a basis $\{\ell_g\}$.  The graded algebra structure is obtained by extending the multiplication rule,

$$\ell_{g_1}\cdot \ell_{g_2} = \ell_{g_1g_2},$$

given on basis elements, by $k$-linearity.

### Lazard ring

The [[Lazard ring]], carrying the universal (1-dimensional, commutative) [[formal group law]] is naturally an $\mathbb{N}$-graded ring.

## References

Textbook account:

* {#Karpilovsky87} [[Gregory Karpilovsky]], Chapter 2 of: *The Algebraic Structure of Crossed Products*, Mathematics Studies **142**, North Holland 1987 ([ISBN:9780080872537](https://www.elsevier.com/books/the-algebraic-structure-of-crossed-products/karpilovsky/978-0-444-70239-5))


For [[Hopf algebras]]:

* Ken Brown, Paul Gilmartin, James J. Zhang, _Connected (graded) Hopf algebras_ ([arXiv:1601.06687](http://arxiv.org/abs/1601.06687))

[[!redirects graded algebras]]

[[!redirects graded ring]]
[[!redirects graded rings]]

[[!redirects connected graded algebra]]
[[!redirects connected graded algebras]]