
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents


## Overview

There are two big questions about [[category theory]] and the logical [[foundations of mathematics]]:

 1. What foundations are adequate to formulate category theory?
 2. How can category theory provide a foundation for mathematics?

These questions also apply to [[higher category theory]], which also involves the relation between them. (2-categories as a foundation for categories, for example.)

## Mathematical foundations of category theory
{#MFCT}

The problem with mathematical foundations of category theory is that in category theory we frequently speak of [[large category|large categories]], which it is tricky to deal with rigorously in the usual sort of [[set theory|set theories]].

One common view seems to be to found category theory on a theory of sets and classes; see [the English Wikipedia\'s definition](https://en.wikipedia.org/wiki/Category_%28mathematics%29#Definition), for example. But the standard reference, Saunders Mac Lane\'s _Categories for the Working Mathematician_, assumes the existence of a universe (an inaccessible cardinal) instead. Both of these approaches rely on a distinction between *small* and *large* categories. There is a category of all [[small category|small categories]], but this category is not itself small; there is no category of all categories.

[[Alexander Grothendieck]] used more (although [apparently](http://permalink.gmane.org/gmane.science.mathematics.categories/6847) he did not need to); he used what we now call [[Grothendieck universes]]\. He assumed that every set is contained within a universe; that is, for every cardinal number $\kappa$, there is a cardinal inaccessible from $\kappa$. (This is still a rather moderate axiom, compared to some of the large-cardinal axioms studied by set theorists.) Now one has a relative notion of small and large; the category of all $U$-small categories (where $U$ is some universe) is $U$-large but must be $U'$-small for some other universe $U'$, and there exists a category (which is both $U$-large and $U'$-large) of all $U'$-small categories.

If one does not accept the [[axiom of choice]], then there are additional complications in general category theory. In particular, one must distinguish between a universal *property* (for example, having all [[product]]s) and having a universal *structure* realising that property (in the example, a functor taking each pair $(x,y)$ of objects to a specific product cone $x \leftarrow x \times y \rightarrow y$). This difficulty was overcome by Michael Makkai using [[anafunctor]]s, but these have not been widely adopted, even by constructivists.

For a discussion of set theoretic foundations of category theory see the references [below](#ReferencesSetTheoreticFoundationsOfCategoryTheory).


### The concept of _identity_
{#Identity}

One way to think of category theory is as a framework in which the idea is formalized that every kind of [[equality]] is really secretly a choice of [[isomorphism]] or [[equivalence]]. In some sense the notion of identity potentially breaks the [[principle of equivalence]].

[[Michael Makkai]] works on a language, [[FOLDS]] ('first-order logic with dependent sorts'), which is designed to make it impossible to formulate any statements that break the [[principle of equivalence]].


## Categorial foundations of mathematics
{#CFM}

[[Bill Lawvere]] proposed to found mathematics on [[ETCC]] (for ' Elementary Theory of the Category of Categories'), a first-order axiomatisation of [[Cat|the category of categories]]. This has not been very successful, 
but his other proposal, a first-order axiomatisation of [[Set|the category of sets]], works well. These and related approaches to foundations may be called _structural_ or _categorial_ (or _categorical_, which is more common but clashes with another sense of 'categorical' in logic).


Lawvere\'s system [[ETCS]] (for 'the Elementary Theory of the Category of Sets') essentially states that the category of sets is a [[topos]] with certain properties, in particular a [[well-pointed topos]]. This can be stated in elementary (first-order) terms; indeed, the system of axioms for ETCS in 1965 was retrospectively an important step in Lawvere's quest to give a first-order axiomatization for the topos concept that was originally formulated in higher-order terms by the Grothendieck school, resulting in 1970 in the by the now-default notion of *elementary* topos that subsumes the original notion, now called [[Grothendieck topos]], as an important special case.

It is also possible to found mathematics on the [[internal logic|internal language]] of a topos. In this case, the topos need *not* be well-pointed (and indeed, the condition that a topos be well-pointed cannot be stated in its own internal language; or if you prefer, *every* topos is well-pointed *internally*). This is equivalent to a certain formulation of [[type theory]], so it is (in a sense) nothing new, although it leads to new perspectives, as in the next paragraph.

Categories (not just toposes) can serve as models of [[type theory|type theories]], each type theory corresponding to a certain class of categories. Toposes correspond directly to a constructive but impredicative type theory; to make the theory predicative (in the constructivists\' sense) you generalise to a [[pretopos]] (maybe [[locally cartesian closed category|locally cartesian closed]]), to make the theory nonconstructive you specialise to a [[Boolean topos]], and so on. More specifically, every category\'s internal language is a type theory (with many odd constants), and every type theory (of appropriate form) defines a category (its free model); this is an [[adjunction]] between categories and type theories. [[Paul Taylor]]\'s book _[[Practical Foundations|Practical Foundations of Mathematics]]_ is essentially all about this subject, as is (at a more advanced level) most of the career of [[Michael Makkai]].

[[Jim Lambek]] proposed to use the [[free topos]] as ambient world to do mathematics in. Being syntactically constructed, but universally determined, with higher-order [[intuitionistic type theory]] as [[internal language]] he saw it as a reconciliation of the three classical schools of [[philosophy of mathematics]], namely [[formalism]], [[platonism]], and [[intuitionism]]. His latest views on this variant of categorical foundations can be found in ([Lambek-Scott 2011](#LS11)).

Certain 'strong' axioms of [[set theory]] (those involving [[quantification]] over all sets) are difficult to state in category-theoretic (or type-theoretic) terms, but this can be overcome in a theory like ETCS; talk to Mike Shulman. (Ironically, this makes it harder to do foundations with categorial foundations!)

In contrast, many of the optional or controversial axioms of set theory (such as the [[axiom of choice]]) can be stated quite directly in ETCS. These can be examined quite well in a na&#239;ve set-theoretic language that never need be precise about whether one\'s foundations are traditional (membership-based), categorial, or whatever.

## Categorial foundations of category theory
{#CFCT}

Relevant topics: [[ETCC]], [[FOLDS]], [[homotopy type theory]]

## Related topics

* [[foundations of mathematics]]

* [[category theory]]

* [[univalent foundations of mathematics]]

## References

### General

* [[William Lawvere]], _Foundations and applications: axiomatization and education_, Bulletin of Symbolic Logic 9 (2003), 213-224 ([ps](http://www.math.ucla.edu/~asl/bsl/0902/0902-006.ps), [Euclid](http://projecteuclid.org/euclid.bsl/1052669290))

The following contains a careful discussion of [[Gödel's incompleteness theorem]] in the context of categorical foundations using the free topos:

* [[Jim Lambek]], [[Phil Scott]], _Reflections on Categorical Foundations of Mathematics_ , pp.171-185 in  Sommaruga (ed.), _Foundational Theories of Classical and Constructive Mathematics_,  Springer New York 2011. ([draft](https://www.site.uottawa.ca/~phil/papers/LS11.final.pdf)) {#LS11}

Some old discussions about category theory and foundations are archived [here](http://nforum.ncatlab.org/discussion/4172/foundation-of-mathematics/?Focus=33992#Comment_33992)

### Set theoretic foundations of category theory
 {#ReferencesSetTheoreticFoundationsOfCategoryTheory}

Without assuming  [[Grothendieck universes]]:

* {#Rao06} [[Vidhyanath K. Rao]], _On Doing Category Theory within Set Theoretic Foundations_ in: Giandomenico Sico (ed.), _What is category theory?_, Polimetrica (2006) &lbrack;[[Rao-CategoryTheory.pdf:file]], [semanticscholar](https://www.semanticscholar.org/paper/What-is-category-theory-Sica/7737401202b220f89ae9c11cf9af65995a4dcf50)&rbrack;, 

Via [[Grothendieck universes]]:

* [[Horst Schubert]], §3 in: *Categories*, Springer (1972) &lbrack;[doi:10.1007/978-3-642-65364-3](https://doi.org/10.1007/978-3-642-65364-3)&rbrack;

* [[Mike Shulman]], _Set theory for category theory_ &lbrack;[arXiv:0810.1279](http://arxiv.org/abs/0810.1279)&rbrack;

* {#Murfet06} [[Daniel Murfet]], _Foundations for category theory_ (2006) &lbrack;[pdf](http://therisingsea.org/notes/FoundationsForCategoryTheory.pdf), [[Murfet-GrothendieckUniverses.pdf:file]]&rbrack;

* [[Zhen Lin Low]], _Universes for category theory_ &lbrack;[arxiv/1304.5227](http://arxiv.org/abs/1304.5227)&rbrack;

* [[Paul Blain Levy]], _Formulating Categorical Concepts using Classes_ &lbrack;[arXiv:1801.08528](https://arxiv.org/abs/1801.08528)&rbrack;



