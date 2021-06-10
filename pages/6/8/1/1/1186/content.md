
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
* table of contents
{:toc}

## Idea 

An [[(∞,1)-category]] is called _locally presentable_ if it has all small [[(∞,1)-colimits]] and its [[objects]] are [[generators and relations|presented]] under [[(∞,1)-colimits]] by a [[small set]] of [[small objects]]. 
This is the direct analog in [[(∞,1)-category]] theory of the notion of _[[locally presentable category]]_ in [[category theory]].

There is a wealth of equivalent ways to make precise what this means, which are listed [below](#Definition). Two particularly useful ones are:

1. A locally presentable $(\infty,1)$-category is an [[accessible (∞,1)-category]] that admits all small [[(∞,1)-colimits]].

1. The locally presentable $(\infty,1)$-categories $\mathcal{C}$ are precisely the [[accessible (∞,1)-functor|accessibly embedded]] [[localization of an (∞,1)-category|localizations]]/[[reflective sub-(∞,1)-category|reflections]] $\mathcal{C} \stackrel{\overset{}{\leftarrow}}{\hookrightarrow} PSh_\infty(K)$ of an [[(∞,1)-category of (∞,1)-presheaves]]. In particular, if the reflector of this reflection is a [[left exact (∞,1)-functor]], then $\mathcal{C}$ is an [[(∞,1)-topos]].

See also at _[[locally presentable categories - introduction]]_.

**Warning on terminology.** In [Lurie](#Lurie) the term _presentable $(\infty,1)$-category_ is used for what we call a _locally presentable $(\infty,1)$-category_ here, in order to be in line with the established terminology of _[[locally presentable category]]_ in ordinary [[category theory]]. 

**Terminological variant.** The term "$\kappa$-[[compactly generated (∞,1)-category]]" is sometimes used to mean "locally $\kappa$-presentable (∞,1)-category. See there for a discussion of usage differences.

## Definition 
 {#Definition}


+-- {: .num_defn}
###### Definition



An [[(∞,1)-category]] $\mathcal{C}$ is called **locally presentable** 
if 

1. it is [[accessible (∞,1)-category|accessible]] 

1. it has all small [[(∞,1)-colimits]].

=--

+-- {: .num_prop #EquivalentCharacterizations}
###### Proposition

That $\mathcal{C}$ is locally presentable is equivalent to each of the following equivalent characterizations.

1. $\mathcal{C}$ is [[locally small (infinity,1)-category|locally small]], with all small [[(∞,1)-colimits]] such that there is a [[small set]] $S \hookrightarrow Obj(\mathcal{C})$ of [[small objects]] which generates all of $\mathcal{C}$ under [[(∞,1)-colimits]].

1.  $\mathcal{C}$ is the [[localization of an (∞,1)-category|localization]] of an [[(∞,1)-category of (∞,1)-presheaves]] $PSh_\infty(K)$ along an [[accessible (∞,1)-functor]]:

    there exists a [[small (∞,1)-category]] $K$ and a pair of [[adjoint (∞,1)-functors]]

    $$
      \mathcal{C} \stackrel{\overset{}{\leftarrow}}{\hookrightarrow} PSh_\infty(K)
    $$

    such that the [[right adjoint]] $\mathcal{C} \hookrightarrow PSh_\infty(K)$ is [[full and faithful (∞,1)-functor|full and faithful]] and [[accessible (∞,1)-functor|accessible]].


    (if here in addition $f$ is [[exact functor|left exact]] then $\mathcal{C}$ is an [[(∞,1)-category of (∞,1)-sheaves]] on $K$).


1. There exists a [[combinatorial simplicial model category]] $A$ and and [[equivalence of (infinity,1)-categories]] $\mathcal{C} \simeq L_W A$ with the [[simplicial localization]] of $A$.
 
   More explicitly: with $\mathcal{C}$ incarnated as a [[quasi-category]] there is an [[equivalence of quasi-categories]] $ \mathcal{C} \simeq N(A^\circ)$ of $\mathcal{C}$ with the [[homotopy coherent nerve]] of the full [[sSet]]-[[enriched category|enriched]] [[subcategory]] of $A$ on [[fibrant object|fibrant]] and [[cofibrant objects]].

1. $\mathcal{C}$ is [[accessible (infinity,1)-category|accessible]] and for every [[cardinal number|regular cardinal]] $\kappa$ the [[full sub-(∞,1)-category]] $\mathcal{C}^\kappa \hookrightarrow \mathcal{C}$ on the $\kappa$ [[compact object in an (∞,1)-category|compact objects]] admits $\kappa$-small [[(∞,1)-colimits]].


1. There exists a [[cardinal number|regular cardinal]] $\kappa$ such that $\mathcal{C}$ is $\kappa$-[[accessible (infinity,1)-category|accessible]] and $C^\kappa$ admits $\kappa$-small [[limit in quasi-categories|colimits]];

1. There exists a [[cardinal number|regular cardinal]] $\kappa$, a [[small (∞,1)-category]] $D$ with $\kappa$-small [[limit in quasi-categories|colimits]] and an equivalence $Ind_\kappa D \stackrel{\simeq}{\to} \mathcal{C}$ with the category of $\kappa$-[[ind-objects]] of $D$.


=--

This is [Lurie, theorem 5.5.1.1](#Lurie), following [Simpson 99](#Simpson99), [Dugger 00](#Dugger00); review in [Cisinski 19, Thm. 7.11.16, Rem. 7.11.17](#Cisinski19).


+-- {: .num_remark}
###### Remark

That [[localization of an (infinity,1)-category|localizations]] $\mathcal{C} \stackrel{\leftarrow}{\hookrightarrow} PSh_{(\infty,1)}(K)$ correspond to combinatorial simplicial model categories is essentially **[[Dugger's theorem]]** ([Dugger](#Dugger)): every [[combinatorial model category]] arises, up to Quillen equivalence, as the left [[Bousfield localization of model categories|left Bousfield localization]] of the global projective [[model structure on simplicial presheaves]].

=--

Locally presentable $(\infty,1)$-categories have a number of nice
properties, and therefore it is of interest to consider as
morphisms between them only those [[(∞,1)-functor]]s that preserve
these properties. It turns out that it is useful to consider
_[[limit in a quasi-category|colimit]] preserving_ functors. By the [[adjoint (∞,1)-functor theorem]] these are precisely the functors that have a right [[adjoint (∞,1)-functor]].

+-- {: .num_defn}
###### Definition

Write [[Pr(∞,1)Cat]] $\subset$ [[(∞,1)Cat]] for the (non-full) [[sub-quasi-category|sub-(∞,1)-category]] of [[(∞,1)Cat]] (the collection of not-necessarily small $(\infty,1)$-categories) on

* those objects that are locally presentable $(\infty,1)$-categories;

* those morphisms that are colimit-preserving [[(∞,1)-functor]]s.

=--

This is [Lurie, def. 5.5.3.1](#Lurie).


This $(\infty,1)$-category $Pr(\infty,1)Cat$ in turn as special properties. More on that is at _[[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]]_.




## Properties

### Equivalent characterizations
 {#EquivalentCharacterizationsDetails}

We indicate stepts in the proof of prop. \ref{EquivalentCharacterizations}.

+-- {: .num_lemma}
###### Lemma

Let $f \colon \mathcal{C} \to \mathcal{D}$ be an [[(∞,1)-functor]] which exhibits $\mathcal{D}$ as an [[idempotent completion]] $\mathcal{C}$. Let $\kappa$ be a [[regular cardinal]]. Then the induced functor on [[(∞,1)-categories of ind-objects]]

$$
  Ind_\kappa(f) \colon Ind_\kappa(\mathcal{C}) \to Ind_\kappa(\mathcal{D})
$$

is an [[equivalence of (∞,1)-categories]].

=--

This is ([Lurie, lemma 5.5.1.3](#Lurie)).

+-- {: .num_lemma}
###### Lemma

Let $L \colon \mathcal{C} \to \mathcal{D}$ be an [[(∞,1)-functor]] between [[(∞,1)-categories]] which have $\kappa$-[[filtered (∞,1)-colimits]], and let $R$ be a [[right adjoint|right]] [[adjoint (∞,1)-functor]] of $L$. If $R$ preserves $\kappa$-[[filtered (∞,1)-colimits]] then $L$ preserves $\kappa$-[[compact objects]].

=--

This is [Lurie, lemma 5.5.1.4](#Lurie).

(...)


### Stability under various constructions
 {#StabilityUnderVariousConstructions}

+-- {: .num_prop}
###### Proposition

For $C$ a locally presentable $(\infty,1)$-category and $p : K \to C$ a [[diagram]] in $C$, also the [[over quasi-category|over (∞,1)-category]] $C_{/pp}$ as well as the under-$(\infty,1)$-category $C_{p/}$ are locally presentable.

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.3.10, prop. 5.5.3.11]].

+-- {: .num_example}
###### Example

Since [[Pr(∞,1)Cat]] admits all small limits, we obtain new locally presentable $(\infty,1)$-categories by forming limits over given ones. In particular the [[product]] of locally presentable $(\infty,1)$-categories is again locally presentable.

=--



### Limits and colimits 
 {#LimitsAndColimits}

In the first definition of locally presentable $(\infty,1)$-category above only the existence of colimits is postulated. An important fact is that it follows automatically that also all small limits exist:

A [[representable functor]] $C^{op} \to \infty Grpd$ preserves [[limit in a quasi-category|limits]] (see [[(∞,1)-Yoneda embedding]]). If $C$ is locally presentable, then also the converse holds:

+-- {: .num_prop}
###### Proposition

If $\mathcal{C}$ is a locally presentable $(\infty,1)$-category then an [[(∞,1)-functor]] $C^{op} \to \infty Grpd$ is a [[representable functor]]
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

+-- {: .num_cor}
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

### As $(\infty,1)$-categories presented by combinatorial simplicial model categories
 {#PresentedByCombinatorialSimplicialModelCategories}

By prop. \ref{EquivalentCharacterizations}
locally presentable $(\infty,1)$-categories are equivalently those [[(∞,1)-categories]] which are _presented_ by a [[combinatorial simplicial model category]] $C$ in that they are the full [[simplicially enriched category|simplicial subcategory]] $C^\circ \hookrightarrow C$ on fibrant-cofibrant objects of $C$ (or, equivalently, the [[quasi-category]] associated to this [[simplicially enriched category]]).

(See also at *[[Ho(CombModCat)]]*).

+-- {: .num_remark #QuillenEquivZigZag} 
###### Remark

Under this presentation, [[equivalence of (∞,1)-categories]] between locally presentable $(\infty,1)$-categories corresponds to [[zigzags]] of [[Quillen equivalences]] between presenting [[combinatorial simplicial model category|combinatorial simplicial model categories]]:

$C^\circ$ and $D^\circ$ are [[equivalence of (∞,1)-categories|equivalent as (∞,1)-categories]] precisely if they are connected by a [[zig-zag]] of [[simplicial Quillen adjunction|simplicial]] [[Quillen equivalences]]

$$
  C 
  \stackrel{\leftarrow}{\to}
  \stackrel{\to}{\leftarrow}
  \stackrel{\leftarrow}{\to}
  \cdots  
  D.
$$

=--

This is [Lurie, remark A.3.7.7](#Lurie).

+-- {: .num_remark}
###### Remark

Partly due to the fact that [[simplicial model category|simplicial model categories]] have been studied for a longer time -- partly because they are simply more tractable than [[(∞,1)-categories]] -- many $(\infty,1)$-categories are indeed handled in terms of such a presentation by a [[simplicial model category]]. 

The canonical example is the presentation of the [[(∞,1)-category of (∞,1)-sheaves]] on an ordinary (1-categorical) [[site]] $S$ by the simplicial [[model structure on simplicial presheaves|model category of simplicial presheaves]] on $S$.

=--



## Examples

The basic example is:

+-- {: .num_example}
###### Example

[[∞Grpd]] is locally presentable.

=--

([Lurie, example 5.5.1.8](#Lurie))

+-- {: .proof}
###### Proof

According to the discussion at [(∞,1)-colimit -- Tensoring with an ∞-groupoid](limit+in+a+quasi-category#Tensoring) every [[∞-groupoid]] is the colimit over itself of the functor contant on the point, the terminal $\infty$-groupoid. This is clearly compact, and hence generates [[∞Grpd]].

=--

+-- {: .num_example}
###### Example

An [[(∞,1)-topos]] is precisely a locally presentable $(\infty,1)$-category where the [[localization of an (∞,1)-category|localization]] functor also preserves finite limits.

=--

+-- {: .num_prop}
###### Proposition

For $C$ and $D$ locally presentable $(\infty,1)$-categories, write $Func^L(C,D) \subset Func(C,D)$ for the full sub-$(\infty,1)$-category on left-adjoint $(\infty,1)$-functors. This is itself locally presentable

=--

This is [[Higher Topos Theory|HTT, prop 5.5.3.8]]

Notice that this makes the [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]] _[[closed monoidal category|closed]]_ .




+-- {: .num_prop}
###### Proposition

For $C$ an $(\infty,1)$-category with finite [[products]], the $(\infty,1)$-category $Alg_{(\infty,1)}(C)$ of algebras over $C$ regarded as an [[(∞,1)-algebraic theory]] is locally presentable.

=--


## Related concepts

* [[Ho(CombModCat)]]

[[!include locally presentable categories - table]]

* [[compactly generated (infinity,1)-category]]

## References 

The theory of locally presentable $(\infty,1)$-categories was first implicitly conceived in terms of [[model category]] presentations in

* {#Simpson99} [[Carlos Simpson]],  _A Giraud-type characterization of the simplicial categories associated to closed model categories as $\infty$-pretopoi ([arXiv:math/9903167](http://arxiv.org/abs/math/9903167))
 

The full intrinsic $(\infty,1)$-categorical theory appears in  

* {#Lurie} [[Jacob Lurie]], Section 5 of: _[[Higher Topos Theory]]_
 
with section A.3.7 establishing the relation to [[combinatorial model categories]] and [[Dugger's theorem]] in [[Higher Topos Theory|HTT, prop A.3.7.6]].

The statement of [[Dugger's theorem]] -- of which the characterization of locally presentable $(\infty,1)$-categories as localizations of $(\infty,1)$-presheaf categories is a variant -- is due to 

* {#Dugger00} [[Dan Dugger]], _[[Combinatorial model categories have presentations]]_,  Adv. Math. 164 (2001), no. 1, 177-201 ([arXiv:math/0007068](http://arxiv.org/abs/math/0007068))

Further textbook account:

* {#Cisinski19} [[Denis-Charles Cisinski]], Section 7.11 in: _Higher category theory and homotopical algebra_,  Cambridge University Press 2019 ([doi:10.1017/9781108588737](https://doi.org/10.1017/9781108588737), [pdf](http://www.mathematik.uni-regensburg.de/cisinski/CatLR.pdf))




[[!redirects presentable (infinity,1)-categories]]
[[!redirects presentable (∞,1)-category]]
[[!redirects presentable (∞,1)-categories]]

[[!redirects locally presentable (infinity,1)-category]]
[[!redirects locally presentable (infinity,1)-categories]]
[[!redirects locally presentable (∞,1)-category]]
[[!redirects locally presentable (∞,1)-categories]]

[[!redirects presentable (infinity,1)-category]]

[[!redirects locally presentable infinity-category]]