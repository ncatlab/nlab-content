
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Cartesian fibrations are one of the types of [[fibrations of quasi-categories]].

A _Cartesian fibration_ of quasi-categories -- or more generally of [[simplicial set]]s -- is a morphism that generalizes the notion of [[Grothendieck fibration]] from [[category theory]] to [[(∞,1)-category theory]], specifically with [[(∞,1)-categories]] incarnated as [[quasi-categories]]:

It is an [[inner fibration]] that lifts also all right _outer_ [[horn]] inclusions whose last edge is a [[cartesian morphism]], and such that there is a sufficient supply of [[cartesian morphisms]].

An [[inner fibration]] $p : C \to D$ may be thought of as a family of [[(infinity,1)-categories]] $(C_d)_{d \in D}$ which is [[functorial]] in $d$ only in the sense of [[correspondences]].  Then the condition of $p$ being a cartesian fibration ensures that the family is actually [[functorial]].
More precisely, if an [[(∞,1)-functor]] $p : C \to D$ is a Cartesian fibration, then it is possible to interpret its value over any [[morphism]] $f : d_1 \to d_2$ in $D$ as an [[(∞,1)-functor]] $p^{-1}(f) : p^{-1}(d_2) \to p^{-1}(d_1)$ between the [[fibers]] $p^{-1}(d_2)$ and $p^{-1}(d_1)$ over its source and target [[objects]]. 

This way a Cartesian fibration $p : C \to D$ determines and is determined by an [[(∞,1)-functor]] $D^{op} \to (\infty,1)Cat$ into the
[[(∞,1)-category of (∞,1)-categories]]. This is the content of the [[(∞,1)-Grothendieck construction]].

Cartesian fibrations over $S$ are the fibrant objects in the [[model structure on marked simplicial over-sets]] over $S$.

## Definition 

+-- {: .un_defn}
###### Definition

A morphism $p : X \to Y$ in [[sSet]] is a 
**Cartesian fibration** (or **Grothendieck fibration**) if

* it is an [[inner fibration]] 

* for every edge $f : x \to y$ of $Y$ and for every lift $\hat {y}$ of 
  $y$ (that is: $p(\hat{y})=y$)
  there is a [[cartesian morphism|Cartesian edge]] 
  $\hat{f} : \hat{x} \to \hat{y}$ in $X$ lifting $f$ 
  (that is: such that $p(\hat f) = f$)

The morphism is a **cocartesian fibration** (or **Cartesian opfibration**, **Grothendieck opfibration**) if the [[opposite quasi-category|opposite]] $p^{op} : X^{op} \to Y^{op}$ is a Cartesian fibration.

=--

This is [[Higher Topos Theory|HTT, def. 2.4.2.1]].

+-- {: .un_defn}
###### Definition

Given cartesian fibrations $p : X \to C$ and $q : Y \to C$, let $Map_C^{cart}(p,q) \subseteq Map_C(p,q)$ and $Fun_C^{cart}(p,q) \subseteq Fun_C(p,q)$ be the full subsimplicial sets spanned by the functors that preserve cartesian morphisms. We call such functors **cartesian functors**.

Dually, we make the analogous definition of cocartesian functor.

=--

+-- {: .un_remark}
###### Remark

The $Map_C^{cart}$ are the mapping spaces in the (cartesian) model structure on marked simplicial sets over $C$.

=--

## Properties {#Properties}

### General properties


+-- {: .un_prop}
###### Proposition

We have:

* Every [[isomorphism]] of [[simplicial sets]] is a Cartesian fibration.

* The composite of two Cartesian fibrations is again a Cartesian fibration.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 2.4.2.3 ]].

=--

+-- {: .un_prop}
###### Proposition


Every Cartesian fibration is a fibration in the [[Andre Joyal|Joyal]]-[[model structure for quasi-categories]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 3.3.1.7]].

=--


### Behaviour under pullback {#BehaviourUnderPullback}

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

a morphism $f \in E'$ is $p'$-Cartesian if $q(f)$ is $p$-Cartesian. Since the morphisms of $E'$ are pairs of morphisms $(\gamma, \hat f) \in C'_1 \times E_1$  and since by assumption $p$ is a Cartesian fibration, there is for $\gamma \in C'_1$ and $y \in E'_0$ such that $p'(y)$ is the target of the morphism $\gamma$ a Cartesian lift $\hat f \in E$ of $k(\gamma)$ such that $q(y)$ is the target of $\hat f$. Hence a Cartesian lift $(\gamma, \hat f)$ of $\gamma$ in $E'$ having $y$ as target.

 
=--



We can test locally if a morphism is a Cartesian fibration:

+-- {: .un_prop}
###### Proposition

