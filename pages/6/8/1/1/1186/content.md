
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

The notion of _locally presentable $(\infty,1)$-category_ is the analog in [[(∞,1)-category]] theory of [[locally presentable category]] in ordinary [[category theory]]:

There is a wealth of equivalent ways to make precise what this means, which are listed below. Two simple ones are:

a locally presentable $(\infty,1)$-category $C$ is precisely

* a [[reflective (∞,1)-subcategory]] of an [[(∞,1)-category of (∞,1)-presheaves]] 

  $$
    C \stackrel{\leftarrow}{\hookrightarrow} PSh_{(\infty,1)}(K)
    \,;
  $$

  such that the inclusion functor is an [[accessible (∞,1)-functor]].

* equivalent to the full subcategory $A^\circ$ of a [[combinatorial simplicial model category]] $A$ on fibrant-cofibrant objects 

  (where the [[Kan complex]]-[[enriched category|enriched]] $A^\circ$ is regarded as an $(\infty,1)$-category, for instance as a [[quasi-category]] after applying the [[homotopy coherent nerve]]).

If the [[left adjoint|left]] [[adjoint (∞,1)-functor]] to the [[full and faithful (∞,1)-functor]] $C \hookrightarrow PSh_{(\infty,1)}(C)$ also preserves finite [[limit]]s, then the locally presentable $C$ is an [[(∞,1)-topos]].


**Warning on terminology.** In [[Higher Topos Theory|HTT]] -- where the notion has been introduced -- the term _presentable $(\infty,1)$-category_ is used for what we call a _locally presentable $(\infty,1)$-category_ here, in order to be in line with the established terminology in ordinary [[category theory]]. 


### Presentation by simplicial model categories {#PresentationBySimpModCat}

Presentable $(\infty,1)$-categories are precisely those [[(∞,1)-categories]] which are _presented_ by a [[combinatorial simplicial model category]] $C$ in that they are the full [[simplicially enriched category|simplicial subcategory]] $C^\circ \hookrightarrow C$ on fibrant-cofibrant objects of $C$ 

(Or, equivalently, the [[quasi-category]] associated to this [[simplicially enriched category]]).

Under this presentation,
equivalence of presentable $(\infty,1)$-categories corresponds precisely
to spans of [[Quillen equivalence]]s between presenting
[[combinatorial simplicial model category|combinatorial simplicial model categories]].

$C^\circ$ and $D^\circ$ are equivalent as $(\infty,1)$-categories precisely
if there exists a chain of simplicial Quillen equivalence

$$
  C 
  \stackrel{\leftarrow}{\to}
  \stackrel{\to}{\leftarrow}
  \stackrel{\leftarrow}{\to}
  \cdots  
  D.
$$

This is remark A.3.7.7 in [[Higher Topos Theory|HTT]].

Partly due to the fact that [[simplicial model category|simplicial model categories]] have been studied for a longer time -- partly because they are simply more tractable -- than [[(∞,1)-categories]], many $(\infty,1)$-categories are indeed handled in terms of such a presentation by a [[simplicial model category]]. 

The canonical example is the presentation of the [[(∞,1)-category of (∞,1)-sheaves]] on an ordinary (1-categorical) [[site]] $S$ by the simplicial [[model structure on simplicial presheaves|model category of simplicial presheaves]] on $S$.


### Presentation by conglomerates of objects in a small $(\infty,1)$-category 

From another perspective, the notion of a presentable [[(∞,1)-category]] is a means to handle [[large category|large]] $(\infty,1)$-categories in terms of small ones.
It is is a slight refinement of the notion of an [[accessible (∞,1)-category]].

A _presentable_ $(\infty,1)$-category is one which may be [[large category|large]], but can entirely be _presented_ as an $(\infty,1)$-category of "conglomerates of objects" in a small $(\infty,1)$-category -- precisely: that it is [[accessible (infinity,1)-category|accessible]] but also admits all small [[limit in quasi-categories|colimits]].

