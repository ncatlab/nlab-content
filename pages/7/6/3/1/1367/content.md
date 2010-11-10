
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

The generalization of the notion of [[functor category]] from [[category theory]] to [[(∞,1)-category|(∞,1)]]-[[higher category theory]].

## Definition

Let $C$ and $D$ be [[(∞,1)-categories]], taken in their incarnation as [[quasi-category|quasi-categories]]. Then

$$
  Func(C,D) := sSet(C,D)
$$

is the [[simplicial set]] of morphisms of simplicial sets between $C$ and $D$ (in the standard [[sSet]]-[[enriched category|enrichment]] of $SSet$):

$$
  sSet(C,D) := [C,D] := ([n] \mapsto Hom_{sSet}(\Delta[n]\times C,D))
  \,.
$$

The objects in $Fun(C,D)$ are the [[(∞,1)-functors]] from $C$ to $D$, the morphisms are the corresponding [[natural transformations]] or [[homotopy|homotopies]], etc.

+-- {: .un_prop }
###### Proposition

The simplicial set $Fun(C,D)$ is indeed a [[quasi-category]].

In fact, for $C$ and $D$ any simplicial sets, $Fun(C,D)$ is a [[quasi-category]] if $D$ is a [[quasi-category]].

=--

+-- {: .proof}
###### Proof

Using that [[sSet]] is a [[closed monoidal category]] the [[horn]] filling conditions

$$
  \array{
    \Lambda[n]_i &\to& [C,D]
    \\
    \downarrow & \nearrow
    \\
    \Delta[n]
  }
$$

are equivalent to 

$$
  \array{
    C \times \Lambda[n]_i &\to& D
    \\
    \downarrow & \nearrow
    \\
    C \times \Delta[n]
  }
  \,.
$$

Here the vertical map is [[fibrations of quasi-categories|inner anodyne]] for inner horn inclusions $\Lambda[n]_i \hookrightarrow \Delta[n]$, and hence the lift exists whenever $D$ has all inner horn fillers, hence when $D$ is a [[quasi-category]].

=--

For the definition of $(\infty,1)$-functors in other models for $(\infty,1)$-categories see [[(∞,1)-functor]].


## Properties

### Models 

The projective and injective [[global model structure on functors]] as well as the [[Reedy model structure]] if $C$ is a [[Reedy category]] [[presentable (infinity,1)-category|presents]] $(\infty,1)$-categories of $(\infty,1)$-functors, at least when there exists a [[combinatorial simplicial model category]] model for the codomain.

Let 

* $C$ be a small [[sSet]]-[[enriched category]];	

* $A$ a [[combinatorial simplicial model category]] and $A^\circ$ 
  its full [[sSet]]-subcategory of fibrant cofibrant objects;

* $[C,A]$ the [[sSet]]-[[enriched functor category]] equipped with either
  the injective or projective [[global model structure on functors]] and
  $[C,A]^\circ$ its full [[sSet]]-[[subcategory]] 
  on fibrant-cofibrant objects.

Write $N : sSet Cat \to sSet$ for the [[homotopy coherent nerve]]. 
Since this is a [[right adjoint]] it preserves [[product]]s and 
hence we have a canonical morphism

$$
  N(C) \times N([C,A]) \simeq
  N(C \times [C,A])
  \stackrel{N(ev)}{\to}
  N(A)
$$

induced from the hom-[[adjunct]] of $Id : [C,A] \to [C,A]$.

The fibrant-cofibrant objects of $[C,A]$ are [[enriched functor]]s that 
in particular take values in fibrant cofibrant objects of $A$. Therefore
this restricts to a morphism

$$
  N(C) \times N([C,A]^\circ) 
  \stackrel{N_{hc}(ev)}{\to}
  N(A^\circ)
  \,.
$$

By the [[internal hom]] [[adjunction]] this corresponds to a morphism

$$
  N([C,A]^\circ) 
  \stackrel{}{\to}
  sSet(N_{hc}(C),  N(A^\circ))
  \,.
