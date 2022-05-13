
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

This page is to provide non-technical or maybe semi-technical discussion of the nature and role of the [[foundation of mathematics|foundational system]] for [[mathematics]] known as _homotopy type theory_. For more technical details and further pointers see at [[homotopy type theory]].



#Contents#
* table of contents
{:toc}

## FAQ

### What is homotopy type theory?

#### For the person on the street

Homotopy type theory is a theory of objects, which we call terms, collections of objects, which we call types, and equalities between any two objects in a collection, which we call identity types. 

One fundamental aspect of mathematics is that equalities between different collections of objects behave differently from each other. If we have a type where for all terms have exactly one identity between them, this is called a proposition or a truth value. The type with no terms is trivially a proposition, as every single one of the nonexistent terms have exactly one identity between them.

However, not all types are propositions: take the type with two distinct terms $a$ and $b$, there is no identity between $a$ and $b$. The identity types between two terms here are propositions, and the types are called sets. 

Still, not all types are sets: take the type of sets with two terms, the first one with terms $a$ and $b$, and the second one with terms $c$ and $d$. There are two ways to say that these types are equal: by adding an identity between $a$ and $c$ and between $b$ and $d$, or by adding an identity between $a$ and $d$ and between $b$ and $c$. Thus, the identity types between the two sets is set-valued, rather than proposition-valued, and the type is a groupoid, rather than a set. In this way, we could say that, for example, the set of positive integers is equal to the set of negative integers, or that the set of complex numbers is equal to the set of ordered pairs of real numbers. 

One could continue the process, yielding 2-groupoids whose identity types are groupoids, 3-groupoids whose identity types are 2-groupoids, and so forth. And finally, one could have types whose identity types are general types: these types are also known as $\infty$-groupoids. 