This means that it is desireable to get hold of presentable $(\infty,1)$-categories. The following long list of equivalent definitions allows for many equivalent characterization of presentable $(\infty,1)$-categories. In particular, all [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-categories of (∞,1)-sheaves]] are presentable.

## Definition 

### Locally presentable $(\infty,1)$-category

+-- {: .un_defn}
###### Definition


An [[(∞,1)-category]] $C$ is called **locally presentable** 
if it is [[accessible (infinity,1)-category|accessible]] and admits small [[limit in quasi-categories|colimits]].

=--

+-- {: .un_prop}
###### Proposition

That $C$ is locally presentable is equivalent to each of the following characterizations.

* $C$ is the [[localization of an (∞,1)-category|localization]] of an [[(∞,1)-category of (∞,1)-presheaves]]:

  there exists a small $(\infty,1)$-category $D$ and a functor $f: PSh(D) \to C$ from the [[(infinity,1)-presheaf|(∞,1)-category of (∞,1)-presheaves]] on $D$ with a [[(infinity,1)-fully faithful functor|fully faithful]] [[right adjoint]].

  * (if in addition $f$ is left [[exact functor|exact]] then $C$ is an [[(∞,1)-category of (∞,1)-sheaves]] on $D$)


* there exists a [[combinatorial simplicial model category]] $A$ and (with $C$ incarnated as a [[quasi-category]]) an equivalence $ C \simeq N(A^\circ)$ of $C$ with the [[homotopy coherent nerve]] of the full [[sSet]]-[[enriched category|enriched]] [[subcategory]] of $A$ on fibrant and cofirant objects.


* $C$ is [[accessible (infinity,1)-category|accessible]] and for every [[cardinal number|regular cardinal]] $\kappa$ the full subcategory $C^\kappa$ (...explanation to be filled in...) admits $\kappa$-small [[limit in quasi-categories|colimits]];


* there exists a [[cardinal number|regular cardinal]] $\kappa$ such that $C$ is $\kappa$-[[accessible (infinity,1)-category|accessible]] and $C^\kappa$ ([explanation]()) admits $\kappa$-small [[limit in quasi-categories|colimits]];

* there exists a [[cardinal number|regular cardinal]] $\kappa$, a small $(\infty,1)$-category $D$ with $\kappa$-small [[limit in quasi-categories|colimits]] and an equivalence $Ind_\kappa D \stackrel{\simeq}{\to} D$ of $D$ with the category of $\kappa$-[[ind-object]]s of $D$;

* $C$ is [[locally small (infinity,1)-category|locally small]], admits small colimits, and there exists a [[cardinal number|regular cardinal]] $\kappa$ and a small [[set]] $Cmptcs$ of $\kappa$-[[compact object in an (infinity,1)-category|compact object]]s of $C$ such that every object in $C$ is a [[limit in quasi-categories|colimit]] of a small diagram in the full subcategory on $Cmpcts$.

=--

The equivalent $(\infty,1)$-categorical characterizations are originally due to [[Carlos Simpson]]. The whose theorem appears as [[Higher Topos Theory|HTT, theorem 5.5.1.1]].

