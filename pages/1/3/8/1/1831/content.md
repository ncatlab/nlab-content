
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

Cartesian fibrations over$S$ are the fibrant objects in the [[model structure on marked simplicial over-sets]] over $S$.

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

### General properties


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


### Pullback of Cartesian fibrations

Since a Cartesian fibration is in particular an [[inner fibration]] and since inner fibrations are stable under [[pullback]] in [[sSet]], it follows that for $p : E \to C$ a Cartesian fibration, the fiber $E_x$ over every point $x \in C_0$ is a [[quasi-category]]

$$
  \array{
    E_x &\to& E
    \\
    \downarrow && \downarrow
    \\
    \{x\} &\to& C
  }
  \,.
$$

The difference between inner fibrations and Cartesian fibrations is that only for Cartesian fibrations is it generally guaranteed that these fibers over the points are _functorially_ related over the morphisms in $C$. This is the content of the [[(∞,1)-Grothendieck construction]].

But moreover:

+-- {: .un_prop}
###### Proposition

The pullback of a Cartesian fibration in [[sSet]] is again a Cartesian fibration.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 2.4.2.3]].

We know from the discussion at [[inner fibration]] that the pullback is an inner fibration. It remains to check if it has enough [[Cartesian morphism]]s. By [[Higher Topos Theory|HTT, prop 2.4.1.3]] we have that in a [[pullback]] diagram

$$  
  \array{
    E' &\stackrel{q}{\to}& E
    \\
    {}^{\mathllap{p'}}\downarrow && \downarrow^{\mathrlap{p}}
    \\ 
    C' &\stackrel{k}{\to}& C
  }
$$

a morphism $f \in E'$ is $p'$-Cartesian if $q(f)$ is $p$-Cartesian. Since the morphisms of $E'$ are pairs of morphisms $(\gamma, \hat f) \in C'_1 \times E_1$  and since by assumption $p$ is a Cartesian, there is for $\gamma \in C'_1$ a Cartesian lift $\hat f \in E$ of $k(\gamma)$. Hence a Cartesian lift $(\gamma, \hat f)$ of $\gamma$ in $E'$.

 
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


### Relation to other kinds of fibrations

The notion of [[right fibration]] is a special case of that 
of Cartesian fibration:

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


There are also the "categorical fibrations", the fibrations in the Joyal [[model structure for quasi-categories]] on $sSet$. These turn out not to have much of an intrinsic category theoretic meaning. By the following proposition one can understand the notion of Cartesian fibration as  a suitable refinement of the notion of categorical fibration

+-- {: .un_prop}
###### Proposition 

Every Cartesian $p : X \to Y$ in [[sSet]] is a fibration with respect to the [[Andre Joyal|Joyal]] [[model structure for quasi-categories]] on [[sSet]].

=--

+-- {: .proof}
###### Proof

This is  [[Higher Topos Theory|HTT, prop. 3.3.1.7]].

=--


However, when the base is an $\infty$-groupoid, then the difference between Cartesian fibrations and categorical fibrations disappears:

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

There is however another [[model category]] structure, which does model Cartesian fibrations.

+-- {: .un_prop}
###### Proposition 

Let $sSet^+/Y$ be the [[overcategory]] of the category of [[marked simplicial set]]s over $S$, equipped with the [[model structure on marked simplicial over-sets]]. 

An object $X \to Y$ is fibrant in that model category precisely if 

* the underlying morphism of simplicial sets $X \to Y$ is a Cartesian fibration;

* the marked edges in $X$ are precisely the [[Cartesian morphism]]s.


=--

+-- {: .proof}
###### Proof

This is  [[Higher Topos Theory|HTT, prop. 3.1.4.1]].

=--

## Examples 

### Cartesian fibrations over simplices {#CartOverSimplex}


... for the moment see [[Higher Topos Theory|HTT, section 3.2.2]] ...


### The universal Cartesian fibration

for the moment see

* [[universal fibration of (∞,1)-categories]]. 



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