#### For set theorists
 {#WhatIsHoTTForSetTheorists}

Homotopy type theory is a refinement of [[constructive set theory]] that takes fully seriously the constructive nature also of [[identity types|identity]]. (As with all [[constructive mathematics]], with the relevant [[axioms]] added, this subsumes, rather than excludes, classical mathematics, see below at _[Is HoTT limited to constructive mathematics?](#IsHoTTLimitedToConstructiveMathematics)_.)

It is this insistence on constructive witnesses for identity and on witnesses for identity of such witnesses, and so ever on, that makes what in traditional [[set theory]] are just [[sets]] (whose elements are either equal or not) in homotopy type theory instead be [[groupoids]] (whose elements may have non-trivial [[isomorphism]] between them) and indeed [[2-groupoids]] (with isomorphisms between these isomorphisms) and so ever on; hence what makes what used to be just [[sets]] be what is kown as _[[∞-groupoids]]_ or _[[homotopy types]]_.


More technically, restriction to the [[0-truncated types]] in HoTT (the "[[h-set]]s") gives a [[predicative topos]] "of sets", and a [[topos]] if one allows the [[resizing axiom]] (details are [here](http://ncatlab.org/nlab/show/set%20theory#ReferencesInHomotopyTypeTheory)). When adding the [[axiom of choice]] to HoTT, one obtains a model of [[ETCS]].
The iterative notion of set can also be captured. Aczel's sets-as-trees interpretation gives a model of constructive set theory [[CZF]]. Again by adding choice to HoTT, one obtains a model of [[ZFC]]; see Ch10 of the HoTT book.

Conversely HoTT has [[models]] in [[ZFC]] (+a number of [[Grothendieck universes]] to model the type theoretic universes), namely in structures called _[[(∞,1)-toposes]]_ which are presented by [[presheaves]] of [[simplicial sets]]. (See also at _[Does HoTT have models in infinity-toposes?](#InterpretationInInfinityToposes)_)

The nature and role of these higher toposes in HoTT may be understood by analogy with the familar [[forcing]] [[models]]:
When one proves something in [[ZF]], it is automatically also true in all [[forcing]] extensions.  The same is true for [[constructive set theory]], except that there are more forcing extensions since we don't have to force the [[law of excluded middle]]; those constructive notions of forcing (which also subsume [[permutation models]]) are called "[[sites]]" and their [[models]] are called "[[topos|1-toposes]]".  Now in HoTT we have an even more general sort of forcing appropriate for [[homotopy theory]], called [[(∞,1)-sites]], whose models are called [[(∞,1)-toposes]].

#### For type theorists

(...)

#### For homotopy theorists

(...)


### Why should I care?
 {#WhyShouldICare}

#### For the person on the street

Homotopy type theory is a foundation upon which all of mathematics is based upon. Every collection of objects in mathematics, such as the collection of natural numbers, collection of real numbers, collection of strings of characters in an alphabet, collection of propositions and the collection of all sets, is represented in homotopy type theory. It is also a language in which one could do mathematics in, from algebra to geometry to calculus. 

#### For set theorists
 {#WhyShouldICareForSetTheorists}

Traditional [[set theory]] is formulated in [[first-order logic]]. Under the [[propositions as types]] interpretation, first order logic maps soundly and completely into [[type theory]] ([Martin-L&#246;f 74, section 3.1](type+theory#MartinLoef74), [Barendregt 91, section 4](pure+type+system#Barendregt91)). But now the [[homotopy 0-types]] in [[homotopy type theory]] already give a [[constructive set theory]], natively, without further axiomatization. See at _[[h-set]]_ for more.

#### For type theorists



#### For homotopy theorists
 {#WhyShouldICareForHomotopyTheorists}

Most homotopy-theoretic theorems that are proven in the [[Homotopy Type Theory -- Univalent Foundations of Mathematics|HoTT textbook]] are, in their traditional informal version, material of a first-year course on homotopy theory. Experts who do not care about [[formal proof]] might not be impressed yet. 

But the point is that there is significant prospect. By the discussion at _[Does HoTT have models in infinity-toposes](#InterpretationInInfinityToposes)_, it is a fact that homotopy type theory is the [[internal language]] of [[(∞,1)-toposes]], hence of the most powerful modern incarnation of [[homotopy theory]]. Whether or not anyone has already made impressive use of this fact (but see below), this is of genuine interest in homotopy theory irrespective of the issue of formal proof.

Historically, making use of the [[internal logic]]-perspective of [[elementary toposes]] led to substantial insight into all theory that uses [[Grothendieck toposes]], such as notably [[algebraic geometry]]. While [[Jacob Lurie|Lurie]]'s book _[[Higher Topos Theory]]_ based on [[Charles Rezk]]'s note _[Homotopy Topos Theory](infinity,1-topos#Rezk10)_ is an astounding piece of work, it falls short of saying anything about this crucial internal aspect of (higher) topos theory. Homotopy type theory is precisely what fills this gap. For more on how this works see at _[[HoTT methods for homotopy theorists]]_.

An illustration of the use of this is the proof of the _[[Blakers-Massey theorem]]_. This basic fact of homotopy theory has a classical proof in the classical homotopy category [[∞Grpd]] $\simeq$ $L_{whe}$ [[Top]], a proof that is however rather roundabout. From this follows a proof in all [[(∞,1)-toposes]] with an [[(∞,1)-site]] of definition by, essentially, reducing [[stalk|stalkwise]] to the classical theorem (details are [here](Blakers-Massey%20theorem#Rezk10)). But now the theorem was also proven in homotopy type theory (details are [here](Blakers-Massey%20theorem#LumsdaineFinsterLicata13)). Translating this formal proof back to ordinary language produces first of all a _new_ and more elegant proof of Blakers-Massey in [[∞Grpd]] $\simeq$ $L_{whe}$ [[Top]], second a new and elegant proof of the statement for [[(∞,1)-toposes]] with [[(∞,1)-site]] of definition. This is something that some homotopy theorists tried to find by classical means and failed (details are [here](Blakers-Massey%20theorem#Rezk14)). And moreover, the HoTT proof of Blakers-Massey is actually a new result when applied to [[elementary (∞,1)-toposes]], where the classical methods of proving it completely break down.

It seems rather plausible that this is just a simple first example of a future where HoTT methods allow to enter new territory in classical homotopy theory. Of course it will require some expert homotopy theorists to seriously look into the internal-language-of-$\infty$-toposes way of doing homotopy theory. This is now an open problem for homotopy theorists just as it is for type theorists.





### What role does the univalence axiom play?
 {#WhatRoleDoesTheUnivalenceAxiomPlay}

#### For the person on the street

The [[axiom]] of [[univalence]] may be thought of as a [[formal logic|formalization]] of what might be called the _[[principle of equivalence]]_ of [[mathematics]], which is the basic but important idea that [[mathematical structures]] which are [[equivalence|equivalent]] should behave the same, satisfy the same theorems and so forth.

In particular, in elementary [[Euclidean geometry]], two shapes are traditionally said to be equal or congruent to each other if there is an [[isometry]] (distance-preserving transformation) between the two shapes. Usually, this congruence requires the need for a quotient of the isomorphism classes in the category of geometric shapes, but with univalence, one does not need such a construction: equality of shapes is the isometries between the shapes. 

Obvious as this may seem, this principle may be violated in other [[foundations of mathematics]] such as [[ZFC]]. On the other hand, while these models allow such violation, in practice one essentially never wants to use such violation. The univalence axiom hence serves to make formal mathematical foundation be closer to the actual "nature of mathematics", at least to the practice of mathematics. 

#### For set theorists

#### For type theorists

The axiom of [[univalence]] added to [[Martin-Löf type theory]] implies all of the following:

1. [[functional extensionality]]

1. [[quotient types]]

1. [[higher inductive types]] with nontrivial homotopies,

   Which in turn imply a wealth of further structure such as (but not limited to)

   1. [[bracket types]]

   1. etc.


#### For homotopy theorists

In view of the answer at _[Does HoTT have interpretation in infinity-toposes?](#InterpretationInInfinityToposes)_
the [[axiom]] of [[univalence]] axiomatizes the presence of an [[object classifier]] in an [[(∞,1)-topos]] $\mathbf{H}$ (details are [here](univalence+axiom#GepnerKock12)). 

In the default choice $\mathbf{H} = $[[∞Grpd]] $\simeq $ $L_{whe}$[[Top]] of traditonal [[homotopy theory]] this is the [[universal principal ∞-bundle|universal fibration]] over the disjoint union of [[classifying spaces]] $\coprod_{[F]} B Aut(F)$ of the [[automorphism ∞-groups]] of all (small) [[homotopy types]] $[F]$.

Therefore from the axiom of [[univalence]] follows for instance the theory of [[∞-actions]], [[associated ∞-bundles]] and of [[twisted cohomology]] (details are [[schreiber:Principal ∞-bundles -- theory, presentations and applications|here]]).


### What advantages does homotopy type theory have over set theory?

As explained at _[What is HoTT for set theorists?](#WhatIsHoTTForSetTheorists)_, HoTT subsumes [[set theory]]. It has all the advantages that [[structural set theory]] ([[Algebraic set theory]], [[ETCS]]) has over [[material set theory]] ([[ZFC]]), but moreover it allows us to natively capture [[higher category theory|higher categorical]] (more precisely, [[infinity-groupoid|higher groupoidal]]) and [[homotopy theory|homotopical]] reasoning. Moreover, as a practical foundation, set theory may be compared to the Turing machine model, or perhaps more generously, say, [ALGOL](http://en.wikipedia.org/wiki/ALGOL). Whereas, homotopy type theory is closely related to modern programming languages like Haskell and ML, or more accurately [[Coq]] and [[Agda]].

### Is homotopy type theory limited to constructive mathematics?
 {#IsHoTTLimitedToConstructiveMathematics}

No. On the [[0-types]] (the [[h-sets]]) the axioms of [[classical logic]] may be imposed, such as the [[law of excluded middle]] (details are [here](excluded+middle#ReferencesInHomotopyTypeTheory)) and the [[axiom of choice]] (details are [here](axiom+of+choice#ReferencesInHomotopy)).

One [[model]] that interprets the resulting axioms is the standard model in [[simplicial sets]] ([here](model%20structure%20on%20simplicial%20sets#KapulkinLumnsdaineVoevodsky12)) inside [[ZFC]]+[[inaccessible cardinals]]. The [[0-types]] in this model are precisely the ordinary sets in ZFC. See also the discussion at _[What is HoTT? For set theorists](#WhatIsHoTTForSetTheorists)_.

For more exposition see also

* [[Andrej Bauer]], _[Univalent foundations subsume classical mathematics](http://math.andrej.com/2014/01/13/univalent-foundations-subsume-classical-mathematics/)_ (2013)


### Does HoTT have interpretation/semantics/models in $\infty$-toposes?
 {#InterpretationInInfinityToposes}

The short answer is: Yes. Homotopy type theory has [[higher category theory|higher]] [[categorical semantics]] in every [[(∞,1)-topos]], in refinement of how plain [[dependent type theory]] has [[categorical semantics]] in [[toposes]].

The more detailed answer depends on which axiomatics precisely one subsumes under "homotopy type theory". A hierarchy of three main variants ("fragments") of homotopy type theory should be distinguished here:

1. HoTT without [[univalence|univalent]] [[type universes]];

1. HoTT with [[univalence|univalent]] weak [[type universes]]   [&#224; la Tarski](type%20of%20types#TarskiStyle);

1. HoTT with [[univalence|univalent]] strict [[type universes]]  [&#224; la Russell](type%20of%20types#RussellStyle) or [&#224; la Tarski](type%20of%20types#TarskiStyle);

In all three cases the $\infty$-categorical semantics is induced by ordinary [[categorical semantics]] in a [[type-theoretic model category]] which in turn [[locally presentable (infinity,1)-category|presents]] an [[(∞,1)-category]]. The way this works is reviewed also at _[[HoTT methods for homotopy theorists]]_. This relies on standard techniques for interpreting any [[dependent type theory]] in a [[locally cartesian closed category]] (see [here](relation+between+type+theory+and+category+theory#DependentTypeTheory) for details).

With that understood, the higher categorical semantics for the above three cases is as follows:

1. HoTT without univalent universes has semantics in every [[locally presentable (∞,1)-category|locally presentable]] [[locally cartesian closed (∞,1)-category]] (details are [here](locally+cartesian+closed+%28infinity,1%29-category#InternalLogic)).

1. HoTT with strict univalent universes has semantics at least in [[(∞,1)-category of (∞,1)-presheaves|(∞,1)-presheaf]] [[(∞,1)-toposes]] over [[elegant Reedy categories]]. This includes in particular the standard [[base (∞,1)-topos]] [[∞Grpd]] as well as for instance the [[Sierpinski (∞,1)-topos]] (details are [here](relation+between+type+theory+and+category+theory#Shulman13)).

1. HoTT with weak univalent universes has semantics in every [[(∞,1)-sheaf (∞,1)-topos]] (details are [[homotopytypetheory:model of type theory in an (infinity,1)-topos|here]]).

Since we are assuming [[locally presentable (∞,1)-category|local presentability]] here, all these models have enough [[(∞,1)-colimits]] to interpret [[higher inductive types]]. (One might also ask for models of HoTT without univalence and without higher inductive types and would expect that this then also includes [[locally cartesian closed (∞,1)-categories]] which are not necessarily locally presentable.)

One may also ask about models in [[elementary (∞,1)-toposes]]. Their theory or even definition is however much in the making. On the other hand, existing proposals essentially turn the question around and define [[elementary (∞,1)-toposes]] as [[(∞,1)-categories]] with the minimum of properties such that HoTT may be modeled in them. This reflects the idea that what is "elementary" about elementary $(\infty,1)$-toposes is precisely the fact that there is an internal type theory language for them.

In conclusion, every [[proposition]] [[proof|proven]] in homtopy type theory yields (subject to the above qualification) a statement that holds true in every [[(∞,1)-topos]] (in every presentable [[locally cartesian closed (∞,1)-category]]), i.e. homotopy type theory is the [[internal language]] of $\infty$-toposes. 

If one wishes to prove statements that hold only in some class of $\infty$-toposes, then one needs to add further [[axioms]] to HoTT that characterize these classes. For instance adding [[higher modalities]] that define [[cohesive homotopy type theory]] make it a language that proves theorems which hold in all [[cohesive (∞,1)-toposes]].



### What is meant by a "computational interpretation of univalence"? 


### What are higher inductive types?

### What do we gain by a proof in homotopy type theory of $\pi_1(S^1) = \mathbb{Z}$ over ordinary proofs?

### Is it possible to define higher coinductive types?


### In what sense does homotopy type theory already contain logic?

A [[proposition]] can be defined as a type such that the identity type between any two terms of the type has a term. One could add to homotopy type theory the [[higher inductive type]] of [[propositional truncation]], which takes any type and turns it into a proposition. The propositional truncation of [[product types]] correspond to [[conjunction]], the propositional truncation of [[sum types]] correspond to [[disjunction]], the propositional truncation of [[function types]] correspond to [[implication]], the propositional truncation of [[dependent product types]] correspond to [[universal quantification]], the propositional truncation of [[dependent sum types]] correspond to [[existential quantification]], the [[empty type]] corresponds to [[false]], a [[function type]] into the empty type corresponds to [[negation]], and [[contractible types]] correspond to true. This corresponds to [[constructive logic|constructive]] [[predicate logic]], and the addition of the axiom of [[excluded middle]] to the type theory yields [[classical logic|classical]] [[predicate logic]]. 

### Can category theory be carried out in homotopy type theory?

Yes. One could define a **category** as a type $C$ whose identity types $a =_C b$ for $a:C$ and $b:C$ are sets, with a set $M$ with functions $s:M \to C$, $t:M \to C$, $id:C \to M$ and function 
$$c:\left(\sum_{f:M} \sum_{g:M} t(f) =_C s(g)\right) \to M$$ 
such that $s(c(g,f)) =_C s(f)$ and $t(c(g,f)) =_C t(g)$, for every $f:M$, $c(f, id(s(f))) =_M f$ and $c(id(t(f)), f) =_M f$, and for every $f:M$, $g:M$, and $h:M$ such that $t(f) =_C s(g)$ and $t(g) =_C s(h)$, $c(h,c(g,f)) =_M c(c(h,g),f)$. 

Then one could define a **functor** between categories $(C,M)$ and $(D,N)$ as a function $F:C \to D$ with a function $G:M \to N$ such that for all $f:M$, $F(s_C(f)) =_D s_D(G(f))$ and $F(t_C(f)) =_D t_D(G(f))$, for all $a:C$, $G(id_C(a)) =_N id_D(F(a))$, and for terms $f:M$ and $g:M$ such that $t(f) =_D s(g)$, $G(g \circ_C f) =_N F(g) \circ_D F(h)$. 

### Can $(\infty,1)$-categories be defined in homotopy type theory?

It is currently unknown how to define the [[coherence theorems]] necessary to define $(\infty,1)$-categories in vanilla homotopy type theory. There are other approaches to type theory such as [[directed homotopy type theory]] which might be able to define $(\infty,1)$-categories. 

## Related articles

* [[homotopy theory FAQ]]

[[!redirects HoTT FAQ]]