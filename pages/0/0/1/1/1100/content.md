
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Recall the following familiar 1-categorical statement:

* Working in the 1-[[category]] [[Set]] of [[0-category|0-categories]] amounts to doing [[set theory]]. The point of [[sheaf topos|sheaf]] [[toposes]] is to pass to _parameterized_  [[0-category|0-categories]], namely  [[presheaf]] categories. Although these [[topos|topoi]] behave much like the 1-topos [[Set]], their objects are generalized [[spaces]] that may carry more structure. For instance, a (pre)[[sheaf]] on [[Diff]] is a [[generalized smooth space]].

The idea of $(\infty,1)$-toposes is to generalize the above situation from $1$ to $(\infty,1)$  (recall the notion of [[(n,r)-category]] and see the general discussion at [[∞-topos]]):

* Working in the [[(∞,1)-category]] [[∞Grpd]] of [[infinity-groupoid|(∞,0)-categories]] amounts to doing [[homotopy theory]]. The point of [[(∞,1)-sheaves]] is to pass to _parameterized_ [[(∞,0)-categories]], namely  [[(∞,1)-presheaf]] categories. Although these $(\infty,1)$-topoi behave much like the $(\infty,1)$-topos [[∞Grpd]], their objects are generalized [[spaces]] with higher [[homotopies]] that may carry more structure. More generally we have topoi of [[sheaves]], and $(\infty,1)$-topoi of [[(∞,1)-sheaves]].  For instance, an [[∞-Lie groupoid]] is an [[(∞,1)-sheaf]] on [[CartSp]].


## Definition {#Definition}