$$

Here $A^\circ$ is [[Kan complex]] enriched by the axioms of an $sSet_{Quillen}$- [[enriched model category]], and so $N(A^\circ)$ is a [[quasi-category]], so that we may write this as

$$
  \cdots = Func(N(C), N(A^\circ))
  \,.
$$

+-- {: .un_prop }
###### Proposition

This canonical morphism

$$
  N([C,A]^\circ) 
  \stackrel{}{\to}
  Func(N(C),  N(A^\circ))
$$

is an $(\infty,1)$-equivalence in that it is a weak equivalence in the
[[model structure for quasi-categories]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 4.2.4.4]].

The strategy is to show that the objects on both sides are [[exponential object]]s in the [[homotopy category]] of $sSet_{Joyal}$, hence isomorphic there.

That $Func(N(C), N(A^\circ)) \simeq (N(A^\circ))^{N(C)}$
is an exponential object in the homotopy category is pretty immediate.

That the left hand is an isomorphic exponential follows from [[Higher Topos Theory|HTT, corollary  A.3.4.12]], which asserts that for $C$ and $D$ $sSet$-[[enriched categories]] with $C$ cofibrant and $A$ as above, we have that composition with the evaluation map induces a bijection

$$
  Hom_{Ho(sSet Cat)}(D, [C,A]^\circ)
  \stackrel{\simeq}{\to}
  Hom_{Ho(sSet Cat)}(C \times D, A^\circ)
  \,.
$$

Since $Ho(sSet Cat_{Bergner}) \simeq Ho(sSet_{Joyal})$ this 
identifies also $N([C,A]^\circ)$ with the exponential object in question.

=--

### Limits and colimits {#Limits}

For $C$ an ordinary [[category]] that admits small [[limit]]s and [[colimit]]s, and for $K$ a [[small category]], the [[functor category]] $Func(D,C)$ has all small limits and colimits, and these are computed objectwise. See [[limits and colimits by example]]. The analogous statement is true for $(\infty,1)$-categories of $(\infty,1)$-functors

+-- {: .un_prop}
###### Propositon

Let $K$ and $C$ be [[quasi-categories]], such that $C$ has all [[limit in a quasi-category|colimits]] indexed by $K$. 

Let $D$ be a small quasi-category. Then 

* The $(\infty,1)$-category $Func(D,C)$ has all $K$-indexed colimits;

* A morphism $K^\triangleright \to Func(D,C)$ is a colimiting cocone precisely if for each object $d \in D$ the induced morphism $K^\triangleright \to C$ is a colimiting cocone.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, corollary 5.1.2.3]]

=--



## Examples

* Since the standard [[model structure on simplicial sets]] presents [[? Grpd]] 

  $$
    (sSet_{Quillen})^\circ \simeq \infty Grpd
  $$

  the [[model structure on simplicial presheaves]] (more precisely and more generally the [[model structure on sSet-enriched presheaves]]) on the [[opposite (∞,1)-category]] $C^{op}$ [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category of (∞,1)-presheaves]] on $C$:

  $$
    N([C^{op},sSet_{Quillen}]^\circ) \simeq Func(C^{op},\infty Grpd)
    = PSh_{(\infty,1)}(C)
    \,.
  $$

## Reference

The intrinsic defintiion is in section 1.2.7 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The discussion of [[model category]] models is in A.3.4.


[[!redirects (∞,1)-category of (∞,1)-functors]]
[[!redirects (infinity,1)-functor category]]
[[!redirects functor (infinity,1)-category]]
[[!redirects (∞,1)-functor categories]]
[[!redirects functor (∞,1)-categories]]
[[!redirects (infinity,1)-functor category]]
[[!redirects functor (infinity,1)-category]]
[[!redirects (∞,1)-functor categories]]
[[!redirects functor (∞,1)-categories]]
[[!redirects functor (∞,1)-category]]