That [[localization of an (infinity,1)-category|localizations]] $C \stackrel{\leftarrow}{\hookrightarrow} PSh_{(\infty,1)}(K)$ correspond to combinatorial simplicial model categories is essentially **[Dugger's theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#DuggerTheorem)**: every [[combinatorial model category]] arises, up to Quillen equivalence, as the left [[Bousfield localization of model categories|left Bousfield localization]] of the global projective [[model structure on simplicial presheaves]].

* [[Dan Dugger]], _[[Combinatorial model categories have presentations]]_



### The $(\infty,1)$-category of presentable $(\infty,1)$-categories 

Locally presentable $(\infty,1)$-categories have a number of nice
properties, and therefore it is of interest to consider as
morphisms between them only those [[(∞,1)-functor]]s that preserve
these properties. It turns out that it is useful to consider
_[[limit in a quasi-category|colimit]] preserving_ functors. By the [[adjoint (∞,1)-functor theorem]] these are precisely the functors that have a right [[adjoint (∞,1)-functor]].

+-- {: .un_defn}
###### Definition

Write [[Pr(∞,1)Cat]] $\subset$ [[(∞,1)Cat]] for the (non-full) [[sub-quasi-category|sub-(∞,1)-category]] of [[(∞,1)Cat]] (the collection of not-necessarily small $(\infty,1)$-categories) on

* those objects that are locally presentable $(\infty,1)$-categories;

* those morphisms that are colimit-preserving [[(∞,1)-functor]]s.

=--

This is [[Higher Topos Theory|HTT, def. 5.5.3.1]].


This $(\infty,1)$-category $Pr(\infty,1)Cat$ in turn as special properties. More on that is at [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]].




## Properties

### Limits and colimits {#LimitsAndColimits}

In the first definition of locally presentable $(\infty,1)$-category above only the existence of colimits is postulated. An important fact is that it follows automatically that also all small limits exist:

A [[representable functor]] $C^{op} \to \infty Grpd$ preserves [[limit in a quasi-category|limits]] (see [[(∞,1)-Yoneda embedding]]). If $C$ is locally presentable, then also the converse holds:

+-- {: .un_prop}
###### Proposition

If $C$ is a locally presentable $(\infty,1)$-category then an [[(∞,1)-functor]] $C^{op} \to \infty Grpd$ is a [[representable functor]]
precisely if it preserves [[limit in a quasi-category|limits]].


=--

This is [[Higher Topos Theory|HTT, prop. 5.5.2.2]].

+-- {: .proof}
###### Proof


We need to prove that a limit-preserving functor $F : C^{op} \to \infty Grpd$ is [[representable functor|representable]]. By the above characterizations we know that $C$ is an accessible localization of a presheaf category.

So consider first the case that $C = PSh(D)$ _is_ a presheaf category.  Write

$$
  f : D^{op} \stackrel{j^{op}}{\to} PSh(D)^{op} \stackrel{F}{\to} \infty Grpd
$$

for the precomposition of $F$ with the [[(∞,1)-Yoneda embedding]]. Then let

$$
  F' := Hom_{C}(-,f) : PSh(D)^{op} \to \infty Grpd
$$

the functor represented by $f$. 

We claim that $F \simeq F'$, which proves that $F$ is represented by $F \circ j^{op}$: since both $F$ and $F'$ preserve limits (hence colimits as functors on $PSh(D)$) it follows from the fact that the Yoneda embedding exhibits the universal co-completion of $D$ that it is sufficient to show that $F \circ j^{op} \simeq F' \circ j^{op}$. But this is the case precisely by the statement of the full [[(∞,1)-Yoneda lemma]].

Now consider more generally the case that $C$ is a [[reflective sub-(∞,1)-category]] of $PSh(D)$. Let $L : PSh(D) \to C $ be the [[left adjoint]] reflector. Since it respects all colimits, the composite

$$
  F \circ L^{op} : PSh(D)^{op} \stackrel{L^{op}}{\to} C^{op} \stackrel{F}{\to} \infty Grpd
$$

respects all limits. By the above it is therefore represented by some object $X \in PSh(D)$.

By the general properties of [[reflective sub-(∞,1)-categories]], we have that $C$ is the full [[sub-(∞,1)-category]] of $PSh(D)$ on those objects that are [[local object]]s with respect to the morphisms that $L$ sends to equivalences. But $X$, since it presents $F \circ L^{op}$, is manifestly local in this sense and therefore also represents $F \circ L^{op}|_{C}$. But on $C$ the functor $L$ is equivalent to the identity, so that this is equivlent to $F$.

=--


This statement has the following important consequence:

+-- {: .un_cor}
###### Corollary

A locally presentable $(\infty,1)$-category $C$ has all small [[limit in a quasi-category|limits]].

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.2.4]].


