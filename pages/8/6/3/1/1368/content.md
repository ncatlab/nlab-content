
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
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

For $C$ a [[simplicially enriched category]] with [[Kan complex]]es as hom-objects, write $[C^{op}, sSet_{Quillen}]_{proj}$ and $[C^{op}, sSet_{Quillen}]_{inj}$ for the projective or injective, respectively, global [[model structure on simplicial presheaves]]. Write $(-)^\circ$ for the full [[sSet]]-[[enriched category|enriched]] [[subcategory]] on fibrant-cofibrant objects, and $N(-)$ for the [[homotopy coherent nerve]] that sends a Kan-complex enriched category to a [[quasi-category]]. 

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

Let $C$ be a small [[quasi-category]] and $j \colon S \to PSh(C)$ the [[(∞,1)-Yoneda embedding]]. 

The identity [[(∞,1)-functor]] $Id \,\colon\, PSh(C) \to PSh(C)$ is the left [[(∞,1)-Kan extension]] of $j$ along itself. 

=--

This is [[Higher Topos Theory|HTT, lemma 5.1.5.3]].


For $D$ a [[quasi-category]] with all small [[limit in a quasi-category|colimits]], write  $Func^L(PSh(C),D) \subset Func(PSh(C),D)$ for the full [[sub-quasi-category]] of the [[(∞,1)-category of (∞,1)-functors]] on those that [[preserved colimit|preserve]] small [[limit in a quasi-category|colimits]].

+-- {: .un_lemma}
###### Lemma

Pre-composition with the Yoneda embedding $j \colon C \to PSh(C)$ induces an [[equivalence of quasi-categories]]

$$
  Func^L(PSh(C),D) \to Func(C,D)
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, theorem 5.1.5.6]].

