
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[set theory]], a class is a [[proposition]] or [[truth value]] in the [[context]] of a [[set]] [[free variable]]. In [[dependent type theory]] with a [[type universe]] $U$, a class is an [[h-proposition]] in the context of a [[free variable]] $x:U$. 

In [[set-level type theory|set-level]] [[dependent type theory]] with a separate [[set]] or [[type]] [[judgment]] but no [[type universes]], there are no [[set]]/[[type]] free variables. However, one could nevertheless interpret a class in [[dependent type theory]] as a generalized [[modal operator]] on [[sets]]/[[types]] which takes sets to [[h-propositions]] by the [[propositions as some types]] interpretation. If we use the [[propositions as types]] interpretation of [[dependent type theory]], then a class in any [[dependent type theory]] is just a generalized [[modal operator]] on [[sets]]/[[types]]. The generalized modal operators here are not required to be either [[idempotent]] or [[monadic]]. 

One could internalize the notion of class inside of the foundations, and this internal notion of class is used to address size issues in foundations, and in particular, are used in [[category theory]] for defining various [[locally small categories]] and [[large categories]]. 

## Definitions

There are multiple ways to define a class in different [[foundations of mathematics]]. Let us work in [[natural deduction]]. 

* Suppose we are given an [[unsorted set theory]] as [[logic over type theory]] whose objects are [[sets]]. A **class** $C$ is a [[proposition]] or [[truth value]] in the [[context]] of a [[free variable]] $A$. 
$$\Gamma, A \vert \Phi \vdash C \; \mathrm{prop}$$

* Suppose we are given a [[simply sorted set theory]] or [[dependently sorted set theory]] as [[logic over type theory]] with a [[sort]] $\mathrm{Set}$ of [[sets]]. A **class** $C$ is a [[proposition]] or [[truth value]] in the [[context]] of a [[free variable]] for a set $A:\mathrm{Set}$. 
$$\Gamma, A:\mathrm{Set} \vert \Phi \vdash C \; \mathrm{prop}$$

* Suppose we are given an [[unsorted set theory]] as [[logic over type theory]] whose objects are "probable sets", with a [[predicate]] $\mathrm{isSet}(A)$ saying whether a "probable set" $A$ is a set. A **class** $C$ is a [[proposition]] or [[truth value]] in the [[context]] of a [[free variable]] $A$ and the true proposition $\mathrm{isSet}(A) \; \mathrm{true}$. 
$$\Gamma, A \vert \Phi, \mathrm{isSet}(A) \; \mathrm{true} \vdash C \; \mathrm{prop}$$

* Suppose we are given a [[simply sorted set theory]] or [[dependently sorted set theory]] as [[logic over type theory]] with a [[sort]] $\mathrm{ProbSet}$ of "probable sets" with a [[predicate]] $\mathrm{isSet}(A)$ on $\mathrm{ProbSet}$ saying whether a term $A:\mathrm{ProbSet}$ is a set. A **class** $C$ is a [[proposition]] or [[truth value]] in the [[context]] of a [[free variable]] for a probable set $A:\mathrm{ProbSet}$ and the true proposition $\mathrm{isSet}(A) \; \mathrm{true}$. 
$$\Gamma, A:\mathrm{ProbSet} \vert \Phi, \mathrm{isSet}(A) \; \mathrm{true} \vdash C \; \mathrm{prop}$$

* Suppose we are given a [[dependent type theory]] with a [[type universes]] $\mathcal{U}$ and a separate [[type]] [[judgment]], as well as a [[type of all propositions]] $\Omega$. Then a **class** $C$ is a [[proposition]] in the [[context]] of a type $A:\mathcal{U}$
$$\Gamma, A:\mathcal{U} \vdash C:\Omega$$

