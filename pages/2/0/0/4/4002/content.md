
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Connected topos
* table of contents
{: toc}

## Idea

If we view a (Grothendieck) [[topos]] as a generalized [[topological space]], then a *connected topos* is a generalization of a [[connected topological space]].

More generally, a *connected geometric morphism* $p\colon E\to F$ is a "relativized" notion of this, saying that $E$ is "connected as a topos over $F$."

## Definition

A [[geometric morphism]] $p\colon E\to F$ is **connected** if its inverse image part $p^*$ is [[fully faithful functor|full and faithful]].

A [[Grothendieck topos]] $E$ is **connected** if the unique geometric morphism $E \to Set = Sh(*)$ is connected.  If $E$ is the [[topos of sheaves]] on a [[topological space]] $X$ (or more generally a [[locale]]), then this is equivalent to the usual definition of connectedness for $X$ (see C1.5.7 in the [[Elephant]]).

## Connected locally connected morphisms

For geometric morphisms which are also [[locally connected geometric morphism|locally connected]], connectedness can be phrased in an especially nice form.

+-- {: .un_prop}
###### Proposition
If $p\colon E\to F$ is locally connected, then it is connected if and only if the left adjoint $p_!$ of the inverse image functor (which exists, since $p$ is locally connected) preserves the terminal object.
=--
+-- {: .proof}
###### Proof
On the one hand, if $p^*$ is fully faithful, then the counit $p_! p^* \to \Id$ is an isomorphism, so we have $p_!(*) \cong p_!(p^*(*)) \cong *$; hence $p_!$ preserves the terminal object.

On the other hand, suppose that $p_!$ preserves the terminal object.  Suppose also for simplicity that $F=Set$.  Then any set $A$ is the [[coproduct]] $\coprod_A *$ of $A$ copies of the terminal object.  But $p^*$ and $p_!$ both preserve coproducts (since they are left adjoints) and terminal objects (since $p^*$ is left exact, and by assumption for $p_!$), so we have
$$
p_!(p^*(A)) \cong p_!(p^*(\coprod_A *)) \cong \coprod_A p_!(p^*(*)) \cong \coprod_A * \cong A
$$
Thus, the counit $p_! p^* \to \Id$ is an isomorphism, so $p^*$ is fully faithful.

When $F$ is not $Set$, we just have to replace ordinary coproducts with "$F$-indexed coproducts," regarding $E$ and $F$ as $F$-[[indexed category|indexed categories]].

(This is C3.3.3 in the [[Elephant]].)
=--

Strengthenings of this condition include
* a [[strongly connected geometric morphism]], which is locally connected such that $p_!$ preserves all finite products, and
* a [[totally connected geometric morphism]], which is locally connected such that $p_!$ preserves all finite limits.


## Connected locally connected sites

+--{: .un_prop}
###### Proposition
If $C$ is a [[locally connected site]] with a [[terminal object]], then the [[topos of sheaves]] $Sh(C)$ on $C$ is (not just locally connected) but connected.
=--
+--{: .proof}
###### Proof
As explained at [[locally connected site]], when $C$ is locally connected, the left adjoint $\Pi_0\colon Sh(C) \to Set$ is simply obtained by taking [[colimits]] over $C^{op}$.  Now by the [[co-Yoneda lemma]], the [[colimit]] over any [[representable presheaf]] is a [[singleton]] (i.e. a terminal object in [[Set]]):

$$
  \lim_\to y(V) = \int^{U \in C} C(U,V) = \int^{U \in C} C(U,V) \cdot * = *
  \,.
$$ 

But if $C$ has a terminal object, then that terminal object represents the terminal presheaf, which is also the terminal presheaf.  Hence under these conditions, $\Pi_0$ preserves the terminal object, so $Sh(C)$ is connected.
=--

## Orthogonality

+--{: .un_prop}
###### Proposition
Connected geometric morphisms are left [[orthogonal]] to [[etale geometric morphisms]] in the [[2-category]] [[Topos]].
=--
+--{: .proof}
###### Proof
Since the functor $Topos^{op} \to Cat$ sending a topos to itself and a geometric morphism to its [[inverse image functor]] is 2-fully-faithful (an [[equivalence of categories|equivalence]] on [[hom-categories]]), connected morphisms are representably [[fully faithful morphism|co-fully-faithful]] in $Topos$.

Therefore, for 2-categorical orthogonality it suffices to show that in any commutative (up to iso) square
$$
  \array{ 
    A & \xrightarrow{f} & B 
    \\ 
    {}^{\mathllap{p}}\downarrow & & \downarrow^{\mathrlap{q}} 
    \\ 
    C & \xrightarrow{g} & D}
$$
of geometric morphisms in which $p$ is connected and $q$ is etale, there exists a filler $h\colon C\to B$ such that $h p \cong f$ and $q h \cong g$.

However, if $X\in D$ is such that $B \cong D/X$ (such exists by definition of $q$ being etale), then for any topos $E$ equipped with a geometric morphism $k\colon E\to D$, lifts of $k$ along $q$ are equivalent to morphisms $* \to k^*(X)$ in $C$.  In particular, $f$ is determined by a map $*\to f^*(q^*(X)) \cong p^*(g^*(X))$, and since $* \cong p^*(p_*(*))$ and $p^*$ is fully faithful, this map comes from a map $*\to g^*(X)$ in $C$, which in turn determines a geometric morphism $h\colon C\to B$ which is the desired filler.
=--

+--{: .un_prop}
###### Proposition
Any locally connected geometric morphism factors as a connected and locally connected geometric morphism followed by an etale one.
=--
+--{: .proof}
###### Proof
Given $f\colon E\to S$ locally connected, we can factor it as $E \to S/f_!(*) \to S$.  The second map is etale by definition, while the first is locally connected (the left adjoint is essentially $f_!$ again) and connected since it preserves the terminal object (by construction).
=--

In particular:

* (Connected, Etale) is a [[factorization system in a 2-category|factorization system]] on the 2-category $LCTopos$ of toposes and locally connected geometric morphisms.

* The category of etale geometric morphisms over a base topos $S$, which is equivalent to $S$ itself, is a [[reflective subcategory]] of the [[slice 2-category]] $LCTopos/S$.  The [[reflector]] constructs "$\Pi_0$ of a locally connected topos."

These results all have generalizations to [[∞-connected (∞,1)-toposes]].

## Examples

* The [[gros topos|gros]] [[sheaf topos]] $Sh(CartSp)$ on the [[nLab:site]] [[CartSp]] -- which contains the [[quasi-topos]] of [[diffeological space]] -- is a connected topos, since the site [[CartSp]] is a locally connected site and contains a terminal object.


## Related concepts

* [[essential geometric morphism]]

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* **connected topos** / [[∞-connected (∞,1)-topos]]

* [[totally connected topos]] / [[totally connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]



[[!redirects connected topoi]]
[[!redirects connected toposes]]
[[!redirects connected locally connected topos]]
[[!redirects connected locally connected topoi]]
[[!redirects connected locally connected toposes]]
[[!redirects connected geometric morphism]]
[[!redirects connected geometric morphisms]]
[[!redirects connected locally connected geometric morphism]]
[[!redirects connected locally connected geometric morphisms]]
