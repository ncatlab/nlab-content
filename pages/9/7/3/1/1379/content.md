
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

A class is a collection of objects in certain [[foundations]], used to address size issues. Classes could be "small", in which they are usually called **[[sets]]**, or "large", in which they are usually called **proper classes**. Exactly what classes are depends on the [[foundations]] of mathematics (such as material class theory, structural class theory, or type theory). 

Classes are used in [[category theory]] for defining various [[locally small categories]] and [[large categories]], but in either case, the categories used are still [[strict categories]] and violate the [[principle of equivalence]] due to the [[propositional equality]] used for classes.

## Definitions

### Classes

There are multiple ways to define a class. Let us work in the foundations of [[natural deduction]] and the framework of [[logic over type theory]]. 

* Suppose we are given an [[unsorted set theory]] whose objects are "probable sets", with a [[predicate]] $\mathrm{isSet}(A)$ saying whether a "probable set" $A$ is a set. A **class** $C$ is a [[proposition]] in the [[context]] of a [[free variable]] $A$ and the true proposition $\mathrm{isSet}(A) \; \mathrm{true}$. 
$$\Gamma, A \vert \Phi, \mathrm{isSet}(A) \; \mathrm{true} \vdash C \; \mathrm{prop}$$

* Suppose we are given a [[simply sorted set theory]] or [[dependently sorted set theory]] with a [[sort]] $\mathrm{ProbSet}$ of "probable sets" with a [[predicate]] $\mathrm{isSet}(A)$ on $\mathrm{ProbSet}$ saying whether a term $A:\mathrm{ProbSet}$ is a set. A **class** $C$ is a [[proposition]] in the [[context]] of a [[free variable]] for a probable set $\mathrm{ProbSet}$ and the true proposition $\mathrm{isSet}(A) \; \mathrm{true}$. 
$$\Gamma, A:\mathrm{ProbSet} \vert \Phi, \mathrm{isSet}(A) \; \mathrm{true} \vdash C \; \mathrm{prop}$$

There are also [[class theories]] where classes are the primitives:

* Material class theory: Classes are primitives of the theory, and sets are defined as specific kinds of classes.  Examples include [[Morse-Kelley class theory]] and [[von Neumann–Bernays–Gödel class theory]]. 

* Structural class theory: A **class** is an object of a [[category of classes]], and sets are defined as specific kinds of classes. Examples include [[category with class structure]] and the branch of [[algebraic set theory]]

### Classes relative to a universe

There are many notions of [[universe]] in [[set theory]] or [[type theory]], including [[Grothendieck universes]], [[well-pointed pretopos|well-pointed]] [[Heyting pretopoi]], [[well-pointed category|well-pointed]] [[division allegories]], [[Tarski universes]], and models of the material [[cumulative hierarchy]] such as the [[material set theory|material]] [[cumulative hierarchy]] [[higher inductive type]] in [[dependent type theory]]. 

Let $Set$ be a [[universe]] of [[sets]]. Then a **class** relative to $Set$ is a [[subset]] $C \subseteq Set$ with a given injection $i:C \hookrightarrow Set$. If one has choice, any subset comes with a given injection via the [[axiom of choice]]. Thus, by this definition, it is a injective [[family of sets|family of $U$-small sets]]. Equivalently, given some set of [[truth values]], [[subobject classifier]], or [[type of propositions]] $\Omega$, a **class** is a function $C:Set \to \Omega$ from $Set$ into $\Omega$. 

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

## References

For the definition of a class in [[homotopy type theory]], see section 10.5.3 of:

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

A paper detailing one approach to the technical side of how classes appear in [[category theory]] (namely using [[Grothendieck universes]]) is

* {#Levy18} Paul Blain Levy, _Formulating Categorical Concepts using Classes_ (arXiv:[1801.08528](https://arxiv.org/abs/1801.08528))

[[!redirects class]]
[[!redirects classes]]
[[!redirects class relative to a universe]]
[[!redirects classes relative to a universe]]

[[!redirects proper class]]
[[!redirects proper classes]]