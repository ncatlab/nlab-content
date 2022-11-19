
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

A class is a [[proposition]] or [[truth value]] in the [[context]] of a [[set]] [[free variable]]. 

Classes are usually used as a primitive notion in [[class theory]], where [[sets]] are a derived notion from classes, and the classes which are not sets are called **proper classes**. 

In [[set theories]], classes are not part of the theory itself; instead, provided we have a notion of [[universe]] in the [[set theory]], we have a notion of **internal class** derived from [[universes]] $U$ as a [[function]] from $U$ to the [[set]] of [[truth values]], or if the set theory does not have a set of truth values, a [[function]] from $U$ to the [[set]] of [[subsingletons]] in $U$. 

A similar thing happens in [[dependent type theory]] with [[Tarski universes]] $U$, but since not every [[type]] is a [[set]], one has to restrict to the type of $U$-small sets $\mathrm{Set}_U$ and define a class as a function from $\mathrm{Set}_U$ to the [[type of all propositions]], or if the [[dependent type theory]] is [[weakly predicative]], a class would have to be defined as as a function from $\mathrm{Set}_U$ to the type of $U$-small propositions $\mathrm{Prop}_U$. In addition, one could use the [[material set theory|material]] [[cumulative hierarchy]] [[higher inductive type]] relative to $U$, $V_U$, in place of the type of $U$-small sets, $\mathrm{Set}_U$, in either type-theoretic definition, to get **material classes**. 

In all cases, these are useful to address size issues in foundations, and in particular, are used in [[category theory]] for defining various [[locally small categories]] and [[large categories]]. 

The definition of a class in [[dependent type theory]] as a function from $\mathrm{Set}_U$ to $\mathrm{Prop}_U$ implies that a class could also be defined in [[set-level type theory|set-level]] [[dependent type theory]] as a generalized [[modal operator]] which turns a [[set]] or [[type]] into an [[h-proposition]] and isn't required to be [[idempotent]] or [[monadic]]. 

## Definitions

### Classes as propositions/truth values

There are multiple ways to define a class in different [[foundations of mathematics]]. Let us work in [[natural deduction]]. 

* Suppose we are given an [[unsorted set theory]] as [[logic over type theory]] whose objects are [[sets]]. A **class** $C$ is a [[proposition]] or [[truth value]] in the [[context]] of a [[free variable]] $A$. 
$$\Gamma, A \vert \Phi \vdash C \; \mathrm{prop}$$

* Suppose we are given a [[simply sorted set theory]] or [[dependently sorted set theory]] as [[logic over type theory]] with a [[sort]] $\mathrm{Set}$ of [[sets]]. A **class** $C$ is a [[proposition]] or [[truth value]] in the [[context]] of a [[free variable]] for a set $A:\mathrm{Set}$. 
$$\Gamma, A:\mathrm{Set} \vert \Phi \vdash C \; \mathrm{prop}$$

* Suppose we are given an [[unsorted set theory]] as [[logic over type theory]] whose objects are "probable sets", with a [[predicate]] $\mathrm{isSet}(A)$ saying whether a "probable set" $A$ is a set. A **class** $C$ is a [[proposition]] or [[truth value]] in the [[context]] of a [[free variable]] $A$ and the true proposition $\mathrm{isSet}(A) \; \mathrm{true}$. 
$$\Gamma, A \vert \Phi, \mathrm{isSet}(A) \; \mathrm{true} \vdash C \; \mathrm{prop}$$

* Suppose we are given a [[simply sorted set theory]] or [[dependently sorted set theory]] as [[logic over type theory]] with a [[sort]] $\mathrm{ProbSet}$ of "probable sets" with a [[predicate]] $\mathrm{isSet}(A)$ on $\mathrm{ProbSet}$ saying whether a term $A:\mathrm{ProbSet}$ is a set. A **class** $C$ is a [[proposition]] or [[truth value]] in the [[context]] of a [[free variable]] for a probable set $A:\mathrm{ProbSet}$ and the true proposition $\mathrm{isSet}(A) \; \mathrm{true}$. 
$$\Gamma, A:\mathrm{ProbSet} \vert \Phi, \mathrm{isSet}(A) \; \mathrm{true} \vdash C \; \mathrm{prop}$$

