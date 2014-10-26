
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

#### For laymen

(...)

#### For set theorists
 {#WhatIsHoTTForSetTheorists}

Homotopy type theory has a model in ZFC (+a number of [[Grothendieck universes]] to model the type theoretic universes). Conversely, 0-truncated types from a [[predicative topos]], and even a [[topos]] if one allows the resizing axiom.
When adding the axiom of choice to HoTT, one obtains a model of [[ETCS]].
The iterative notion of set can also be captured. Aczel's sets-as-trees interpretation gives a model of constructive set theory [[CZF]]. Again by adding choice to HoTT, one obtains a model of [[ZFC]]; see Ch10 of the HoTT book.

When you prove something in [[ZF]], it is automatically also true in all [[forcing]] extensions.  The same is true for [[constructive set theory]], except that there are more forcing extensions since we don't have to force the [[law of excluded middle]]; those constructive notions of forcing (which also subsume [[permutation models]]) are called "[[sites]]" and their [[models]] are called "[[topos|1-toposes]]".  Now in HoTT we have an even more general sort of forcing appropriate for [[homotopy theory]], called [[(∞,1)-sites]], whose models are called [[(∞,1)-toposes]].

#### For type theorists

(...)

#### For homotopy theorists

(...)

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

### What role does the univalence axiom play?

### What is meant by a "computational interpretation of univalence"? 


### What are higher inductive types?

### What do we gain by a proof in homotopy type theory of $\pi_1(S^1) = \mathbb{Z}$ over ordinary proofs?

### Is it possible to define higher coinductive types?

### Is homotopy type theory limited to constructive mathematics?

No. 

For a longer answer, see for instance

* [[Andrej Bauer]], _[Univalent foundations subsume classical mathematics](http://math.andrej.com/2014/01/13/univalent-foundations-subsume-classical-mathematics/)_ (2013)

### What advantages does homotopy type theory have over set theory?

### In what sense does homotopy type theory already contain logic?

### Can category theory be carried out in homotopy type theory?

### Can $(\infty,1)$-categories be defined in homotopy type theory?

