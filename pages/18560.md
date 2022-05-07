[[!redirects (infinity, 1)-profunctor]]
[[!redirects (infinity, 1)-profunctor]]
[[!redirects (\infty, 1)-profunctor]]
#Contents#
* table of content
{:toc}

## Idea

The concept of _$(\infty, 1)$-profunctor_ plays the role of [[profunctor]] in [[(∞,1)-category theory]].

## Definition ##

If $C$ and $D$ are [[(∞,1)-categories]], then a **profunctor** from $C$ to $D$ is a [[(∞,1)-functor]] of the form

$$
  F \colon D^{op}\times C \to \infty Grpd
  \,.
$$

Such a  profunctor is usually written as $F\colon  C &#8696; D$. Composition of (∞,1)-profunctors in [[(∞,1)Prof]] is by the "tensor product of (∞,1)-functors" [[homotopy coend]] construction: if $H\colon A &#8696;  B$ and $K\colon B &#8696;  C$, their composite is given as a functor $C^{op}\times A \to \infty Grpd$ by
$$(c,a)\mapsto \int^{b\in B} H(b,a)\times K(c,b).$$

Every [[(∞,1)-functor]] $f\colon C\to D$ induces two (∞,1)-profunctors $D(1,f)\colon C &#8696; D$ and $D(f,1)\colon D &#8696; C$, defined by $D(1,f)(d,c) = D(d,f(c))$ and $D(f,1)(c,d) = D(f(c),d)$. (Here $D(-,-)$ denotes the [[hom functor]] of $D$ and $1$ denotes the identity (∞,1)-functor on the respective category.) 

Since a profunctor is also known as a (bi)module or a distributor or a correspondence, we should expect other names to be used for $(\infty, 1)$-profunctor. In [[Higher Topos Theory]] (Definition 2.3.1.3), Lurie speaks of a **correspondence**.

##Related pages

* [cograph of an (∞,1)-profunctor](cograph+of+a+profunctor#in_category_theory_2)
* [[(∞,1)Prof]]

##References

* [[Emily Riehl]], [[Dominic Verity]], _Kan extensions and the calculus of modules for ∞-categories_, ([arXiv:1507.01460](https://arxiv.org/abs/1507.01460))
* [[Rune Haugseng]], _Bimodules and natural transformations for enriched ∞-categories_, ([arXiv:1506.07341](https://arxiv.org/abs/1506.07341))

[[!redirects (∞,1)-profunctor]]
[[!redirects (∞,1)-profunctors]]
[[!redirects (infinity,1)-profunctors]]