An [[inner fibration]] $p : X \to Y$ is Cartesian precisely if for each $n \leq 2$ and for every $n$-[[simplex]] $\sigma : \Delta[n] \to Y$ the [[sSet]]-[[pullback]] $\sigma^* p : X \times_Y \Delta[n] \to \Delta[n]$ in

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


+-- {: .un_prop}
###### Proposition

The [[pullback]] in [[sSet]] of a weak equivalence in the [[Andre Joyal|Joyal]]-[[model structure for quasi-categories]] along a Cartesian fibration is again a Joyal-weak equivalence

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 3.3.1.3]]

=--


+-- {: .un_lemma}
###### Lemma

Equivalences in $sSet_{Joyal}$ are stable under pullback along Cartesian fibrations:

if 

$$
  \array{
    X \times_S T &\to & X
    \\
    \downarrow && \downarrow
    \\ 
    T &\stackrel{\simeq}{\to}& S 
  }
$$

is a [[pullback]] square in [[sSet]] with $T \to S$ a weak equivalence in $sSet_{Joyal}$ and $X \to S$ a Cartesian fibration, then $X \times_S T \to X$ is also a weak equivalence.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 3.3.1.3]].

=--


The following proposition asserts that the ordinary pullback (in [[sSet]]) of Cartesian fibrations already models the correct [[homotopy pullback]].

+-- {: .un_prop}
###### Proposition


Let 

$$
  \array{
    X &\to& X'
    \\
    \downarrow && \downarrow
    \\
    S &\to & S'
  }
$$

be an [[pullback]] [[diagram]] in [[sSet]] of quasi-categories, where $X' \to S'$ is a Cartesian fibration. Then this is already a [[homotopy pullback]] diagram with respect to the [[model structure for quasi-categories]]. 

=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop 3.3.1.4]]. We factor the bottom morphism as $ S \stackrel{\simeq}{\to} T \to S' $ into a weak equivalence and a fibration in $sSet_{Joyal}$. Then the right square in 

