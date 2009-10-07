<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>



#Contents#

* automatic table of contents
{:toc}

#Idea#

A _smooth locus_ is the [[duality|formal dual]] of a finitely generated [[smooth algebra]] (or $C^\infty$-ring):

a [[space]] that behaves as if its algebra of functions is a finitely generated [[smooth algebra]].


Given that a [[smooth algebra]] is a smooth refinement of an ordinary [[ring]] with a morphism from $\mathbb{R}$, a smooth locus is the analog in [[Models for Smooth Infinitesimal Analysis|well-adapted models]] for [[synthetic differential geometry]] for what in [[algebraic geometry]] is an [[affine variety]] over $\mathbb{R}$.

#Definition#

A finitely generated [[smooth algebra]] is one of the form $C^\infty(\mathbb{R}^n)/J$, for $J$ an ideal of the ordinary underlying algebra.

Write $C^\infty Ring^{fin}$ for the [[category]] of finitely generated smooth algebras. 

Then the [[opposite category]] $\mathbb{L} := (C^\infty Ring^{fin})^{op}$ is the [[category]] of **smooth loci**.


## Notation ##

For $A \in C^\infty Ring^{fin}$ one write $\ell A$ for the corresponding object in $\mathbb{L}$.

Often one also write

$$
  R := \ell C^\infty(\mathbb{R})
$$ 

for the real line regarded as an object of $\mathbb{L}$. 

# Properties #

The category $\mathbb{L}$ has the following properties:

* there is a [[full and faithful functor]] 

  $$
    Diff \to \mathbb{L}
  $$

  from the category [[Diff]] of [[manifold]]s 
  that   preserves [[pullback]]s along [[transversal map]]s.

* the [[Tietze extension theorem]] holds in $\mathbb{L}$: $R$-valued functions on closed subobjects in $\mathbb{L}$ have an extension.

# Applications #

There are various [[Grothendieck topology|Grothendieck topologies]] on $\mathbb{L}$ and various of its subcategories, such that [[category of sheaves|categories of sheaves]] on these are [[smooth topos]]es that are well-adapted models for [[synthetic differential geometry]].

For more on this see 

* [[Models for Smooth Infinitesimal Analysis]]

#References#

the concept originates in ...

A comprehensive textbook discussion is in chapter II, section 1 of 

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]].