* Suppose we are given a [[set-level type theory|set-level]] [[dependent type theory]]. Then a **class** $C$ is a generalized [[modal operator]], which isn't required to be either [[idempotent]] or [[monadic]], on the type theory such that given a [[type]] or [[set]] $A$, the [[type]] or [[set]] $C(A)$ is an [[h-proposition]]. 
$$\frac{\Gamma \vdash A \; \mathrm{set}}{\Gamma \vdash C(A) \; \mathrm{set}} \qquad \frac{\Gamma \vdash A \; \mathrm{set}}{\Gamma \vdash p_A^C \in \mathrm{isProp}(C(A))}$$

### Classes as primitive

There are also [[class theories]] where classes are the primitives:

* Material class theory: Classes are primitives of the theory, and sets are defined as specific kinds of classes.  Examples include [[Morse-Kelley class theory]] and [[von Neumann–Bernays–Gödel class theory]]. 

* Structural class theory: A **class** is an object of a [[category of classes]], and sets are defined as specific kinds of classes. Examples include [[category with class structure]] and the branch of [[algebraic set theory]]

## Internal classes

Provided one has a notion of [[universe]] in the set theory or type theory, it is possible to [[internalization|internalize]] the notion of class inside of the [[set theory]] or [[type theory]] itself. 

### In set theory

There are many notions of [[universe]] in [[set theory]], including [[Grothendieck universes]], [[well-pointed pretopos|well-pointed]] [[Heyting pretopoi]], and [[well-pointed category|well-pointed]] [[division allegories]]. 

Let $U$ be a [[universe]]. Then a **class** relative to $U$ is a [[subset]] $C \subseteq U$ with a given injection $i:C \hookrightarrow U$. If one has choice, any subset comes with a given injection via the [[axiom of choice]]. Thus, by this definition, it is a injective [[family of sets|family of $U$-small sets]]. 

Equivalently, let $\mathrm{Prop}_U$ be the set of [[subsingletons]] in $U$. A **class** relative to $U$ is an [[function]] $f:U \to \mathrm{Prop}_U$. 

### In dependent type theory

In [[dependent type theory]], let $(U, T)$ be a [[univalent universe|univalent]] [[Tarski universe]], let $(\mathrm{Set}_U, \mathrm{Set}_T)$ be the univalent [[h-groupoid]] of $U$-small [[h-sets]], let $V_U$ be the [[material set theory|material]] [[cumulative hierarchy]] [[higher inductive type]] relative to $U$, and let $(\mathrm{Set}_U, \mathrm{Set}_T)$ be the univalent [[h-set]] of $U$-small [[h-propositions]]. Then a **class** is a function $C:\mathrm{Set}_U \to \mathrm{Prop}_U$, and a **material class** is a function $C:V_U \to \mathrm{Prop}_U$. 

## Proper classes

A **proper class** is a class which is not a [[set]]. What not being a set means depends upon the foundation; in [[material set theory]], one would use the property of not being equal to any sets, while in [[structural set theory]], one would use the property of not being in [[bijection]] with any sets. 

In the context of the [[global axiom of choice]], a proper class is a class which can be put in [[bijection]] with the class of all [[ordinal number|ordinals]], $Ord$. 

## Usage

A __[[large category]]__ is a [[category]] whose class of [[morphisms]] is a proper class.  It is sufficient that the class of [[objects]] be a proper class, which is also necessary if the category is [[locally small category|locally small]].

Category theorists care about proper classes because many examples of categories in practice (such as [[Set]], to begin with!) are large.


## Category of classes

The [[category of classes]] is closed under all large [[colimits]]
and [[small limits]].
See the linked article for more information and precise definitions.

Just as an [[elementary topos]] is an axiomatization of basic properties of the category [[Set]], a [[category with class structure]] is an axiomatization of basic properties of the category $Class$.  See also [[algebraic set theory]].

## See also

* [[category of classes]]

* [[type of classes]]

* [[family of sets]]

* [[large set]], [[small set]]

* [[class object]]

## References

For the definition of a material class in [[homotopy type theory]], see section 10.5.3 of:

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

A paper detailing one approach to the technical side of how classes appear in [[category theory]] (namely using [[Grothendieck universes]]) is

* {#Levy18} Paul Blain Levy, _Formulating Categorical Concepts using Classes_ (arXiv:[1801.08528](https://arxiv.org/abs/1801.08528))

[[!redirects class]]
[[!redirects classes]]
[[!redirects internal class]]
[[!redirects internal classes]]
[[!redirects class relative to a universe]]
[[!redirects classes relative to a universe]]

[[!redirects proper class]]
[[!redirects proper classes]]

[[!redirects structural class]]
[[!redirects structural classes]]

[[!redirects material class]]
[[!redirects material classes]]