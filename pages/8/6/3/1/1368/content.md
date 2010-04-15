
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Definition ##

For [[∞Grpd]] the [[(∞,1)-category]] of [[∞-groupoids]], and for $S$ a [[(∞,1)-category]] (or in fact any [[simplicial set]]), an **$(\infty,1)$-presheaf** on $S$ is an $(\infty,1)$-functor

$$
  F : S^{op} \to \infty Grpd
  \,.
$$

The **$(\infty,1)$-category of $(\infty,1)$-presheaves** is the [[(∞,1)-category of (∞,1)-functors]]

$$
  PSh_{(\infty,1)}(S) := Func(S^{op}, \infinity Grpd)
  \,.
$$

## Properties

### Models {#Models}

A [[model category|model]] for an $(\infty,1)$-presheaf categories is the [[model structure on simplicial presheaves]]. See also the discussion at [[models for ∞-stack (∞,1)-toposes]].

+-- {: .un_prop}
###### Proposition

For $C$ a [[simplicially enriched category]] with [[Kan complex]]es as hom-objects, write $[C^{op}, sSet_{Quillen}]_{proj}$ and $[C^{op}, sSet_{Quillen}]_{inj}$ for the projective or injective, respectively, gloabl [[model structure on simplicial presheaves]]. Write $(-)^\circ$ for the full [[sSet]]-[[enriched category|enriched]] [[subcategory]] on fibrant-cofibrant objects, and $N(-)$ for the [[homotopy coherent nerve]] that sends a Kan-complex enriched category to a [[quasi-category]]. 

Then there is an [[equivalence of quasi-categories]]

$$
  PSh(N(C))
  \simeq
  N ([C^{op}, sSet_{Quillen}]_{proj})^\circ
  \,.
$$

Similarly for the injective model structure.

=--

+-- {: .proof}
###### Proof

This is a special case of the more general statement that the [[model structure on functors]] models an [[(∞,1)-category of (∞,1)-functors]]. See there for more details.

=--

Notice that the result in particular means that any $(\infty,1)$-presheaf -- an "$\infty$-[[pseudofunctor]]" -- may be _straightened_ or _rectified_ to a genuine [[sSet]]-[[enriched functor]], that respects horizontal compositions strictly.


### Limits and colimits

In an ordinary [[category of presheaves]], [[limit]]s and colimits are computed objectwise, as described at [[limits and colimits by example]]. The analogous statement is true for [[limit in a quasi-category|(∞,1)-limits]] and colimits in an $(\infty,1)$-category of $(\infty,1)$-presheaves.

This is a special case of the general existence of limits and colimits in an [[(∞,1)-category of (∞,1)-functors]]. See there for more details.

+-- {: .un_cor}
###### Corollary

For $C$ a small $(\infty,1)$-category, the $(\infty,1)$-category $PSh(C)$ admits all small limits and colimits.

=--

See around [[Higher Topos Theory|HTT, cor. 5.1.2.4]].

### As the free completion under colimits {#FreeColimCompletion}

An ordinary [[category of presheaves]] on a small category $C$ is the [[free cocompletion]] of $C$, the free completion under forming colimits.

The analogous result holds for $(\infty,1)$-category of $(\infty,1)$-presheaves.


+-- {: .un_lemma}
###### Lemma

Let $C$ be a small [[quasi-category]] and $j : S \to PSh(C)$ the [[(∞,1)-Yoneda embedding]]. 

The identity [[(∞,1)-functor]] $Id : PSh(C) \to PSh(C)$ is the left [[(∞,1)-Kan extension]] of $j$ along itself. 

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, lemma 5.1.5.3]].

=--


For $D$ a [[quasi-category]] with all small [[limit in a quasi-category|colimits]], write  $Func^L(PSh(C),D) \subset Func(PSh(C),D)$ for the full [[sub-quasi-category]] of the [[(∞,1)-category of (∞,1)-functors]] on those that preserve small [[limit in a quasi-category|colimits]].

+-- {: .un_lemma}
###### Lemma

Composition with the Yoneda embedding $j : C \to PSh(C)$ induces an [[equivalence of quasi-categories]]

