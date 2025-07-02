
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
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

Let $M$ be a [[monoid]].  (Often $M$ will be an abelian group, and often by default $M = \mathbb{Z}$, the additive group of [[integers]].  However, another common choice is $M = \mathbb{N}$, the additive monoid of [[natural numbers]].)

An **$M$-graded ring** or simply a **graded ring** is a [[ring]] $R$ equipped with a decomposition of the underlying [[abelian group]] as a [[direct sum]] $R = \oplus_{m \in M} R_m$ such that the product maps $R_{m} \times R_{m'}$ to $R_{m m'}$.

Analogously there is the notion of graded [[associative algebra]] over any field $k$.  We can express it as follows: an **$M$-graded algebra** or simply **graded algebra** is a [[monoid in a monoidal category]] of $M$-[[graded vector spaces]] over $k$. 

Both graded rings and graded algebras over a field are, in turn, special cases of graded algebras over a commutative ring.

An $\mathbb{N}$-graded ring is often called a **nonnegatively graded ring**.   An $\mathbb{N}$-graded ring is called _connected_ if in degree zero it is just the ground ring.

A *[[differential graded algebra]]* is a graded algebra $A$ equipped with a [[derivation]] $d : A\to A$ of degree +1 (or -1, depending on conventions) and such that $d \circ d = 0$. This is the same as a [[monoid]] in the category of [[chain complexes]].

{#StronglyGraded} A $\mathbb{N}$-graded algebra is called **strongly $\mathbb{N}$-graded** (in [Ardizzoni & Menini (2007), Def. 3.2](#ArdizzoniMenini07)) if for every $n,p \ge 0$, the [[multiplication]] $A_{n} \otimes A_{p} \rightarrow A_{n+p}$ is an [[epimorphism]].



## Properties


+-- {: .un_prop}
###### Proposition

For $R$ a commutative ring write $Spec R \in Ring^{op}$ for the corresponding object in the [[opposite category]]. Write $\mathbb{G}_m$ for the multiplicative group underlying the [[affine line]]. 

There is a [[natural isomorphism]] between

* $\mathbb{Z}$-gradings on $R$;

* $\mathbb{G}_m$-[[action]]s on $Spec R$.

=--

The proof is spelled out at [[affine line]] in the section *[Properties](affine+line#Properties)*.



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

The notion of strongly $\mathbb{N}$-graded algebra is defined in:

* {#ArdizzoniMenini07} Alessandro Ardizzoni, Claudia Menini, _Associated graded algebras and coalgebras_ ([arXiv:0704.2106](https://arxiv.org/abs/0704.2106))

[[!redirects graded algebras]]

[[!redirects graded ring]]
[[!redirects graded rings]]

[[!redirects connected graded algebra]]
[[!redirects connected graded algebras]]