$$
  \array{
    X &\to& T \times_{S'} X'& \to& X'
    \\
    \downarrow && \downarrow && \downarrow
    \\
    S &\to & T &\to& S'
  }
$$

is the ordinary pullback over a fibrant replacement of the original diagram hence is a homotopy pullback. The claim follows thus if $X \to T \times_{S'} X'$ is a weak equivalence, which it is by one of the above lemmas.

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

Every Cartesian fibration $p : X \to Y$ in [[sSet]] is a fibration with respect to the [[Andre Joyal|Joyal]] [[model structure for quasi-categories]] on [[sSet]].

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

Let $sSet^+/S$ be the [[overcategory]] of the category of [[marked simplicial set]]s over $S$, equipped with the [[model structure on marked simplicial over-sets]]. 

An object $X \to S$ is fibrant in that model category precisely if 

* the underlying morphism of simplicial sets $X \to S$ is a Cartesian fibration;

* the marked edges in $X$ are precisely the [[Cartesian morphism]]s.


=--

+-- {: .proof}
###### Proof

This is  [[Higher Topos Theory|HTT, prop. 3.1.4.1]].

=--

### Free (co)cartesian fibrations

The inclusion of the cartesian fibrations and cartesian functors in the category $(\infty,1)Cat_{/C}$ has a left adjoint.

+-- {: .un_prop}
###### Proposition 

For maps $p : X \to C$ and cartesian fibrations $q : Y \to C$, there are a natural equivalences
$$
  Fun_C(p, q) \simeq Fun_C^{cart}((C \downarrow p), q)
$$
Dually, for maps $p : X \to C$ and cocartesian fibrations $q : Y \to C$, there are natural equivalences
$$
  Fun_C(p, q) \simeq Fun_C^{cocart}((p \downarrow C), q)
$$

=--

+-- {: .proof}
###### Proof

The cartesian case for mapping spaces is theorem 4.11 of [Gepner-Haugseng-Nikolaus](#GepnerHaugsengNikolaus15). For the cocartesian case,

$$
  Fun_C(p,q) \simeq Fun_{C^{op}}(p^{op}, q^{op})^{op}
  \simeq \Fun_{C^{op}}^{cart}((C^{op} \downarrow p^{op}), q^{op})^{op}
  \simeq \Fun_C^{cocart}((p \downarrow C), q)
$$

=--


## Examples 

### Projections from comma categories 


+-- {: .un_prop}
###### Proposition 

Given functors $F : A \to C$ and $G : B \to C$ between quasi-categories,
the projection $(F \downarrow G) \to A$ is a Cartesian fibration
and the projection $(F \downarrow G) \to B$ is a coCartesian fibration.

In particular, if $C$ is a quasi-category, then $eval_0 : C^{\Delta^1} \to C$
is a Cartesian fibration and $eval_1 : C^{\Delta^1} \to C$ is a coCartesian fibration.

=--


+-- {: .proof}
###### Proof

Consider the diagram of pullback squares

$$
  \array{
    (F \downarrow G) &\to& (id_C \downarrow G) &\to& B
    \\
    \downarrow && \downarrow && \downarrow G\!\!
    \\
    (F \downarrow id_C) &\to& C^{\Delta^1} &\xrightarrow{1}& C
    \\
    \downarrow && \downarrow 0\!\!
    \\
    A &\xrightarrow{F}& C
  }
$$

[[Higher Topos Theory|HTT, prop. 2.4.7.12]] states the projection $(id_C \downarrow G) \to C$ is a Cartesian fibration.  Then $(F \downarrow G) \to A$ is as well, since fibrations are preserved by pullback. Dually for the other projection.

=--

The fiber of $eval_1 : C^{\Delta^1} \to C$ at an object $X \in C$ is the slice category $C_{/X}$. So, by the [[(infinity,1)-Grothendieck construction]],
this fibration corresponds to the slice functor
$C \to (\infty,1)Cat : X \mapsto C_{/X}$, where a morphism $X \to Y$
induces the composition map $C_{/X} \to C_{/Y}$.


### Cartesian fibrations over one morphism and Adjunctions

By the [[(infinity,1)-Grothendieck construction]] a Cartesian fibration $K \to \Delta[1]$ corresponds to a morphism $\Delta[1]^{op} \to (\infty,1)Cat$, hence to an [[(infinity,1)-functor]] $f : C \to D$.

Obtaining this through the straightening functor above is tedious, but there is a more immediate way to characterize $f$:

+-- {: .un_def}
###### Definition

For $p : K \to \Delta[1]$ a Cartesian fibration with specified equivalences

$$
  h_0  : C \stackrel{\simeq}{\to} p^{-1}(0)
$$

and 

$$
  h_1 : D \stackrel{\simeq}{\to} p^{-1}(1)
$$

an [[(infinity,1)-functor]] $f : D \to C$ is **associated** to $p$ if there exists a commuting diagram

$$
  \array{
    D \times \Delta[1] &&\stackrel{s}{\to}&& K
    \\
    & \searrow && \swarrow
    \\
    && \Delta[1]
  }
$$

such that 

* $s|_{D \times \{1\}} = h_1$;

* $s|_{D \times \{0\}} = h_0 \circ f$

* for every object $x$ of $D$ we have that $s|_{\{x\} \times \Delta[1]}$ is 
  a p-[[Cartesian morphism]] of $K$. 

=--

This is [[Higher Topos Theory|HTT, def. 5.2.1.1]].

If $p : K \to \Delta[1]$ is both a Cartesian fibration as well as a coCartesian fibration, then it determines $(\infty,1)$-functors in both directions

$$
  C
    \stackrel{\leftarrow}{\to} 
  D
  \,.
$$

Such a pair is a pair of [[adjoint (infinity,1)-functor]]s.

### Cartesian fibrations over simplices {#CartOverSimplex}


... for the moment see [[Higher Topos Theory|HTT, section 3.2.2]] ...


### The universal Cartesian fibration

for the moment see

* [[universal fibration of (∞,1)-categories]]. 

## Related concepts

* [[Kan fibration]], [[anodyne morphism]]

* [[right/left Kan fibration]], [[right/left anodyne map]]

* [[inner fibration]]

* **Cartesian fibration**, [[Cartesian fibration of dendroidal sets]]

* [[coCartesian fibration of (∞,1)-operads]]


## References 
 

* [[Jacob Lurie]], section 2.4.2 in _[[Higher Topos Theory]]_

* {#MazelGee15} [[Aaron Mazel-Gee]], _A user's guide to co/cartesian fibrations_ ([arXiv:1510.02402](http://arxiv.org/abs/1510.02402))


* {#GepnerHaugsengNikolaus15} [[David Gepner]], [[Rune Haugseng]], [[Thomas Nikolaus]], _Lax colimits and free fibrations in $\infty$-categories_ ([arXiv:1501.02161](http://arxiv.org/abs/1501.02161))

[[!redirects cartesian fibration]]
[[!redirects coCartesian fibration]]
[[!redirects co-cartesian fibration]]
[[!redirects cocartesian fibration]]
[[!redirects Cartesian fibrations]]
[[!redirects cartesian fibrations]]
[[!redirects coCartesian fibrations]]
[[!redirects co-cartesian fibrations]]
[[!redirects cocartesian fibrations]]