* Suppose we are given a [[dependent type theory]] with a [[type universes]] $\mathcal{U}$ and a separate [[type]] [[judgment]], and are using the [[propositions as some types]] interpretation of dependent type theory. Then a **class** $C$ is a [[type]] in the [[context]] of a type $A:\mathcal{U}$
$$\Gamma, A:\mathcal{U} \vdash C \; \mathrm{type}$$
with the rule
$$\frac{\Gamma, A:\mathcal{U} \vdash C \; \mathrm{type} \quad \Gamma \vdash B:\mathcal{U}}{\Gamma \vdash p^C(B):\mathrm{isProp}(C[B/A])}$$

* Suppose we are given a [[dependent type theory]] with a [[type universes]] $\mathcal{U}$ and a separate [[type]] [[judgment]], and are using the [[propositions as types]] interpretation of dependent type theory. Then a **class** $C$ is a [[type]] in the [[context]] of a type $A:\mathcal{U}$
$$\Gamma, A:\mathcal{U} \vdash C \; \mathrm{type}$$

* Suppose we are given a [[dependent type theory]] with a [[sequence]] of [[Russell universes]] $\mathcal{U}_i$ but no separate [[type]] [[judgment]], and are using the [[propositions as some types]] interpretation of dependent type theory. Then a **class** $C$ is an [[h-proposition]] in the successor universe $\mathcal{U}_{s_\mathcal{N}(i)}$ in the [[context]] of a type $A:\mathcal{U}_i$
$$\Xi \vert \Gamma, A:\mathcal{U}_i \vdash C:\mathrm{Prop}_{\mathcal{U}_{s_\mathcal{N}(i)}}$$

* Suppose we are given a [[dependent type theory]] with a [[sequence]] of [[Russell universes]] $\mathcal{U}_i$ but no separate [[type]] [[judgment]], and are using the [[propositions as types]] interpretation of dependent type theory. Then a **class** $C$ is a [[type]] in the successor universe $\mathcal{U}_{s_\mathcal{N}(i)}$ in the [[context]] of a type $A:\mathcal{U}_i$
$$\Xi \vert \Gamma, A:\mathcal{U}_i \vdash C:\mathcal{U}_{s_\mathcal{N}(i)}$$

* Suppose we are given a [[dependent type theory]] with a separate [[type]] [[judgment]] but no universes. Then a **class** $C$ is a generalized [[modal operator]] on the type theory, which isn't required to be either [[idempotent]] or [[monadic]], such that given a [[type]] $A$, the [[type]] $C(A)$ is an [[h-proposition]]. 
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash C(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash p_A^C:\mathrm{isProp}(C(A))}$$

* Suppose we are given a [[dependent type theory]] with a separate [[type]] [[judgment]] but no [[type universes]], and are using the [[propositions as types]] interpretation of dependent type theory. Then a **class** $C$ is a generalized [[modal operator]] on the type theory which isn't required to be either [[idempotent]] or [[monadic]]. 
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash C(A) \; \mathrm{type}}$$

## Examples

* In [[set theory]], there is a class $\exists a.a \in A$ for whether the set $A$ is an [[inhabited set]]. In [[dependent type theory]], the class is the [[propositional truncation]] [[modal operator]] $[A]$. 

* In [[set theory]], there is a class $\forall a.a \in A \wedge \forall b.b \in A \wedge a = b$ for whether the set $A$ is a [[subsingleton]]. In [[dependent type theory]], the class is the [[isProp]] [[modal operator]] $\Pi (a:A).\Pi (b:A).(a =_A b)$. 

* In [[set theory]], there is a class $\exists a.a \in A \wedge \forall b.b \in A \wedge a = b$ for whether the set $A$ is a [[singleton]]. In [[dependent type theory]], the class is the [[isContr]] [[modal operator]] $\Sigma (a:A).\Pi (b:A).(a =_A b)$. 

## Internal classes

It is possible to [[internalization|internalize]] the notion of class inside of the [[foundations]] itself. Classes are either primitive, such as in [[class theory]], or a derived concept from a notion of [[universe]] in the foundations, such as in [[set theory]] or [[type theory]]. These internal classes are useful to address size issues in foundations, and in particular, are used in [[category theory]] for defining various [[locally small categories]] and [[large categories]]. 

### Classes as primitive

