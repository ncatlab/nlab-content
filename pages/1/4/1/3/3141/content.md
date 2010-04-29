
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

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

## Properties

The cograph of a profunctor can be given a universal property: it is the [[lax colimit]] of that profunctor, considered as a single arrow in the [[bicategory]] of profunctors.  (The word "collage" is also sometimes used more generally for any lax colimit, especially in a $Prof$-like bicategory.)  The cograph of a profunctor is also a [[cotabulation]] in the [[proarrow equipment]] of profunctors.  Furthermore, the [[cospans]] $A\to \bar{H} \leftarrow B$ which are cographs of profunctors can be characterized as the two-sided [[codiscrete cofibrations]] in the [[2-category]] [[Cat]].

Cographs of profunctors can also be characterized as categories equipped with a functor to the [[interval category]] $(0\to 1)$, where $B$ is the fiber over $0$ and $A$ is the fiber over $1$.  See [[joyalscatlab:Distributors and barrels]].


## In higher category theory

All of this can be generalized to [[enriched categories]] and also to [[higher category theory|higher categories]].

### In $(\infty,1)$-category theory

In [[Higher Topos Theory|HTT, def 2.3.1.3]] we have the following definition of cographs of profunctors between [[(∞,1)-categories]].

+-- {: .un_defn}
###### Definition

For $C$ and $D$ two [[(∞,1)-categories]] incarnated as [[quasi-categories]], the cograph of a profunctor between them is an [[inner fibration]]
$p : K \to \Delta[1]$ over the [[interval category]] $\Delta[1] = \{0 \to 1\}$ with an identification $K_0 \simeq C$ and $K_1 \simeq D$.

=--

In this language an $(\infty,1)$-profunctor comes from an ordinary [[(∞,1)-functor]] $F : C \to D$ precisely if its cograph $p : K \to Delta[1]$ is not just an inner fibration but a [[coCartesian fibration]]. And it comes from a functor $G : D \to C$ precisely if it is a [[Cartesian fibration]]. And precisely if both is the case do is $G$ the right [[adjoint (∞,1)-functor]] to $G$.


## References

The notion of a cograph of a profunctor appears here and there in the literature under different names. For instance in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

it appears under the term _correspondence_ in section 2.3.1


[[!redirects collage]]
[[!redirects collages]]
