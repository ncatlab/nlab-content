
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

If $C$ is a [[finitely complete category]] (a category with all finite limits), then it is interesting to consider a left [[exact functor]] on $C$ (a functor that preserves all [[finite limit]]s).  Even if $C$ lacks some finite limits, then this concept still makes sense, but it may not be the correct one.  Instead we use the stronger concept of a _flat functor_, which may be thought of as a functor that preserves all finite limits ---even the ones that don\'t exist yet!


## Definitions

It turns out that the most appropriate generality in which to speak of a flat functor $C \to D$ is when $D$ is a [[site]].  We build up to this definition in stages through several more classical notions, remarking at each stage on some basic properties and equivalences.  Proofs will be given in the following section.


### $Set$-valued functors

The most classical notion is the following.

+-- {: .num_defn #SetValuedFlat}
###### Definition

A functor $C\to Set$ is **flat** if the opposite of its [[category of elements]], $el(C)^{op}$, is a [[filtered category]].

=--

For disambiguation with the later notions, we may refer to such a functor as being **$Set$-valued flat**.

+-- {: .num_remark }
###### Remark

Spelled out explicitly, this means that $E : C \to Set$ is flat precisely if the following three conditions hold.

1. (non-emptiness) There is at least one [[object]] $c \in C$ such that $E(c)$ is an [[inhabited set]].

1. (transitivity) For objects $c,d \in C$ and elements $y \in E(c)$, $z \in E(d)$, there exists an object $b \in C$, [[morphisms]] $\alpha : b \to c$, $\beta : b \to d$ and an element $w \in E(b)$ such that $E(\alpha) : w \mapsto y$ and $E(\beta) :w \mapsto z $.

1. (freeness) For two parallel morphisms $\alpha, \beta : c \to d$ and $y \in E(c)$ such that $E(\alpha)(y) = E(\beta)(y)$, there exists a morphism $\gamma : b \to c$ and an element $z \in E(b)$ such that $\alpha \circ \gamma = \beta \circ \gamma$ and $E(\gamma) : z \mapsto y$.

=--

+-- {: .num_prop}
###### Proposition
When $C$ is [[small category|small]], a functor $F\colon C\to Set$ is $Set$-valued flat if and only if its [[Yoneda extension]] $[C^{op},Set] \to Set$ preserves finite limits.
=--

This partially explains the terminology "flat", since the Yoneda extension is a sort of [[tensor product of functors|tensoring with]] $F$, and a [[flat module]] is one such that tensoring with it preserves finite limits.

+-- {: .num_cor}
###### Corollary
If $F\colon C\to Set$ is flat, then it preserves all finite limits that exist in $C$.  Conversely, if $C$ has finite limits and $F$ preserves them, then it is flat.
=--


### Representable flatness

+-- {: .num_defn #RepresentablyFlat}
###### Definition
A functor $F\colon C \rightarrow E$ is **flat** if for each [[object]] $e \in E$, the [[opposite category|opposite]] [[comma category]] $(e / F)^{op}$ is a [[filtered category]].
=--

Since $(e/F)$ is equivalent to the category of elements of the composite $C \xrightarrow{F} E \xrightarrow{E(e,-)} Set$, this is equivalent to saying  that $E(e,F-)\colon C\to Set$ is Set-valued flat for every $e\in E$.  Hence, this notion of flatness may be called **representably flat**.  Spelled out explicitly as we did above for flat set-valued functors, this means that for every $e\in E$, we have:

1. There is an object $c\in C$ and a morphism $e\to F(c)$.
1. For any $c,d\in C$ and morphisms $y:e\to F(c)$ and $z:e\to F(d)$, there exists an object $b\in C$, morphisms $\alpha : b \to c$, $\beta : b \to d$ in $C$, and a morphism $w: e\to F(b)$ such that $F(\alpha)\circ w = y$ and $F(\beta)\circ w = z$.

1. For two parallel morphisms $\alpha, \beta : c \to d$ in $C$, and a morphism $y : e \to F(c)$ such that $F(\alpha)\circ y = F(\beta)\circ y$, there exists a morphism $\gamma : b \to c$ in $C$ and a morphism $z : e \to F(b)$ such that $\alpha \circ \gamma = \beta \circ \gamma$ and $F(\gamma) \circ z = y$.

Representably flat functors are sometimes referred to simply as "[[exact functor|left exact functors]]".  On the $n$Lab we try to generally reserve the latter terminology for the case when $C$ has [[finite limits]].

+-- {: .num_prop}
###### Proposition
A functor $F \colon C \to E$ between small categories is representably flat if and only if the operation $Lan_F\colon [C^{op}, Set] \to [E^{op},Set]$ of [[left Kan extension]] preserves finite limits.
=--

A proof of this is given below as prop. \ref{FlatnessIfYonedaExtensionPreservesFiniteLimits}.
+-- {: .num_cor}
###### Corollary
If $F\colon C\to E$ is representably flat, then it preserves all finite limits that exist in $C$.  Conversely, if $C$ has finite limits and $F$ preserves them, then it is representably flat.
=--

+-- {: .num_cor}
###### Corollary
If $C$ has finite limits, then a functor $C\to Set$ is representably flat if and only if it is Set-valued flat, if and only if it preserves finite limits.
=--

However, if $C$ lacks finite limits, then representable flatness of $C\to Set$ can be stronger than Set-valued flatness.


### Topos-valued functors
 {#ToposValuedFlatFunctors}

+-- {: .num_defn #InternallyFlat}
###### Definition

Let $E$ be a [[cocomplete category|cocomplete]] [[topos]] (for instance a [[Grothendieck topos]]).  A functor $F\colon C\to E$ is **flat** if the statement "$F$ is $Set$-valued flat, def. \ref{SetValuedFlat}." is true in the [[internal logic]] of $E$.

Explicitly, this means that for any finite diagram $D\colon I\to C$, the family of factorizations through $\lim (F\circ D)$ of the $F$-images of all [[cones]] over $D$ in $C$ is [[epimorphism|epimorphic]] in $E$.
=--

For disambiguation, this notion of flatness may be called **internally flat** since it refers to the internal logic of $E$.  Internally flat functors have multiple other names:

* In [Johnstone, C2.3.7 and B3.2.3](#Johnstone) they are called "torsors".
* In [Mac Lane-Moerdijk, VII.8](#MLM) they are called "filtering functors".
* In [Moerdijk, II.2](#Moerdijk) they are called "principal functors".

+-- {: .num_remark }
###### Remark

Since the internal logic of $Set$ is just ordinary logic, a functor $C\to Set$ is internally flat just when it is $Set$-valued flat, def. \ref{SetValuedFlat}.

=--

More generally:

+-- {: .num_example }
###### Example

If $E$ has [[point of a topos|enough points]], then $F$ is internally flat precisely if for all [[stalks]] $x^* : E \to Set$ the composite $x^* \circ F$ is $Set$-valued flat.

=--

+-- {: .proof}
###### Proof

In a topos $E$ with enough points, a morphism $f : X \to Y$ is an [[epimorphism]] precisely if $x^* f$ is an epimorphism in $Set$. By definition, the [[stalks]] $x^* : E \to Set$ commute with [[finite limits]].

=--

+-- {: .num_prop}
###### Proposition
When $C$ is [[small category|small]], a functor $F\colon C\to E$ is internally flat if and only if its [[Yoneda extension]] $[C^{op},Set] \to E$ preserves finite limits.
=--

+-- {: .num_cor}
###### Corollary
If $F\colon C\to E$ is internally flat, then it preserves all finite limits that exist in $C$.  Conversely, if $C$ has finite limits and $F$ preserves them, then it is internally flat.
=--


### Site-valued functors
 {#SiteValuedFunctors}

Finally, we can give the most general definition, due to [Karazeris](#Karazeris)

+-- {: .num_defn #CoveringFlat}
###### Definition
Let $E$ be any [[site]].  A functor $F\colon C\to E$ is **flat** if for any finite diagram $D\colon I\to C$ and any [[cone]] $T$ over $F\circ D$ in $E$ with vertex $u$, the [[sieve]]
$$ \{ h\colon v\to u | T h \;\text{ factors through the }\; F\text{-image of some cone over }\; D \} $$
is a covering sieve of $u$ in $E$.
=--

For disambiguation, we may refer to this notion as being **covering-flat**.  

This subsumes the other three definitions as follows:

* If $E=Set$ with its [[canonical topology]], then covering-flatness reduces to Set-valued flatness, def. \ref{SetValuedFlat}.

* More generally, if $E$ is a cocomplete [[topos]] with its [[canonical topology]], then covering-flatness reduces to internal flatness, def. \ref{InternallyFlat}.

* On the other hand, if $E$ has a [[trivial topology]], then covering-flatness reduces to representable flatness, def. \ref{RepresentablyFlat}.

+-- {: .num_prop}
###### Proposition
If $C$ is a small category and $E$ is a [[small-generated site]], then a functor $F \colon C \to E$ is covering-flat if and only if its extension $[C^{op}, Set] \to Sh(E)$ preserves finite limits.
=--

+-- {: .num_cor}
###### Corollary
If $F\colon C\to E$ is covering-flat, where $E$ has finite limits and all covering families in $E$ are [[extremal epimorphism|extremal-epic]], then $F$ preserves all finite limits that exist in $C$.  Conversely, if $C$ has finite limits and $F$ preserves them, then it is covering-flat.
=--


## Properties

### Yoneda extensions

We now prove the asserted propositions about the equivalence of flatness with finite-limit-preserving extensions to presheaf categories.

+-- {: .num_prop}
###### Proposition
When $C$ is [[small category|small]], a functor $F\colon C\to Set$ is Set-valued flat if and only if its [[Yoneda extension]] $[C^{op},Set] \to Set$ preserves finite limits.
=--
+-- {: .proof}
###### Proof
This is prop. 6.3.8 in ([Borceux](#Borceux)).
=--

+-- {: .num_prop #FlatnessIfYonedaExtensionPreservesFiniteLimits}
###### Proposition

When $C$ and $E$ are [[small category|small]], a functor $F \colon C \to E$ is representably flat if and only if its [[Yoneda extension]] $Lan_F\colon [C^{op}, Set] \to [E^{op},Set]$ preserves finite limits.

=--
+-- {: .proof}
###### Proof
Since [[presheaf topos]]es have all [[colimit]]s, $F_! = Lan_F$ is computed on any object $e \in E$ (as discussed at [[Kan extension]]) by the [[colimit]]
$$ (F_! X(e) = \lim_{\to} \left( (e/F)^{op} \to C^{op} \stackrel{X}{\to} Set \right) $$
where $(e/F)$ is the corresponding [[comma category]] and $(e/F)^{op} \to C^{op}$ is the canonical projection.

Now, by definition $F$ being representably-flat means that $(e/F)^{op}$ is a [[filtered category]]. So this is a [[filtered colimit]]. By the discussion there, it is precisely the filtered colimits that commute with finite limits.
=--

+-- {: .num_prop}
###### Proposition
When $C$ is [[small category|small]] and $E$ is a cocomplete topos, a functor $F\colon C\to E$ is internally flat if and only if its [[Yoneda extension]] $[C^{op},Set] \to E$ preserves finite limits.
=--
+-- {: .proof}
###### Proof
This is VII.9.1 in [Mac Lane-Moerdijk](#MLM).
=--

If $C$ is a [[site]], $E$ is a sheaf topos, and $F\colon C\to E$ is internally flat, then the restriction of $[C^{op},Set] \to E$ to $Sh(C)$ still preserves finite limits, and it is cocontinuous just when $F$ preserves covering families.  Since cocontinuous left-exact functors between sheaf toposes are precisely the [[inverse image]] parts of [[geometric morphisms]], we conclude that cover-preserving internally-flat functors out of a site $C$ characterise geometric morphisms into $Sh(C)$.  In other words, $Sh(C)$ is the [[classifying topos]] for such functors.  This can be very useful when a [[Grothendieck topos]] has a presentation by a particularly simple site.


### Category of flat functors
 {#CategoryOfFlatFunctors}

For $A$ a [[category]] the [[full subcategory]]

$$
  FlatFunc(A^{op}, Set) \subset Func(A^{op}, Set)
$$

of the [[category of presheaves]] on $A$ 
(which is the [[free cocompletion]] of $A$) on the flat functors is the 
free cocompletion under [[filtered colimits]].  When regarded in this way, flat functors are also known as [[ind-objects]].

+-- {: .num_prop}
###### Proposition

$FlatFunc(A^{op},Set)$ has [[finite limits]] precisely if for every finite [[diagram]] $D$ in $A$, the category of [[cones]] on $D$ is [[filtered category|filtered]].

=--

This is due to ([KarazerisVelebil](#KarazerisVelebil)).


### Classifying toposes and Diaconescu's theorem
  {#DiaconescuTheorem}

The following statement is known as _[[Diaconescu's theorem]]_, see there for more details. It says that the internally flat functors, def. \ref{InternallyFlat} $F \colon C \to \mathcal{E}$ are precisely the [[inverse images]] of [[geometric morphisms]] from $E$ into the [[presheaf topos]] over $C$.

+-- {: .num_theorem}
###### Theorem
**(Diaconescu's theorem)**

There is an [[equivalence of categories]]

$$
  Topos(\mathcal{E}, PSh(C))
   \simeq
  FlatFunc(C, \mathcal{E})
$$

between the category of [[geometric morphisms]] $f : \mathcal{E} \to PSh(C)$ and the category of [[internally flat functors]] $C \to \mathcal{E}$.

This equivalence takes $f$ to the composite

$$
  C \stackrel{j}{\to} PSh(C) \stackrel{f^*}{\to} \mathcal{E}
  \,,
$$

where $j$ is the [[Yoneda embedding]] and $f^*$ is the [[inverse image]] of $f$.

=--

One says that $PSh(C)$ is the _[[classifying topos]]_ for internally flat functors out of $C$.

## Examples

* [[morphism of sites|Morphisms of sites]] are flat functors which additionally preserve covering families.

* [[tensor product of modules]] with a [[flat module]]

## Related concepts

* [[theory of flat functors]]

* [[exact (∞,1)-functor]]

* [[ind-object]]

## References

* [[Francis Borceux]], _Handbook of categorical algebra_ , volume I, _Basic category theory_.  Representable flatness is discussed in chapter 6.
{#Borceux}

In 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ .  
 {#Johnstone}

internally flat functors ("torsors") are discussed around B3.2, and representably flat functors around C2.3.7.

In 

* [[Saunders Mac Lane]] and [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ .  
 {#MLM}

$Set$-valued flat functors are discussed in VII.6, and internally flat functors in VII.8 (both called "filtering functors").

In section 2 of 

* [[Ieke Moerdijk]], _Classifying spaces and classifying topoi_, Lecture Notes in Mathematics __1616__, Springer 1995. vi+94 pp. ISBN: 3-540-60319-0
 {#Moerdijk}

internally flat functors with values in a topos with enough points are discussed.

For the relationship between the various notions of flatness, and the notion of covering-flatness, see

* [[Panagis Karazeris]], _Notions of flatness relative to a Grothendieck topology_, Theory and Applications of Categories, 12 (2004), 225-236 ([TAC](http://www.tac.mta.ca/tac/volumes/12/5/12-05abs.html))
 {#Karazeris}

* [[Mike Shulman]], _[Flat Functors and Morphisms of Sites](http://golem.ph.utexas.edu/category/2011/06/flat_functors_and_morphisms_of.html)_
 {#Shulman}

Limits in the category of flat functors are discussed in 

* [[Panagis Karazeris]], Ji&#345;&#237; Velebil, _Representability relative to a doctrine_ , Cahiers de Topologie et G&#233;ometrie Diff&#233;rentielle Cat&#233;goriques 50 (2009), 3&#8211;22.
 {#KarazerisVelebil}


Discussion of [[left exact functors]] or flat functors in the context of [[(∞,1)-category theory]] is in 

* [[Jacob Lurie]], def. 5.3.2.1 in _[[Higher Topos Theory]]_

A notion of "flat 2-functor" is discussed, with an eye towards applications with [[2-topos]]es, in the article

* M.E. Descotte, E.J. Dubuc, M. Szyld, _On the notion of flat 2-functors_, arXiv:[1610.09429](https://arxiv.org/abs/1610.09429)

[[!redirects flat functor]]
[[!redirects flat functors]]

[[!redirects representably flat functor]]
[[!redirects representably flat functors]]

[[!redirects internally flat functor]]
[[!redirects internally flat functors]]

[[!redirects covering-flat functor]]
[[!redirects covering-flat functors]]