+-- {: .proof}
###### Proof

We may compute the limit after applying the [[(∞,1)-Yoneda embedding]] $j : C \to PSh_{(\infty,1)}(c)$. Since this is a [[full and faithful (∞,1)-functor]] it is sufficient to check that the limit computed in $PSh(C)$ lands in the essential image of $j$. But by the above lemma, this amounts to checking that the limit over limit-preserving functors is itself a limit-preserving functor. This follows using that limits of functors are computed objectwise and that generally limits commute with each other (see [[limit in a quasi-category]]):

to check for $I \to PSh(C)$ a diagram of limit-preserving functors that $\lim_i F_i$ is a functor that commutes with all limits, let $a : J \to C$ be a diagram and compute (verbatim as in ordinary category theory)

$$
  \begin{aligned}
    \lim_j (\lim_i F_i)(a_j)
    & \simeq 
    \lim_j (\lim_i F_i(a_j))
    \\
    & \simeq
    \lim_i (\lim_j F_i(a_j))
    \\
    & \simeq
    \lim_i F_i(\lim a_j)
    \\
    & \simeq
    (\lim_i F_i)(\lim a_j)
  \end{aligned}
  \,.
$$

=--

## Examples

* An [[(∞,1)-topos]] is precisely a locally presentable $(\infty,1)$-category where the [[localization of an (∞,1)-category|localization]] functor also preserves finite limits.

* Since [[Pr(∞,1)Cat]] admits all small limits, we obtain new locally presentable $(\infty,1)$-categories by forming limits over given ones. In particular the [[product]] of locally presentable $(\infty,1)$-categories is again locally presentable.


+-- {: .un_prop}
###### Proposition

For $C$ and $D$ locally presentable $(\infty,1)$-categories, write $Func^L(C,D) \subset Func(C,D)$ for the full sub-$(\infty,1)$-category on left-adjoint $(\infty,1)$-functors. This is itself locally presentable

=--

This is [[Higher Topos Theory|HTT, prop 5.5.3.8]]

Notice that this makes the [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]] _[[closed monoidal category|closed]]_ .


+-- {: .un_prop}
###### Proposition

For $C$ a locally presentable $(\infty,1)$-category and $p : K \to C$ a [[diagram]] in $C$, also the [[over quasi-category|over (∞,1)-category]] $C_{/pp}$ as well as the under-$(\infty,1)$-category $C_{p/}$ are locally presentable.

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.3.10, prop. 5.5.3.11]].


+-- {: .un_prop}
###### Proposition

For $C$ an $(\infty,1)$-category with finite [[product]]s, the $(\infty,1)$-category $Alg_{(\infty,1)}(C)$ of algebras over $C$ regarded as an [[(∞,1)-algebraic theory]] is locally presentable.

=--




## References 

The theory of locally presentable $(\infty,1)$-categories was first implicitly conceived in terms of [[model category]] presentations in

* [[Carlos Simpson]],  _A Giraud-type characterization of the simplicial categories associated to closed model categories as $\infty$-pretopoi ([arXiv:math/9903167](http://arxiv.org/abs/math/9903167))

The full intrinsic $(\infty,1)$-categorical theory appears in section 5 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

with section A.3.7 establishing the relation [[combinatorial model categories]] and [Dugger's theorem](http://ncatlab.org/nlab/show/combinatorial+model+category#DuggerTheorem) in [[Higher Topos Theory|HTT, prop A.3.7.6]]



[[!redirects presentable (infinity,1)-categories]]
[[!redirects presentable (∞,1)-category]]
[[!redirects presentable (∞,1)-categories]]

[[!redirects locally presentable (infinity,1)-category]]
[[!redirects locally presentable (infinity,1)-categories]]
[[!redirects locally presentable (∞,1)-category]]
[[!redirects locally presentable (∞,1)-categories]]

[[!redirects presentable (infinity,1)-category]]
