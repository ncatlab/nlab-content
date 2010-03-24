
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Cartesian fibrations are one of the types of [[fibrations of quasi-categories]].

A _Cartesian fibration_ of quasi-categories -- or more generally of [[simplicial set]]s -- is a morphism that generalizes the notion of [[Grothendieck fibration]] from [[category theory]] to [[(∞,1)-category theory]], specifically with [[(∞,1)-categories]] incarnated as [[quasi-categories]]:

it is an [[inner fibration]] that lifts also all right _outer_ [[horn]] inclusions whose last edge is a [[cartesian morphism]], and such that there is a sufficient supply of cartesian morphisms.

If an [[(∞,1)-functor]] $p : C \to D$ if a Cartesian fibration then it possible to interpret its value over any [[morphism]] $f : d_1 \to d_2$ in $D$ as an [[(∞,1)-functor]] $p^{-1}(f) : p^{-1}(d_2) \to p^{-1}(d_1)$ between the [[fibers]] $p^{-1}(d_2)$ and $p^{-1}(d_1)$ over its source and target [[objects]]. 

This way a Cartesian fibration $p : C \to D$ determines and is determined by an [[(∞,1)-functor]] $D^{op} \to (\infty,1)Cat$ into the
[[(∞,1)-category of (∞,1)-categories]]. This is the content of the [[(∞,1)-Grothendieck construction]].

## Definition 

+-- {: .un_defn}
###### Definition

A morphism $p : X \to Y$ in [[sSet]] is a 
**Cartesian fibration** if

* it is an [[inner fibration]] 

* for every edge $f : x \to y$ of $Y$ and for every lift $\hat {y}$ of 
  $y$ (that is: $p(\hat{y})=y$)
  there is a [[cartesian morphism|Cartesian edge]] 
  $\hat{f} : \hat{x} \to \hat{y}$ in $X$ lifting $f$ 
  (that is: such that $p(\hat f) = f$)

The morphism is a Cartesian **opfibration** if the [[opposite quasi-category|opposite]] $p^{op} : X^{op} \to Y^{op}$ is a Cartesian fibation.

=--

This is [[Higher Topos Theory|HTT, def. 2.4.2.1]].



## Properties {#Properties}


+-- {: .un_prop}
###### Proposition

We have:

* Every [[isomorphism]] of [[simplicial sets]] is a Cartesian fibration.

* Cartesian fibrations are [[pullback stability|stable under pullback]] in [[SSet]].

* The composite of two Cartesian fibrations is again a Cartesian fibration.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 2.4.2.3 ]].

=--


+-- {: .un_prop}
###### Proposition 


The following are equivalent:

* $p : X \to Y$ is a Cartesian fibration and every edge in $X$ is 
  $p$-Cartesian

* $p$ is a [[right fibration]];

* $p$ is a Cartesian fibration and every fiber is a [[Kan complex]].

=--

+-- {: .proof}
###### Proof

This is  [[Higher Topos Theory|HTT, prop. 2.4.2.4]].

=--



+-- {: .un_prop}
###### Proposition (over $\infty$-groupoids)

Let $p : X \to Y$ be a morphism of [[simplicial set]]s where $Y$ is a [[Kan complex]]. Then the following are equivalent:

1. $p$ is a Cartesian fibration

1. $p$ is a coCartesian fibration

1. $p$ is a [[Joyal model structure on simplicial sets|categorical fibration]]

=--

+-- {: .proof}
###### Proof

This is  [[Higher Topos Theory|HTT, prop. 3.3.1.8]].

=--


We can test locally if a morphism is a Cartesian fibration:

+-- {: .un_prop}
###### Proposition

An [[inner fibration]] $p : X \to Y$ is Cartesian precisely if for every $n$-[[simplex]] $\sigma : \Delta[n] \to Y$ the [[sSet]]-[[pullback]] $\sigma^* p : X \times_Y \Delta[n]$ in

$$
  \array{
    X \times_Y \Delta[n] &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    \Delta[n] &\stackrel{\sigma}{\to}& Y
  }
$$

is a Cartesian fibration.

=--

+-- {: .proof}
###### Proof

This is  [[Higher Topos Theory|HTT, cor. 2.4.2.10]].

=--



## References 


Section 2.4.2 in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects cartesian fibration]]
[[!redirects coCartesian fibration]]
[[!redirects co-cartesian fibration]]
[[!redirects cocartesian fibration]]
[[!redirects Cartesian fibrations]]
[[!redirects cartesian fibrations]]
[[!redirects coCartesian fibrations]]
[[!redirects co-cartesian fibrations]]
[[!redirects cocartesian fibrations]]