In terms of the model given by the [[model structure on simplicial presheaves]], this is statement made in [Dugger (2001)](#Dugger2001), which gives that article its name.

+-- {: .un_def}
###### Definition

Let $A$ and $B$ be [[model categories]], $D$ a plain [[category]] and

$$
  \array{
    D &\overset{r}{\longrightarrow}& A
    \\
    &  \mathllap{{}_{\gamma}}\searrow 
    \\
    && B
  }
$$

two plain [[functors]]. Say that a **model-category theoretic factorization** of $\gamma$ through $A$ is 

1. a [[Quillen adjunction]] $(L \dashv R) : A \stackrel{\overset{L}{\to}}{\underset{R}{\leftarrow}} B$

1. a [[natural transformation|natural]] weak equivalence $\eta  : L \circ r \to \gamma$

   $$
     \array{
       D &&\stackrel{r}{\to}&& A
       \\
       & \mathllap{{}_\gamma}\searrow 
         &{}^\eta\swArrow
       & \swarrow_{\mathrlap{L}}
       \\
       && B
     }
     \,.
   $$

Let the [[category]] of such factorizations have morphisms $\big((L \dashv R), \eta \big) \to \big((L' \dashv R'\big), \eta' )$ given by [[natural transformation]]s $L \to L'$ such that for all all objects $d \in D$ the diagrams

$$
  \array{
     L\circ r(d) &&\longrightarrow&& L'\circ r(d)
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

This is [Dugger (2001), theorem 1.1](#Dugger2001), 
where the proof appears on page 30.


+-- {: .proof}
###### Proof

To produce the factorization $[C^{op},sSet] \to B$ given the functor $\gamma$, first
notice that the ordinary [[Yoneda extension]] $[C^{op},Set] \to B$ would be given by the left [[Kan extension]] given by the [[coend]] formula

$$
  F \mapsto \int^{c \in C} \gamma(c) \cdot F(c)
  \,,
$$

where the dot in the integrand is the [[copower|tensoring]] of cocomplete category $B$ over [[Set]]. To refine this to a [[Quillen adjunction|left Quillen functor]] $L : [C^{op},sSet] \to B$, _choose_ a [[cosimplicial object|cosimplicial]] [[resolution]]

$$
  \Gamma \;\colon\; C \to [\Delta,B]
$$

of $\gamma$. Then set

$$
  L \;\colon\; 
  F \mapsto 
  \int^{c \in C} 
  \int^{[n] \in \Delta}
  \Gamma^n(c) \cdot F_n(c)
  \,.
$$

The [[right adjoint]] $R \colon B \to [C^{op},sSet]$ of this functor is given by

$$
  R(X) \colon c \mapsto Hom_B(\Gamma^\bullet(c), X)
  \,.
$$

For $(L \dashv R) \colon [C^{op}, sSet]_{proj} \stackrel{\to}{\leftarrow} B$ to be a [[Quillen adjunction]], it is  sufficient to check that $R$ preserves [[fibrations]] and [[acyclic fibrations]]. By definition of the projective model structure this means that for every (acyclic) fibration $b_1 \to b_2$ in $B$ we have for every object $c \in C$ that that

$$
  Hom_C\big(\Gamma^\bullet(c), b_1 \to b_2\big)
$$

is an (acyclic) fibration of simplicial sets. But this is one of the standard properties of [[cosimplicial object|cosimplicial [[resolutions]].

Finally, to find the natural weak equivalence $\eta \colon L \circ j \simeq \gamma$, write $j : C \to [C^{op},sSet]$ for the [[Yoneda embedding]] and notice that by [[Yoneda reduction]] it follows that for $x \in C$ we have

$$
  L(j(x))
  \;=\;
  \int^{c \in C} \int^{[n] \in \Delta}
  \Gamma^n(c) \cdot C(c,x)
  \;=\;
  \Gamma^0(x)
$$
(where equality signs denote [[isomorphisms]]).

By the very definition of cosimplicial resolutions, there is a natural weak equivalence $\Gamma(x) \stackrel{\simeq}{\to}$. We can take this to be the component of $\eta$.

=--



+-- {: .un_cor}
###### Corollary

The [[(∞,1)-Yoneda embedding]] $j \colon C \to PSh(C)$ generates $PSh(C)$ under small colimits:

a full [[sub-quasi-category|(∞,1)-subcategory]] of $PSh(C)$ that contains all representables and is closed under forming $(\infty,1)$-colimits is already equivalent to $PSh(C)$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, corollary 5.1.5.8]].

=--


### Functorality
 {#Functoriality}

The two descriptions of $PSh(S)$ as the functor category $Func(S^{op}, \infty Grpd)$ and as the free cocompletion $S \to PSh(S)$ ([above](#FreeColimCompletion)) both extend to contravariant and covariant [[(infinity,1)-functors|functors]] on [[(infinity,1)Cat|$(\infty, 1)Cat$]].

These two constructions are related.

$Func(-, \infty Grpd) \colon (\infty, 1)Cat^{op} \to (\infty, 1)\widehat{Cat}$ takes values in the subcategory of [[presentable (∞,1)-categories]] and functors [[preserved colimit|preserving]] [[small limit|small]] [[(infinity,1)-limit|limits]] and [[(infinity,1)-colimit|colimits]], and thus having [[left adjoint|left]] and [[right adjoint|right]] [[adjoint (infinity,1)-functor|adjoints]].

Let $Pr^L(\infty,1)Cat$ be the (∞,1)category of [[presentable (∞,1)-categories]] and functors that are left adjoints,
and similarly for $Pr^R(\infty,1)Cat$.


+-- {: .un_theorem}
###### Theorem

The [[adjoint (infinity,1)-functor#category_of_adjunctions|local left adjoint]]
to $Func(-, \infty Grpd) \colon (\infty, 1)Cat^{op} \to Pr^R(\infty,1)Cat$
is naturally equivalent to the free cocompletion functor $P \colon (\infty, 1)Cat \to Pr^L(\infty,1)Cat$
by a natural equivalence whose components at a small (∞,1)-category $S$ are homotopic to the [[identity functor]] on $PSh(S)$.

=--

+-- {: .proof}
###### Proof

Consider the (∞,1)-category of possibly large (∞,1)-categories that have small colimits, and functors preserving small colimits. By [[Higher Topos Theory|HTT, 5.3.6.10]], the inclusion into the full (∞,1)-category of (∞,1)-categories has a left adjoint $P$, which is characterized by the natural equivalence
$$
  Func^L\big(P(S), -\big) \simeq Func(S, -)
$$
given by pre-composition with the [[(infinity,1)-Yoneda embedding|Yoneda embedding]].

Let $Func(-, \infty Grpd)^{ladj}$ denote the [local left adjoint](adjoint+infinity1-functor#LadjAndRadj) to $Func(-, \infty Grpd)$.
Then for $C \in Pr^L(\infty,1)Cat$
and $S \in (\infty,1)Cat$, there are natural equivalences
$$
  \begin{aligned}
  Func^L\big(Func(S^{op}, \infty Grpd)^{ladj}, C\big)
  &\simeq Func^R\big(C^{radj}, Func(S^{op}, \infty Grpd)\big)^{op}
  \\ &\simeq Func\big(S^{op}, Func^R(C^{radj}, \infty Grpd)\big)^{op}
  \\&\simeq Func\big(S, Func^L(\infty Grpd, C)\big)
  \\&\simeq Func(S, C)
  \end{aligned}
$$
The second equivalence holds because, for presentable $C$, the property of being in $Func^R$ is characterized by being accessible and preserving small limits, which can be determined pointwise.

The first and third equivalences are general properties of [local left adjoints](adjoint+infinity1-functor#LadjAndRadj) and opposite functor categories.

The last equivalence is because $Func^L(\infty Grpd, C) \simeq Func(1, C)$. 

Since both constructions corepresent the same functor $Func(S, -)$, the yoneda lemma ensures there is a natural equivalence $ P(S) \simeq Func(S^{op}, \infty Grpd)^{ladj} $.

Now consider the chain of equivalences

$$
  Func(S, C)
  \leftarrow Func^L\big(Func(S^{op}, \infty Grpd)^{ladj}, C\big)
  \to Func^L\big(P(S), C\big)
  \to Func(S, C)
  \mathrlap{\,,}
$$

where the first map is inverse to composition with the Yoneda embedding, the second map is the equivalence constructed previously, and the third map is composition with the Yoneda embedding.

Be careful to note that the first equivalence has not yet been shown to be natural in $S$.

The overall composite is essentially uniquely determined by an automorphism of $\alpha_S$ of $S$. It remains to be shown that  $\alpha_S$ is an identity.

When $S = \Delta^n$, $S$ has no nontrivial automorphisms, so 
$\alpha_{\Delta^n}$ is the identity.

For a functor $\phi : \Delta^n \to S$. The naturality of the above equivalence gives a commutative square

\begin{tikzcd}
  P(\Delta^n) \arrow[r] \arrow[d] &
  \mathrm{Func}(\Delta^{op}, \infty \mathrm{Grpd})^{ladj} \arrow[d]
  \\ P(S) \arrow[r] &
  \mathrm{Func}(S^{op}, \infty \mathrm{Grpd})^{ladj}
\end{tikzcd}


[[Higher Topos Theory|HTT, 5.2.6.3]] asserts $P(\phi)$ is left adjoint to $\Func(\phi, \infty Grpd)$, so the left and right arrows are homotopic. 

We've already seen the top arrow is homotopic to the identity, and so we infer $\alpha_S \phi \simeq \phi$. Since the $\Delta^n$ generate $(\infty,1)Cat$, $\alpha_S$ is thus homotopic to the identity.

=--

Note that a natural automorphism of either functor extending $PSh$ would induce a natural automorphism of the identity functor on $(\infty,1)Cat$. By [[Higher Topos Theory|HTT, 5.2.9.1]], the space of such automorphisms is contractible.





### Relation to slicing
  {#WithOvercategories}

The following analog of the corresponding result for
1-[[categories of presheaves]] holds for $(\infty,1)$-presheaves. See [[functors and comma categories]].

+-- {: .num_prop #SlicingCommutesWithFormingPresheaves}
###### Proposition
**(slicing commutes with passing to presheaves)**

Let $\mathcal{C}$ be a [[small (∞,1)-category]] and 
$p \colon \mathcal{K} \to \mathcal{C}$ a [[diagram]]. 

Write $\mathcal{C}_{/p}$  and $PSh_\infty(\mathcal{C})/_{y p}$
for the corresponding [[over quasi-category|over categories]], where 
$y \colon \mathcal{C} \to PSh_\infty(\mathcal{C})$ is the [[(∞,1)-Yoneda embedding]].

Then we have an [[equivalence of quasi-categories|equivalence of (∞,1)-categories]]

$$
  PSh_\infty(\mathcal{C}_{/p}) 
    \stackrel{\simeq}{\to} 
  PSh_\infty(\mathcal{C})_{/y p}
  \,.
$$

=--


This appears as [[Higher Topos Theory|HTT, 5.1.6.12]].




## $(\infty,1)$-subcategories of $(\infty)$-presheaf categories

### Locally presentable $(\infty,1)$-categories

A [[reflective (∞,1)-subcategory]] of an $(\infty,1)$-category of $(\infty,1)$-presheaves is called a [[presentable (∞,1)-category]].

### $(\infty,1)$-Sheaf $(\infty,1)$-categories

If that [[left adjoint|left]] [[adjoint (∞,1)-functor]] to the embedding of the [[reflective (∞,1)-subcategory]] furthermore preserves finite [[limit]]s, then the subcategory is an [[(∞,1)-category of (∞,1)-sheaves]]: an [[(∞,1)-topos]]


## Related concepts

[[!include locally presentable categories - table]]


## References ##

* {#Dugger01} [[Dan Dugger]], *[[Universal homotopy theories]]*, Advances in Mathematics **164** (2001) 144-176 &lbrack;[arXiv:math/0007070](https://arxiv.org/abs/math/0007070), [doi:10.1006/aima.2001.2014](https://doi.org/10.1006/aima.2001.2014)&rbrack;

* {#Lurie09} [[Jacob Lurie]], section 5.1 in: _[[Higher Topos Theory]]_, Annals of Mathematics Studies **170**, Princeton University Press (2009) &lbrack;[pup:8957](https://press.princeton.edu/titles/8957.html)&rbrack;




[[!redirects (infinity,1)-categories of (infinity,1)-presheaves]]

[[!redirects (∞,1)-category of (∞,1)-presheaves]]
[[!redirects (∞,1)-categories of (∞,1)-presheaves]]

[[!redirects free (∞,1)-cocompletion]]
[[!redirects free (infinity,1)-cocompletion]]

[[!redirects (∞,1)-presheaf (∞,1)-topos]]
[[!redirects (∞,1)-presheaf (∞,1)-toposes]]


[[!redirects (infinity,1)-presheaf (infinity,1)-category]]
[[!redirects (∞,1)-presheaf (∞,1)-category]]
[[!redirects (infinity,1)-presheaf (infinity,1)-categories]]
[[!redirects (∞,1)-presheaf (∞,1)-categories]]

[[!redirects infinity-category of infinity-presheaves]]
[[!redirects infinity-categories of infinity-presheaves]]

[[!redirects infinity1-category of infinity1-presheaves]]
[[!redirects infinity1-categories of infinity1-presheaves]]

