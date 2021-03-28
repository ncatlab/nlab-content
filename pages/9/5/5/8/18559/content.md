[[!redirects (infinity, 1)Prof]]
#Contents#
* table of contents
{:toc}


## Definition

$\mathbf{(\infty, 1)Prof}$ is the [[(∞,2)-category]] of [[(∞,1)-categories]], [[(\infty, 1)-profunctor|(∞,1)-profunctors]], and [[natural transformations]].  

Recall that a (∞,1)-profunctor from $A$ to $B$ is a (∞,1)-functor $B^{op}\times A\to \infty Grpd$.  Composition of (∞,1)-profunctors in $(\infty, 1)Prof$ is by the "tensor product of (∞,1)-functors" [[homotopy coend]] construction: if $H\colon A &#8696;  B$ and $K\colon B &#8696;  C$, their composite is given as a functor $C^{op}\times A \to \infty Grpd$ by
$$(c,a)\mapsto \int^{b\in B} H(b,a)\times K(c,b).$$
The identity on an (∞,1)-category $A$ is its hom-functor $Hom_A(-,-)$.



## Properties

Note that every (∞,1)-functor $f\colon A\to B$ gives two [[representable functor|representable]] (∞,1)-profunctors $B(f-,-)$ and $B(-,f-)$.  This defines two [[(∞,2)-functors]] $(\infty,1)Cat \to (\infty,1)Prof$ that are the identity on objects.  The relationship between [[(∞,1)Cat]] and $(\infty,1)Prof$ encoded in this way makes them into an $(\infty, 1)$-version of an [[equipment]], see ([Haugseng 15](#Haugseng15)).

$(\infty, 1)Prof$ can act as a classifying object for kinds of (∞,1)-functors; see [higher exponentiable functor](Conduch&#233;+functor#highercategorical_versions).

$(\infty,1)Prof$ is equivalent to the full subcategory of [[Pr(∞,1)Cat]] whose objects are presheaf categories.

## Related concepts

* [[Prof]]
* [[Pr(∞,1)Cat]]

##References

* {#Haugseng15} [[Rune Haugseng]], _Bimodules and natural transformations for enriched ∞-categories_, ([arXiv:1506.07341](https://arxiv.org/abs/1506.07341))


[[!redirects (∞,1)Prof]]