$$
  Func^L(PSh(C),D) \to Func(C,D)
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, theorem 5.1.5.6]].

=--


In terms of the model given by the [[model structure on simplicial presheaves]], this is statement made in 

* [[Dan Dugger]], _[[Universal homotopy theories]]_ ,

which gives that article its name.

+-- {: .un_def}
###### Definition

Let $A$ and $B$ be [[model categories]], $D$ a plain [[category]] and

$$
  \array{
    D &\stackrel{r}{\to}& A
    \\
    & \searrow_\gamma 
    \\
    && B
  }
$$

two plain [[functor]]s. Say that a **model-category theoretic factorization** of $\gamma$ through $A$ is 

1. a [[Quillen adjunction]] $(L \dashv R) : A \stackrel{\overset{L}{\to}}{\underset{R}{\leftarrow}} B$

1. a [[natural transformation|natural]] weak equivalence $\eta  : L \circ r \to \gamma$

   $$
     \array{
       D &&\stackrel{r}{\to}&& A
       \\
       & \searrow_\gamma &{}^\eta\swArrow& \swarrow_L
       \\
       && B
     }
     \,.
   $$

Let the [[category]] of such factorizations have morphisms $((L \dashv R), \eta ) \to ((L' \dashv R'), \eta' )$ given by [[natural transformation]]s $L \to L'$ such that for all all objects $d \in D$ the diagrams

$$
  \array{
     L\circ r(d) &&\to&& L'\circ r(d)
     \\
     & {}_{\eta_{d}}\searrow && \swarrow_{\eta'_{d}}
     \\
     &&
     \gamma()
  }
$$

commutes.

=--

Notice that the [[(∞,1)-category]] presented by a [[model category]] -- at least by a [[combinatorial model category]] -- has all [[limit in a quasi-category|(∞,1)-categorical colimits]], and that the Quillen left adjoint functor $L$ presents, via its [[derived functor]], a left [[adjoint (∞,1)-functor]] that preserves $(\infty,1)$-categorical colimits. So the notion of factorization as above is really about factorizations through colimit-preserving $(\infty,1)$-functors into $(\infty,1)$-categories that have all colimits.

+-- {: .un_theorem}
###### Theorem
**(model category presentation of free $(\infty,1)$-cocompletion)**

For $C$ a [[small category]], the projective global [[model structure on simplicial presheaves]] $[C^{op}, sSet]_{proj}$ on $C$ is universal with respect to such factorizations of functors out of $C$:

every functor $C \to B$ to any [[model category]] $B$ has a factorization through $[C^{op}, sSet]_{proj}$ as above, and the category of such factorizations is [[contractible]].

=--

+-- {: .proof}
###### Proof

This is theorem 1.1 in

* [[Dan Dugger]], _[[Universal homotopy theories]]_

=--



+-- {: .un_cor}
###### Corollary

The [[(∞,1)-Yoneda embedding]] $j : C \to PSh(C)$ generates $PSh(C)$ under small colimits:

a full [[sub-quasi-category|(∞,1)-subcategory]] of $PSh(C)$ that contains all representables and is closed under forming $(\infty,1)$-colimits is already equivalent to $PSh(C)$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, corollary 5.1.5.8]].

=--



## $(\infty,1)$-subcategories of $(\infty)$-presheaf categories

### Locally presentable $(\infty,1)$-categories

A [[reflective (∞,1)-subcategory]] of an $(\infty,1)$-category of $(\infty,1)$-presheaves is called a [[presentable (∞,1)-category]].

### $(\infty,1)$-Sheaf $(\infty,1)$-categories

If that [[left adjoint|left]] [[adjoint (∞,1)-functor]] to the embedding of the [[reflective (∞,1)-subcategory]] furthermore preserves finite [[limit]]s, then the subcategory is an [[(∞,1)-category of (∞,1)-sheaves]]: an [[(∞,1)-topos]]


## References ##

This is the topic of section 5.1 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects (∞,1)-category of (∞,1)-presheaves]]
[[!redirects free (∞,1)-cocompletion]]
[[!redirects free (infinity,1)-cocompletion]]