There are foundational theories called [[class theories]] where classes are primitives, rather than propositions in the context of a free variable $x:\mathrm{Set}$. This is similar to [[dependently sorted set theory|dependently sorted]] [[allegorical set theories]], where [[relations]] are primitives, rather than propositions in the context of free variables $a:A$ and $b:B$. 

* Material class theory: Classes are primitives of the theory, and sets are defined as specific kinds of classes.  Examples include [[Morse-Kelley class theory]] and [[von Neumann–Bernays–Gödel class theory]]. 

* Structural class theory: A **class** is an object of a [[category of classes]], and sets are defined as specific kinds of classes. Examples include [[category with class structure]] and the branch of [[algebraic set theory]]

### Classes as derived from universes

#### In set theory

There are many notions of [[universe]] in [[set theory]], including [[Grothendieck universes]], [[well-pointed pretopos|well-pointed]] [[Heyting pretopoi]], and [[well-pointed category|well-pointed]] [[division allegories]]. 

Let $U$ be a [[universe]]. Then a **class** relative to $U$ is a [[subset]] $C \subseteq U$ with a given injection $i:C \hookrightarrow U$. If one has choice, any subset comes with a given injection via the [[axiom of choice]]. Thus, by this definition, it is a injective [[family of sets|family of $U$-small sets]]. 

Equivalently, a class $C$ relative to $U$ is an [[endofunction]] $C:U \to U$ such that for all $U$-small sets $A \in U$, $C(A)$ is a [[subsingleton]] subset. 

#### In dependent type theory

In [[dependent type theory]], let $(U, T)$ be a [[univalent universe|univalent]] [[Tarski universe]], let $(\mathrm{Set}_U, \mathrm{Set}_T)$ be the univalent [[h-groupoid]] of $U$-small [[h-sets]], let $V_U$ be the [[material set theory|material]] [[cumulative hierarchy]] [[higher inductive type]] relative to $U$. Then a **class** is an [[endofunction]] $C:\mathrm{Set}_U \to \mathrm{Set}_U$ such that for all $U$-small sets $A:\mathrm{Set}_U$, $(C(A))$ is a $U$-small [[h-proposition]], and a **material class** is a function $C:V_U \to \mathrm{Set}_U$ such that for all material sets $A:V_U$, $(C(A))$ is a $U$-small [[h-proposition]]. 

### Proper classes

A **proper class** is a class which is not a [[set]]. What a set is differs from foundations to foundations. 

What not being a set means depends upon the foundation; in [[material set theory]], one would use the property of not being equal to any sets, while in [[structural set theory]], one would use the property of not being in [[bijection]] with any sets. 

Given a notion of [[universe]], a **[[proper class]] relative to $U$** is a class relative to $U$ which is not a set. If classes are defined as subsets of $U$ with an injection into $U$, then a proper class is a class which is not a [[singleton subset]]. 

In the context of the [[global axiom of choice]], a proper class is a class which can be put in [[bijection]] with the class of all [[ordinal number|ordinals]], $Ord$. 

## Category of classes

The [[category of classes]] is closed under all large [[colimits]]
and [[small limits]].
See the linked article for more information and precise definitions.

Just as an [[elementary topos]] is an axiomatization of basic properties of the category [[Set]], a [[category with class structure]] is an axiomatization of basic properties of the category $Class$.  See also [[algebraic set theory]].

## See also

* [[class object]]

* [[class theory]]

* [[category of classes]]

* [[type of classes]]

* [[family of sets]]

* [[large set]], [[small set]]



## References

For the definition of a material class relative to a universe $U$ in [[homotopy type theory]], see section 10.5.3 of:

* [[Univalent Foundations Project]], *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]*, Institute for Advanced Study (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;


A paper detailing one approach to the technical side of how classes appear in [[category theory]] (namely using [[Grothendieck universes]]) is

* {#Levy18} [[Paul Blain Levy]], _Formulating Categorical Concepts using Classes_ &lbrack;[arXiv:1801.08528](https://arxiv.org/abs/1801.08528)&rbrack;

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
