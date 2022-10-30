
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[Andre Joyal|Joyal]]- _[[model category|model structure]] on [[simplicial object|simplicial]] [[sheaves]]_ over a [[site]] is a [[model category]] [[presentable (infinity,1)-category|presentation]] of the [[hypercomplete (∞,1)-topos]] over that site.

It is [[Quillen equivalence|Quillen equivalent]] to the Jardine-local [[model structure on simplicial presheaves]].

There is also a _[[Čech model structure on simplicial sheaves]]_ (see there) modelling not the hypercompletion but just the [[topological localization]] of the [[(∞,1)-category of (∞,1)-presheaves]].


## Definition

Let $C$ be a [[small category|small]] [[site]]. Write $Sh(C)$ for the [[category of sheaves]] on $C$ and $Sh(C)^{\Delta^{op}}$ for the category of [[simplicial object]]s in $Sh(C)$: the category of _simplicial sheaves_ over $C$.

+-- {: .num_theorem }
###### Theorem 

There is a [[left proper model category|left proper]] [[simplicially enriched category|simplicially enriched]] [[model category]] structure on $Sh(C)^{\Delta^{op}}$ such that

* cofibrations are precisely the objectwise cofibrations (monomorphisms) of [[simplicial set]]s;

* weak equivalences are the _local weak equivalences_ of the underlying simplicial presheaves as defined at [[model structure on simplicial presheaves]].

=--

This is ([Jardine, theorem 5](#Jardine)).

Call this the **local injective model structure** on simplicial sheaves.


## Properties


+-- {: .num_theorem }
###### Theorem 

The [[geometric embedding]] of a [[category of sheaves]] into its [[category of presheaves]]

$$
  (L \dashv i) : Sh(C) \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh(C)
$$

with $L$ given by [[sheafification]] extends to a [[Quillen equivalence]]

$$
  (L \dashv i) : Sh(C)^{\Delta^{op}}_{loc} \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh(C)^{\Delta^{op}}_{loc}
$$


between the above local model structure on simplicial sheaves and the injective hyperlocal Jardine-[[model structure on simplicial presheaves]].

=--

This is ([Jardine, theorem 5](#Jardine)).


+-- {: .num_prop #PresentationOfhypercompleteTopos}
###### Proposition

The [[simplicial combinatorial model category]] $Sh(C)^{\Delta^{op}}_{loc}$ is a [[presentable (∞,1)-category|presentation]] for the [[hypercompletion]] $\hat Sh_{(\infty,1)}(c)$ of the [[(∞,1)-category of (∞,1)-sheaves]] on $C$:

$$
  \hat Sh_{(\infty,1)}(C) \simeq (Sh(C)^{\Delta^{op}}_{loc})^\circ
  .
$$

=--

+-- {: .proof}
###### Proof

The proof is spelled out at [[hypercomplete (∞,1)-topos]].

=--

+-- {: .num_cor }
###### Corollary

For $D$ a [[dense sub-site]] of $C$ we have an [[equivalence of (∞,1)-categories]]

$$
  \hat Sh_{(\infty,1)}(C) \simeq \hat Sh_{(\infty,1)}(D)
  \,.

$$

=--

+-- {: .proof}
###### Proof

By the _comparison lemma_ at [[dense sub-site]] we have already an [[equivalence of categories]]


$$
  Sh(C) \simeq Sh(D)
  \,.
$$

This implies the claim with the [above proposition](#PresentationOfhypercompleteTopos).

=--

## Related concepts

* [[Čech model structure on simplicial sheaves]]

* [[model structure on cubical presheaves]]

## References

The local model structure on simplicial sheaves was proposed in

* [[Andre Joyal]], Letter to [[Alexander Grothendieck]], 11.4.1984, ([pdf scan](http://webusers.imj-prg.fr/~georges.maltsiniotis/ps/lettreJoyal.pdf)).

This is with [[BrownAHT]] among the first proposals for models for [[∞-stack]].

A discussion can be found in

* [[Sjoerd Crans]], _Quillen closed model structure for sheaves_,  J. Pure Appl. Algebra  101 (1995), 35-57 ([web](http://home.tiscali.nl/secrans/papers/thcms.html))

Jardine's lectures

* {#Jardine} [[John Frederick Jardine]], _Field Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))


discuss the Quillen equivalence between the model structure on simplicial sheaves and the [[model structure on simplicial presheaves]].


Wendt discusses "the construction of classifying spaces of fibre sequences in model categories of simplicial sheaves" in 

* [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_, [arxiv/1009.2930](http://arxiv.org/abs/1009.2930) 

[[!redirects model structures on simplicial sheaves]]
[[!redirects model structure on the category of simplicial sheaves]]