### As a geometric embedding into a $(\infty,1)$-presheaf category
 {#AsAGeometricEmbedding}

Recall that [[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes]] and that the inclusion functor is necessarily an [[accessible functor]]. This characterization has the following immediate generalization to a definition in [[(∞,1)-category theory]], where the only subtlety is that accessibility needs to be explicitly required:

+-- {: .num_defn #ToposByLocalization}
###### Definition

A [[Alexander Grothendieck|Grothendieck]]--[[Charles Rezk|Rezk]]--[[Jacob Lurie|Lurie]] **$(\infty,1)$-topos** $\mathbf{H}$ is an [accessible](reflective%20sub-%28infinity,1%29-category#AccessibleReflectiveSubcategory) [left exact](reflective+sub-%28infinity%2C1%29-category#ExactLocalizations) [[reflective sub-(∞,1)-category]] of an [[(∞,1)-category of (∞,1)-presheaves]]

$$
  \mathbf{H}
  \stackrel{\overset{lex}{\leftarrow}}{\hookrightarrow}
  PSh_{(\infty,1)}(C)
  \,.
$$

If the above localization is a [[topological localization]] then $\mathbf{H}$ is an **[[(∞,1)-category of (∞,1)-sheaves]]**.

=--

### By Giraud-Rezk-Lurie axioms 
 {#GiraudAxioms}

Equivalently: 

+-- {: .num_prop}
###### Proposition

An $(\infty,1)$-topos $\mathbf{H}$ is

an [[(∞,1)-category]] that satisfies the $(\infty,1)$-categorical analogs of [[Giraud's axioms]]:

* $\mathbf{H}$ is [[presentable (infinity,1)-category|presentable]];
* [[limit in quasi-categories|(∞,1)-colimits]] in $\mathbf{H}$ [[universal colimits|are universal]];
* [[coproduct]]s in $\mathbf{H}$ are [[disjoint coproduct|disjoint]];
* every [[groupoid object in an (infinity,1)-category|groupoid object]] in $\mathbf{H}$ is [[quotient object|effective]] (i.e. has a [[delooping]]). 

=--

This is  part of the statement of [[Higher Topos Theory|HTT, theorem 6.1.0.6]].

This is derived from the following equivalent one:

+-- {: .num_prop #CharacterizationByObjectClassifier}
###### Proposition

An [[(∞,1)-topos]] is

* a [[presentable (∞,1)-category]] with [[universal colimits]]

* that has [[object classifiers]].

=--

+-- {: .num_remark #ReflectonOnCharacterizationByObjectClassifier}
###### Remark

An [[object classifier]] is a (small) _self-reflection_ of the $\infty$-topos inside itself ([[type of types]], internal [[universe]]). See also ([WdL, book 2, section 1](Science+of+Logic#WesenAlsReflexionInIhmSelbst)).

=--

A further equivalent one (essentially by an invocation of the adjoint functor theorem) is:

+-- {: .num_prop}
###### Proposition

An [[(∞,1)-topos]] is

* a [[presentable (∞,1)-category]]

* in which all colimits are [[van Kampen colimits]].
 
=--

### Morphisms

A [[morphism]] between $(\infty,1)$-toposes is an [[(∞,1)-geometric morphism]].

The [[(∞,1)-category]] of all $(\infty,1)$-topos is [[(∞,1)Toposes]].


## Types of $(\infty,1)$-toposes

### Topological localizations / $(\infty,1)$-sheaf toposes

for the moment see

* [[topological localization]]


### Hypercomplete $(\infty,1)$-toposes

for the moment see 

* [[hypercomplete (∞,1)-topos]]

### Cubical type theory

The Cartesian cubical model of [[cubical type theory]] and [[homotopy type theory]] is [conjectured](https://groups.google.com/d/msg/homotopytypetheory/RQkLWZ_83kQ/s6iazlFdBgAJ) to be an (∞,1)-topos not equivalent to (∞,1)-groupoids.

## Models 

Another main theorem about $(\infty,1)$-toposes is that
[[models for ∞-stack (∞,1)-toposes]] are given by the [[model structure on simplicial presheaves]]. See there for details


## Properties

### Global sections geometric morphism
 {#GlobalSectionsGeometricMorphism}

Every [[∞-stack]] $(\infty,1)$-topos $\mathbf{H}$ has a canonical [[(∞,1)-geometric morphism]] to the terminal $\infty$-stack $(\infty,1)$-topos [[∞Grpd]]: the [[direct image]] is the [[global section]]s [[(∞,1)-functor]] $\Gamma$, the [[inverse image]] is the [[constant ∞-stack]] functor

$$
  (LConst \dashv \Gamma) 
  \;\colon\;
  \mathbf{H}
  \underoverset
    {\underset{\Gamma}{\longrightarrow}}
    {\overset{LConst}{\longleftarrow}}
    {\;\;\; \bot \;\;\;}
  \infty Grpd
  \,.
$$

In fact, this is unique, up to [[equivalence in an (infinity,1)-category|equivalence]]: Since every $\infty$-groupoid is an [[(infinity,1)-colimit|$(\infty,1)$-colimit]] (namely over itself, by [this Prop.](infinity1-limit#EveryInfinityGroupoidIsHomotopyColimitOfConstantFunctorOverItself)) of the [[point]] (hence of the [[terminal object]]), and since the [[inverse image]] $\infty$-functor $LConst$ needs to preserve these $\infty$-colimits (being a [[left adjoint]]) as well as the point (being a [[lex functor]]).

### Powering and copowering over $\infty Grpd$ --  Hochschild homology {#Powering}

Being a [[locally presentable (∞,1)-category]], an $(\infty,1)$-topos $\mathbf{H}$ is [[power]]ed and [[copower]]ed over [[∞Grpd]], as described at <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#Tensoring">(∞,1)-tensoring</a>. 

For any $K \in \infty Grpd$ and $X \in \mathbf{H}$ the powering is the [[(∞,1)-limit]] over the [[diagram]] constant on $X$

$$
  X^K = {\lim_\leftarrow}_K X
$$

and the $(\infty,1)$-copowering is is the [[(∞,1)-colimit]] over the diagram constant on $X$

$$
  K \cdot X = {\lim_{\to}}_K X
  \,.
$$

Under [[Isbell duality]] the powering operation corresponds to higher order [[Hochschild cohomology]] in $X$, as discussed there.

Below we discuss that the powering is equivalently given by the [[internal hom]] ([[mapping stack]]) out of the [[constant ∞-stack]] $LConst K$ on $K$:

$$
  X^K \simeq [LConst K, X]
  \,.
$$


### Closed monoidal structure {#ClosedMonoidalStructure}

+-- {: .num_prop}
###### Proposition

Every $(\infty,1)$-topos is a [[cartesian closed (∞,1)-category]].

=--

+-- {: .proof}
###### Proof

By the fact that every $(\infty,1)$-topos $\mathbf{H}$ has [[universal colimits]] it follows that for every object $X$ the [[(∞,1)-functor]]

$$
  X \times (-) : \mathbf{H} \to \mathbf{H}
$$

preserves all [[(∞,1)-colimit]]s. Since every $(\infty,1)$-topos is a [[locally presentable (∞,1)-category]] it follows with the [[adjoint (∞,1)-functor theorem]] that there is a [[right adjoint|right]] [[adjoint (∞,1)-functor]]

$$
  (X \times (-) \dashv [X,-]) : \mathbf{H} \stackrel{\overset{X \times (-)}{\leftarrow}}{\underset{[X,-]}{\to}} \mathbf{H}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $C$ an [[(∞,1)-site]] for $\mathbf{H}$ we have that the [[internal hom]] ([[mapping stack]]) $[X,-]$ is given on $A \in \mathbf{H}$ by the [[(∞,1)-sheaf]]

$$
  [X,A] : U \mapsto \mathbf{H}(X \times L y(U), A)
  \,,
$$

where $y : C \to \mathbf{H}$ is the [[(∞,1)-Yoneda embedding]] and $L : PSh_C \to \mathbf{H}$ denotes [[∞-stackification]].

=--


+-- {: .proof}
###### Proof

The argument is entirely analogous to that of the [[closed monoidal structure on sheaves]].

We use the [[full and faithful (∞,1)-functor|full and faithful]] [[geometric embedding]] $(L \dashv i) : \mathbf{H} \hookrightarrow PSh_C$ and the [[(∞,1)-Yoneda lemma]] to find for all $U \in C$ the value

$$
  [X,A](U) \simeq PSh_C(y U, [X,A])
$$

and then the fact that [[∞-stackification]] $L$ is [[left adjoint]] to inclusion to get

$$
  \cdots \simeq \mathbf{H}(L y(U), [X,A])
  \,.
$$

Then the defining adjunction $(X \times (-) \dashv [X,-])$ gives

$$
  \cdots \simeq \mathbf{H}(X \times L y(U) , A)
  \,.
$$


=--

+-- {: .num_prop}
###### Proposition

Finite colimits may be taken out of the internal hom: For $I$ a finite $(\infty,1)$-category and $X : I \to \mathbf{H}$ a [[diagram]], we have for all $A \in \mathbf{H}$

$$
  [{\lim_\to}_i X_i, A]
   \simeq
  {\lim_\leftarrow}_i [X_i,A]
$$

=--

+-- {: .proof}
###### Proof

By the above proposition we have

$$
  [{\lim_\to}_i X_i, A](U) 
  \simeq
  \mathbf{H}(({\lim_\to}_i X_i) \times L y(U), A)
  \,.
$$

By [[universal colimits]] in $\mathbf{H}$ this is

$$
  \cdots \simeq
  \mathbf{H}({\lim_\to}_i X_i \times L y(U), A)
  \,.
$$

Using the fact that the [[hom-functor]] sends colimits in the first argument to limits this is

$$
  \cdots \simeq {\lim_\leftarrow}_i \mathbf{H}(X_i \times L y U, A)
  \,.
$$

By the internal hom adjunction and Yoneda this is

$$
  \cdots \simeq {\lim_\leftarrow}_i [X_i, A](U)
  \,.
$$

Since [[(∞,1)-limit]]s in the [[(∞,1)-category of (∞,1)-presheaves]] are computed objectwise, this is

$$
  \cdots \simeq ({\lim_\leftarrow}_i [X_i,A])(U) 
  \,.
$$

Finally, because $L$ is a  [[left exact (∞,1)-functor]] this is also the [[(∞,1)-limit]] in $\mathbf{H}$.


=--

+-- {: .num_prop}
###### Proposition

For $S \in$ [[∞Grpd]] write $LConst S$ for its [[inverse image]] under the [[global section]] [[(∞,1)-geometric morphism]] $(LConst \dashv \Gamma) : \mathbf{H} \to \infty Grpd$: the [[constant ∞-stack]] on $S$.

Then the internal hom $[LConst S,A]$ coincides with the [(∞,1)-powering](#Powering) of $A$ by $S$:

$$
  [LConst S, A] \simeq A^S
$$

=--

+-- {: .proof}
###### Proof

By the above we have

$$
  [LConst S, A](U) \simeq \mathbf{H}(LConst S \times L y(U), A)
  \,.
$$

As the notation indicates, $LConst S$ is precisely $L Const S$: the [[∞-stackification]] of the [[(∞,1)-presheaf]] that is literally constant on $S$. Morover $L$ is a [[left exact (∞,1)-functor]] and hence commutes with [[(∞,1)-product]]s, so that

$$
  \cdots \simeq \mathbf{H}(L(Const S \times y(U)), A)
  \,.
$$

By the defining geometric embedding $(L \dashv i)$ this is

$$
  \cdots \simeq PSh_C(Const S \times y(U), A)
  \,.
$$

Since limits of [[(∞,1)-presheaves]] are taken objectwise, we have in the first argument the [[tensoring]] of $y(U)$ over $S$

$$
  \cdots \simeq PSh_C(S \cdot y(U), A)
  \,.
$$

By the defining property of tensoring and cotensoring (or explicitly writing out $S \cdot y(U) = {\lim_\to}_{S} const y(U) $, taking the colimit out of the hom, thus turning it into a limit and then inserting that back in the second argument) this is

$$
  \cdots \simeq PSh_C(y(U), A^S)
  \,.
$$


So finally with the [[(∞,1)-Yoneda lemma]] we have

$$
  \cdots \simeq A^S(U)
  \,.
$$

=--

### Over-$(\infty,1)$-toposes

+-- {: .num_prop}
###### Proposition

For $\mathbf{H}$ an $(\infty,1)$-topos and $X \in \mathbf{H}$ an object, the [[over-(∞,1)-category]] $\mathbf{H}_{/X}$ is itself an $(\infty,1)$-topos -- an **[[over-(∞,1)-topos]]**. The projection $\pi_! : \mathbf{H}_{/X} \to \mathbf{H}$ part of an  [[essential geometric morphism]]

$$
  \pi : \mathbf{H}_{/X} 
  \stackrel{\overset{\pi_!}{\to}}{\stackrel{\overset{\pi^*}{\leftarrow}}{\underset{\pi_*}{\to}}}
  \mathbf{H}
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, prop. 6.3.5.1]].

The $(\infty,1)$-topos $\mathbf{H}_{/X}$ could be called the [[gros topos]] of $X$. A [[geometric morphism]] $\mathbf{K} \to \mathbf{H}$ that factors as $\mathbf{K} \xrightarrow{\simeq} \mathbf{H}_{/X} \stackrel{\pi}{\to} \mathbf{H}$ is called an [[etale geometric morphism]].


### Syntax in univalent homotopy type theory

$(\infty,1)$-Toposes provide [[categorical semantics]] for [[homotopy type theory]] with a [[univalence|univalent]] Tarskian [[type of types]] (which inteprets as the [[object classifier]]).

For more on this see at 

* _[[homotopytypetheory:model of type theory in an (infinity,1)-topos]]_

* _[relation between type theory and category theory -- Univalent homotopy type theory and infinity-toposes](relation+between+type+theory+and+category+theory#HomotopyWithUnivalence)_



## $(\infty,1)$-Topos theory {#ToposTheory}

Most of the standard constructions in [[topos theory]] have or should have  immediate generalizations to the context of $(\infty,1)$-toposes, since all notions of [[category theory]] exist for [[(∞,1)-categories]].

For instance there are evident notions of

* [[geometric morphism]]s between $(\infty,1)$-toposes, such as the [[global section]] geometric morphism to the [[terminal object|terminal]] [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf]] $(\infty,1)$-topos [[∞Grpd]].

Moreover, it turns out that $(\infty,1)$-toposes come with plenty of internal structures, more than canonically present in an ordinary topos. 
Every $(\infty,1)$-topos comes with its intrinsic notion of

* [[cohomology|cohomology in an (∞,1)-topos]]

and with an intrinsic notion of

* [[homotopy groups in an (∞,1)-topos|homotopy in an (∞,1)-topos]].


In classical topos theory, cohomology and homotopy of a topos $E$ are defined in terms of [[simplicial object]]s in $C$. If $E$ is a [[sheaf topos]] with [[site]] $C$ and [[point of a topos|enough point]]s, then  this classical construction is secretly really a model for the intrinsic cohomology and homotopy in the above sense of the  [[hypercomplete (∞,1)-topos]] of [[∞-stack]]s on $C$.


The beginning of a list of all the structures that exist intrinsically in a big $(\infty,1)$-topos is at

* [[cohesive (∞,1)-topos]].

But **$(\infty,1)$-topos theory** in the style of an $\infty$-analog of the [[Elephant]] is only barely beginning to be conceived. 

There are some indications as to what the

* [[internal logic of an (∞,1)-topos]]

should be.


## Related concepts

* [[elementary (∞,1)-topos]], [[(∞,1)-pretopos]]

* [[model topos]]

* [[structured (∞,1)-topos]]

* [[compact topos]], [[coherent (∞,1)-topos]]

* [[category object in an (∞,1)-topos]]


[[!include flavors of higher toposes -- list]]





[[!include locally presentable categories - table]]


## References

### General

In retrospect it turns out that the [[homotopy category of an (∞,1)-category|homotopy categories]] of [[(∞,1)-topos]]es have been known since

* [[Kenneth Brown]], _[[BrownAHT|Abstract homotopy theory and generalized sheaf cohomology]]_ .

And the [[model category]] theory models have been known since [[Andre Joyal]] proposed the [[model structure on simplicial sheaves]] in his letter to [[Alexander  Grothendieck]].

This work used 1-categorical [[site]]s. The generalization to [[(∞,1)-category|(∞,1)categorical sites]] -- modeled by [[model sites]] -- was discussed in

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry I: Topos theory_, Advances in Mathematics 193.2 (2005): 257-372. ([arXiv:math.AG/0207028](http://arxiv.org/abs/math.AG/0207028))

and "model topos"-theory was also developed in

* {#Rezk10} [[Charles Rezk]], _Toposes and homotopy toposes_, 2010 ([pdf](http://www.math.uiuc.edu/~rezk/homotopy-topos-sketch.pdf))

The intrinsic [[higher category theory|category-theoretic]] definition of an [[(∞,1)-topos]] was given in section 6.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

building on ideas by [[Charles Rezk]]. There is is also proven that the Brown-Joyal-Jardine-To&#235;n-Vezzosi models indeed precisely model $\infty$-stack $(\infty,1)$-toposes. Details on this relation are at [[models for ∞-stack (∞,1)-toposes]].

Overview

* [[Denis-Charles Cisinski]], _Cat&#233;gories sup&#233;rieures et th&#233;orie des topos_, S&#233;minaire Bourbaki, 21.3.2015, [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/1097.pdf).

* [[Charles Rezk]], _Lectures on Higher Topos Theory_, Leeds 2019 ([pdf](https://faculty.math.illinois.edu/~rezk/leeds-lectures-2019.pdf), [[RezkHigherToposTheory2019.pdf:file]])


A useful collection of facts of [[simplicial homotopy theory]] and [[(infinity,1)-topos theory]] is in

* [[Zhen Lin Low]], _[[Notes on homotopical algebra]]_

A quick introduction to the topic is in 

* [[André Joyal]], _[[A crash course in topos theory -- The big picture]]_, lecture series at [Topos &#224; l'IHES](https://indico.math.cnrs.fr/event/747/), November 2015, Paris 


### Giraud-Rezk-Lurie axioms

A discussion of the $(\infty,1)$-[[universal colimits]] in terms of [[model category]] presentations is due to

* [[Charles Rezk]], _Fibrations and homotopy colimits of simplicial sheaves_ ([pdf](http://www.math.uiuc.edu/~rezk/rezk-sharp-maps.pdf))

More on this with an eye on [[associated ∞-bundles]] is in 

* [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_ ([arXiv](http://arxiv.org/abs/1009.2930))

### Homotopy type theory

Proof that all [[∞-stack]] [[(∞,1)-topos]] have [[presentable (∞,1)-category|presentations]] by [[model categories]] which interpret (provide [[categorical semantics]]) for [[homotopy type theory]] with [[univalence|univalent]] [[type universes]]:

* {#Shulman19} [[Michael Shulman]], _All $(\infty,1)$-toposes have strict univalent universes_ ([arXiv:1904.07004](https://arxiv.org/abs/1904.07004)).



[[!redirects (infinity,1)-topos]]
[[!redirects (infinity,1)-topoi]]
[[!redirects (infinity,1)-toposes]]
[[!redirects (∞,1)-topos]]
[[!redirects (∞,1)-topoi]]
[[!redirects (∞,1)-toposes]]

[[!redirects Grothendieck (infinity,1)-topos]]
[[!redirects Grothendieck (infinity,1)-topoi]]
[[!redirects Grothendieck (infinity,1)-toposes]]
[[!redirects Grothendieck (∞,1)-topos]]
[[!redirects Grothendieck (∞,1)-topoi]]
[[!redirects Grothendieck (∞,1)-toposes]]

[[!redirects Grothendieck-Rezk-Lurie (infinity,1)-topos]]
[[!redirects Grothendieck-Rezk-Lurie (infinity,1)-topoi]]
[[!redirects Grothendieck-Rezk-Lurie (infinity,1)-toposes]]
[[!redirects Grothendieck-Rezk-Lurie (∞,1)-topos]]
[[!redirects Grothendieck-Rezk-Lurie (∞,1)-topoi]]
[[!redirects Grothendieck-Rezk-Lurie (∞,1)-toposes]]
[[!redirects Grothendieck?Rezk?Lurie (infinity,1)-topos]]
[[!redirects Grothendieck?Rezk?Lurie (infinity,1)-topoi]]
[[!redirects Grothendieck?Rezk?Lurie (infinity,1)-toposes]]
[[!redirects Grothendieck?Rezk?Lurie (∞,1)-topos]]
[[!redirects Grothendieck?Rezk?Lurie (∞,1)-topoi]]
[[!redirects Grothendieck?Rezk?Lurie (∞,1)-toposes]]
[[!redirects Grothendieck--Rezk--Lurie (infinity,1)-topos]]
[[!redirects Grothendieck--Rezk--Lurie (infinity,1)-topoi]]
[[!redirects Grothendieck--Rezk--Lurie (infinity,1)-toposes]]
[[!redirects Grothendieck--Rezk--Lurie (∞,1)-topos]]
[[!redirects Grothendieck--Rezk--Lurie (∞,1)-topoi]]
[[!redirects Grothendieck--Rezk--Lurie (∞,1)-toposes]]

[[!redirects (infinity,1)-Giraud theorem]]
[[!redirects (∞,1)-Giraud theorem]]

[[!redirects infinity,1-topos]]
[[!redirects infinity1-topos]]
