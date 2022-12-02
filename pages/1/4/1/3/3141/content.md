
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## In category theory

### Definition

Let $H\colon A &#8696;B$ be a [[profunctor]], i.e. a [[functor]] $B^{op}\times A\to Set$.  Its **cograph**, also called its **collage**, is the [[category]] $\bar{H}$ whose set of objects is the [[disjoint union]] of the sets of objects of $A$ and $B$, and where

$$ \begin{aligned}
  \bar{H}(a_1,a_2) &= A(a_1,a_2)\\
  \bar{H}(b_1,b_2) &= B(b_1,b_2)\\
  \bar{H}(b,a) &= H(b,a)\\
  \bar{H}(a,b) &= \emptyset
  \end{aligned}
$$

where composition is defined as in $A$, $B$, and according to the actions of $A$ and $B$ on $H$.

The [[cograph of a functor]] is the special case when $H$ is a "representable profunctor" of the form $B(f-,-)$ for some functor $f\colon A\to B$.

### Properties

The cograph of a profunctor can be given a universal property: it is the [[lax colimit]] of that profunctor, considered as a single arrow in the [[bicategory]] of profunctors.  (The word "collage" is also sometimes used more generally for any lax colimit, especially in a $Prof$-like bicategory.)  The cograph of a profunctor is also a [[cotabulator]] in the [[proarrow equipment]] of profunctors.  Furthermore, the [[cospans]] $A\to \bar{H} \leftarrow B$ which are cographs of profunctors can be characterized as the two-sided [[codiscrete cofibrations]] in the [[2-category]] [[Cat]].

Cographs of profunctors can also be characterized as categories equipped with a functor to the [[interval category]] $(0\to 1)$, where $B$ is the fiber over $0$ and $A$ is the fiber over $1$.  See [[joyalscatlab:Distributors and barrels]].


## In $(\infty,1)$-category theory

The notion of a cograph of a profunctor generalizes to [[(∞,1)-category theory]].


### Definition

+-- {: .un_defn}
###### Definition

For $C$ and $D$ two [[(∞,1)-categories]] a **correspondence** between them is an $(\infty,1)$-category $p : K \to \Delta[1]$ over the [[interval category]] $\Delta[1] = \{0 \to 1\}$ with an [[equivalence of (∞,1)-categories|equivalences]] $K_0 \simeq C$ and $K_1 \simeq D$.

=--

This appears as ([Lurie, def 2.3.1.3](#Lurie)).

### Properties

+-- {: .un_prop}
###### Proposition

There is a canonical bijection between equivalence classes of correspondences between $C$ and $D$ and equivalence classes of [[(∞,1)-profunctors]], i.e., [[(∞,1)-functors]]

$$
  C^{op} \times D \to \infty Grpd
$$

from the product of $D$ with the [[opposite-(∞,1)-category]] of $C$ to [[∞Grpd]].

=--

This appears as ([Lurie, remark 2.3.1.4](#Lurie)).

Therefore the correspondence corresponding to a profunctor is its cograph/collage.

+-- {: .un_prop}
###### Proposition

An $(\infty,1)$-profunctor comes from an ordinary [[(∞,1)-functor]] $F : C \to D$ precisely if its cograph $p : K \to \Delta[1]$ is not just an inner fibration but a [[coCartesian fibration]]. 

And it comes from a functor $G : D \to C$ precisely if it is a [[Cartesian fibration]]. And precisely if both is the case is $F$ the right [[adjoint (∞,1)-functor]] to $G$.


=--

Because by the [[(∞,1)-Grothendieck construction]] 

* coCartesian fibrations $K \to \Delta[1]$ correspond to [[(∞,1)-functor]]s $\Delta[1] \to$ [[(∞,1)Cat]];

* [[Cartesian fibration]]s $K \to \Delta[1]$ correspond to [[(∞,1)-functor]]s $\Delta[1]^{op} \to$ [[(∞,1)Cat]].

* and as discussed at [[adjoint (∞,1)-functor]], an $(\infty,1)$-functor has an adjoint precisely if the coCartesian fibration corresponding to it is also Cartesian.




## Related concepts

* [[graph of a functor]]

* [[cograph of a functor]], **cograph of a profunctor**

* [[cotabulator]]


## References

For ordinary and [[enriched category theory|enriched]] categories, cographs were studied (and used to characterize profunctors) by:

* [[Ross Street]], "Fibrations in bicategories"

* Carboni and Johnson and Street and Verity, "Modulated bicategories"

The $(\infty,1)$-category theoretic notion ("correspondence") is the topic of section 2.3.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 
{#Lurie}

See Ross Street's post in category-list 2009, [Re: pasting along an adjunction](http://article.gmane.org/gmane.science.mathematics.categories/255/match=).

[[!redirects collage]]
[[!redirects collages]]
