
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

## Definition

An [[(∞,1)-category]] $C$ has [[finite limit|finite]] [[(∞,1)-limits]] if it has a [[terminal object in a quasi-category|terminal object]] and for every [[object]] $x \in C$, the [[over-(∞,1)-category]] $C_{/x}$ has finite [[products]]. 

We say that such a $C$ is **locally cartesian closed** if moreover $C_{/x}$ is a [[cartesian closed (∞,1)-category]] for every object $x$.  This is equivalent to asking that the pullback functor $f^*\colon C_{\y} \to C_{\x}$, for any $f\colon x\to y$ in $C$, has a right adjoint $\Pi_f$.

## Examples

* Every (Grothendieck) [[(∞,1)-topos]] is locally cartesian closed.  This follows from the [[universal colimit|universality of colimits]] and the [[adjoint functor theorem]].

## Properties
 {#Properties}


### Presentations
 {#Presentations}

The following theorem should be compared with the fact that every [[locally presentable (∞,1)-category]] admits a presentation by a [[Cisinski model category]], indeed by a [[left Bousfield localization]] of a [[global model structure on simplicial presheaves]].

+-- {: .num_theorem #PresentationTheorem}
###### Theorem
For a locally presentable $(\infty,1)$-category $C$, the following are equivalent.

1. $C$ is locally cartesian closed.

1. [[(∞,1)-colimit|(∞,1)-Colimits]] in $C$ are [[universal colimits|stable under pullback]].

1. $C$ admits a presentation by a [[combinatorial model category|combinatorial]] [[locally cartesian closed model category]].

1. $C$ admits a presentation by a [[right proper model category|right proper]] [[Cisinski model category]].

1. $C$ admits a [[presentable (infinity,1)-category|presentation]] by a [[right proper model category|right proper]] [[Bousfield localization of model categories|left Bousfield localization]] of an [[model structure on simplicial presheaves|injective]] [[model structure on sSet-enriched presheaves]] over some small [[sSet-site]] (see [[model structure on simplicial presheaves#Properness|here]] for sufficient conditions).


=--

+-- {: .proof}
###### Proof

Since [[left adjoints]] preserve colimits, the first condition implies the second.  The converse holds by the [[adjoint functor theorem]] since each slice of $C$ is locally presentable.

Suppose $M$ is a right proper Cisinski model category.  Then pullback along a fibration preserves cofibrations (since they are the monomorphisms) and weak equivalences (since $M$ is right proper).  Since $M$ is a locally cartesian closed 1-category, pullback also has a right adjoint, so it is a [[Quillen adjunction|left Quillen functor]]; thus the fourth condition implies the third.  Since left Quillen functors preserve homotopy colimits, the third condition implies the second.

The fifth condition implies the fourth, since the model structure therein is Cisinski.  The only nonobvious part of this is that its underlying category is a topos, which follows from the fact that $sSet$-enriched presheaves on a $sSet$-enriched category $C$ can be identified with [[internal diagrams]] on $C$ regarded as an [[internal category]] in $sSet$, and the category of internal diagrams on any internal category in a topos (such as $sSet$) is again a topos.

It remains to show that the second condition implies the fifth.  For that, see [this blog comment](http://golem.ph.utexas.edu/category/2012/05/the_mysterious_nature_of_right.html#c041306) by [[Denis-Charles Cisinski]].  An alternative proof can be found in [(Gepner-Kock 12, Thm 7.10)](#GepnerKock12).

=--

+-- {: .num_remark }
###### Remark

Further equivalent characterizations of locally cartesian closed $(\infty,1)$-categories are in 
([Lurie, prop. 6.1.1.4, lemma 6.1.3.3](#Lurie))

=--

+-- {: .num_remark }
###### Remark

Comparing the third and the fifth item in theorem \ref{Presentations}
notice that the projective and the injective [[model structure on simplicial presheaves]] are [[Quillen equivalence|Quillen equivalent]] (as discussed at _[[model structure on functors]]_.)

=--


### Internal logic and homotopy type theory
 {#InternalLogic}

It is expected that the [[internal logic]] of locally cartesian closed $(\infty,1)$-categories should be a sort of [[homotopy type theory]] (specifically, that with intensional [[identity types]] and [[dependent products]]), in higher analogy with the [[relation between type theory and category theory]].  More specifically, the following are hoped to be true:

* From any type theory, its [[syntactic category]] is (or gives rise to) an $(\infty,1)$-category, which is the [[initial object]] in an appropriate $(\infty,1)$-category (or perhaps $(\infty,2)$-category) of locally cartesian closed $(\infty,1)$-categories (perhaps with additional structure corresponding to additional axioms or rules in the type theory).  Thus, type theory can be "interpreted" in any lcc $(\infty,1)$-category by way of the universal morphism from this initial object.

* From any locally cartesian closed $(\infty,1)$-category $C$, one can construct a type theory with rules or axioms corresponding to its objects and morphisms, which has a canonical interpretation in $C$ itself.  This would be the "internal language" of $C$.

* These construction should set up some sort of adjunction, or perhaps equivalence, between some $(\infty,1)$- or $(\infty,2)$-category of type theories and that of lcc $(\infty,1)$-categories.

Some partial results in these directions are known.  For instance, Theorem \ref{Presentations} says in particular that every *locally presentable* and locally cartesian closed $(\infty,1)$-category has a presentation by a [[type-theoretic model category]].  As discussed there, this provides [[categorical semantics]] for [[homotopy type theory]] (without in general the [[univalence]] [[axiom]]), at least if we assume the initiality of the syntactic 1-category (which is known in a special case and expected to be true in all cases).  Together, this yields:

+-- {: .num_theorem #InterpretationTheoemForHoTT}
###### Theorem
**(Cisinski, Shulman)** Assuming the initiality of the syntactic 1-category, every locally presentable locally cartesian closed $(\infty,1)$-category admits an interpretation of [[Martin-Löf type theory]] with [[dependent sum types]], [[dependent product types]], and [[identity types]] ("[[homotopy type theory]]").

Moreover it also interprets [[function extensionality]] ([Shulman 12, lemma 5.9](#Shulman12), see this [this discussion](function+extensionality#EveryPresentableLocallyCartesinClosedInfinityCatInterpretsHoTTPlusFunExt).

Hence every presentable locally cartesian closed $\infty$-category interprets [[HoTT]]+[[FunExt]].


=--

{#UnivalentUniverses} This includes in particular all ([[∞-stack]]-) [[(∞,1)-toposes]], which in addition interpret [[univalence axiom|univalent]] [[type universes]] ([[(infinity,1)-topos#Shulman19|Shulman 19]]).

This statement is not fully satisfactory for several reasons.  Firstly, it assumes local presentability.  Secondly, rather than staying in the world of $(\infty,1)$-categories, it goes by way of a strict presentation.  Thus, the existence and behavior of a "universal model" is unclear.

A step in the latter direction was conjectured in ([Joyal 2011](#Joyal11)), and established in [[Chris Kapulkin]]'s PhD thesis (see [Kapulkin 14](#Kapulkin14), [Kapulkin 15](#Kapulkin15)): 

+-- {: .num_theorem }
###### Theorem
**(Kapulkin)** If **T** is any [[dependent type theory]] with (at least) $\Sigma$-types, $\Pi$-types, and $\mathrm{Id}$-types, then the [[simplicial localisation]] of its [[syntactic category|classifying category]] $\mathrm{Cl}(\mathbf{T})$ is a locally cartesian closed $(\infty,1)$-category.
=--

However, this "syntactic $(\infty,1)$-category" will not in general be locally presentable, lacking appropriate colimits.  There is thus a mismatch between the two best statements we have at present, for the two directions of the internal language correspondence.

{#Initiality} Furthermore, the *initiality* of this syntactic $(\infty,1)$-category is subtle (see at *[[initiality conjecture]]*), but such initiality is a central aspect of what it means to have an internal language.  Finally, no one has yet explicitly constructed an "internal language" type theory from an $(\infty,1)$-category, and so of course the desired adjunction/equivalence cannot yet even be stated as a precise conjecture.



## Related concepts

* [[cartesian closed category]], [[locally cartesian closed category]]

* [[cartesian closed functor]], [[locally cartesian closed functor]]

* [[cartesian closed model category]], [[locally cartesian closed model category]]

* [[cartesian closed (∞,1)-category]], **locally cartesian closed (∞,1)-category**

## References

Characterizations of locally presentable locally cartesian closed $(\infty,1)$-categories (as [[locally presentable (∞,1)-categories]] with [[universal colimits]]) are discussed in section 6.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}

Early discussion in the context of [[homotopy type theory]] is 

* {#Joyal11} [[André Joyal]], _Remarks on homotopical logic_, Oberwolfach (2011) ([pdf](http://hottheory.files.wordpress.com/2011/06/report-11_2011.pdf#page=19))
 
proposing [[homotopy type theory]] as an internal language for locally cartesian closed $\infty$-categories ([[Awodey's conjecture]]).

[[Denis-Charles Cisinski]]'s argument in Theorem \ref{Presentations} above, that every locally presentable locally cartesian closed $(\infinity,1)$-category admits a presentation by a [[type-theoretic model category]], originally appeared on the Caf&#233; ([this blog comment](http://golem.ph.utexas.edu/category/2012/05/the_mysterious_nature_of_right.html#c041306)) and is mentioned in print in Examples 2.16 of 

* {#Shulman12} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_, Mathematical Structures in Computer Science, Volume 25, Issue 5 ( _From type theory and homotopy theory to Univalent Foundations of Mathematics_ ) June 2015 ([arXiv:1203.3253](https://arxiv.org/abs/1203.3253), [doi:/10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565))

which gives a detailed account of the categorical semantics of homotopy type theory in [[type-theoretic model categories]] such as those presenting locally cartesian closed $(\infty,1)$-categories.

For more on this see also the relevant sections at _[[relation between type theory and category theory]]_.

Discussion of the converse direction, obtaining locally cartesian closed $(\infty,1)$-categories as [[syntactic categories]] of [[homotopy type theory|homotopy type theories]] is in 

* {#Kapulkin14} [[Chris Kapulkin]], _Type theory and locally cartesian closed quasicategories_, Oxford 2014 ([video](https://www.youtube.com/watch?v=g87bZJ2bvYk))

* {#Kapulkin15} [[Chris Kapulkin]], _Locally Cartesian Closed Quasicategories from Type Theory_ ([arXiv:1507.02648](http://arxiv.org/abs/1507.02648))

A discussion of object classifiers, univalent families, and model category presentations is the context of $(\infty,1)$-categories (and hence in categorical semantics for what should be homotopy type theory with univalent universes "weakly a la Tarski") appeared also in

* {#GepnerKock12} [[David Gepner]], [[Joachim Kock]], "Univalence in locally cartesian closed ∞-categories", [arXiv](http://arxiv.org/abs/1208.1749)


[[!redirects locally cartesian closed (∞,1)-category]]
[[!redirects locally cartesian closed (infinity,1)-categories]]
[[!redirects locally cartesian closed (∞,1)-categories]]
[[!redirects locally cartesian closed infinity,1-category]]

[[!redirects locally Cartesian closed (∞,1)-category]]
[[!redirects locally Cartesian closed (∞,1)-categories]]
[[!redirects locally Cartesian closed (infinity,1)-category]]
[[!redirects locally Cartesian closed (infinity,1)-categories]]

[[!redirects locally Cartesian closed infinity,1-category]]
[[!redirects locally Cartesian closed infinity,1-categories]]
