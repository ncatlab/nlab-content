
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A *pseudo-equivalence relation* is like an [[equivalence relation]], but where we allow more than one element in the relation; i.e. the underlying [[directed graph]] of the relation is a [[directed pseudograph]]. In the same way that [[magmoids]] are the raw structure used to build [[semicategories]] and [[categories]], sets with pseudo-equivalence relations are the raw structure used to build [[dagger categories]] and [[groupoids]] (i.e. a groupoid without associativity, unital laws, and inverse laws). 

Sets equipped with pseudo-equivalence relations are sometimes called *[[setoids]]* (i.e. in [Wilander (2012), §4](#Wilander12); [Palmgren & Wilander (2014), §2, §6](#PalmgrenWilander14); [Emmenegger & Palmgren (2020), §6](#EmmeneggerPalmgren20);  [Cipriano (2020), Def. 1.1.1](#Cipriano20)), but the term "setoid" is also used in mathematics to refer only to the sets with [[equivalence relations]]. In this article, the term "setoid" is used in the former sense of "sets equipped with pseudo-equivalence relations". 

## Definition

### With a family of sets

Using graph theoretic terminology, a **pseudo-equivalence relation** on a set $V$ of [[vertices]] is a family of sets $E(a, b)$ of [[edges]] for each vertex $a \in V$ and $b \in V$, which comes with the following additional structure 

* for each vertex $a \in V$ an element
$$\mathrm{refl}(a) \in E(a, a)$$ 

* for each vertex $a \in V$ and $b \in V$ a family of functions
$$\mathrm{sym}(a, b):E(a, b) \to E(b, a)$$

* for each vertex $a \in V$, $b \in V$, and $c \inV$, a family of functions
$$\mathrm{trans}(a, b, c):(E(a, b) \times E(b, c)) \to E(a, c)$$

### With a set

A **pseuodo-equivalence relation** on a [[set]] $V$ is a set $E$ and functions $s:E \to V$, $t:E \to V$ (a loop [[directed pseudograph]]), with with functions $\mathrm{refl}:V \to E$, $\mathrm{sym}:E \to E$, and  
$$\mathrm{trans}:\{(f,g) \in E \times E \vert t(f) =_V s(g)\} \to E$$ 
such that 

* for every $a \in V$, $s(\mathrm{refl}(a)) =_E a$
* for every $a \in V$, $t(\mathrm{refl}(a)) =_E a$
* for every $f \in E$, $s(f) =_V t(\mathrm{sym}(f))$
* for every $f \in E$, $t(f) =_V s(\mathrm{sym}(f))$
* for every $f \in E$ and $g \in E$ such that $t(f) =_V s(g)$, $s(\mathrm{trans}(f,g)) =_E s(f)$ 
* for every $f \in E$ and $g \in E$ such that $t(f) =_V s(g)$, $t(\mathrm{trans}(f,g)) =_E t(g)$

### Extensional functions, dagger functors, and isomorphisms

We define an **[[extensional function]]** $f:A \to B$ between two sets $A$ and $B$ with pseudo-equivalence relations $(E_A, \mathrm{refl}_A, \mathrm{sym}_A, \mathrm{trans}_A)$ and $(E_B, \mathrm{refl}_B, \mathrm{sym}_B, \mathrm{trans}_B)$ to be a function $f_V:A \to B$ and a family of functions $f_E(a, b):E_A(a, b) \to E_B(f_V(a), f_V(b))$

Composition of extensional functions is defined as composition of the vertex function and of each edge function. 

An extensional function between two sets with pseudo-equivalence relations is **full** if every edge function $f_E(a, b):E_A(a, b) \to E_B(f_V(a), f_V(b))$ is a [[surjection]], and an extensional function is **faithful** if every edge function is an [[injection]]. An extensional function is **[[injective-on-objects]]** if the vertex function $f_V:V_A \to V_B$ is an [[injection]], **[[surjective-on-objects]]** if the vertex function is a [[surjection]], and **[[bijective-on-objects]]** if the vertex function is a [[bijection]]. 

An extensional function is a **[[dagger functor]]** if additionally it preserves the functions $\mathrm{refl}$, $\mathrm{sym}$, $\mathrm{trans}$ 
$$f_E(a, a)(\mathrm{refl}_A(a)) = \mathrm{refl}_B(f_V(a))$$
$$f_E(a, b)(\mathrm{sym}_A(a, b)(f)) = \mathrm{sym}_B(f_V(a), f_V(b))(f_E(a, b)(f))$$
$$f_E(a, c)(\mathrm{trans}_A(f,g)) = \mathrm{trans}_B(f_E(a, b)(f), f_E(b, c)(g)$$

An **isomorphism of setoids** is a [[full and faithful]] [[bijective-on-objects]] [[dagger functor]]. 

### Equivalence of definitions

Given a one-set-of-edges setoid $E\rightrightarrows V$, we define a family-of-sets-of-edges setoid by taking $E(x,y)$ to be the [[preimage]] of $(x,y)$ under the [[function]] $(s,t):E \to V\times V$.  Conversely, given a family-of-sets-of-edges setoid we define a one-set-of-edges setoid by taking $E$ to be the [[disjoint union]] of the families of edges $E = \coprod_{x,y\in V} E(x,y)$. 

...

## Examples

The [[morphisms]] $E(a, b)$ of a [[category]] $V$ with a [[contravariant functor|contravariant]] [[endofunctor]] that is the [[identity-on-objects]] is a pseudo-equivalence relation where

* for every vertex $a \in V$, $b \in V$, $c \in V$, and $d \in V$ and edge $f \in E(a, b)$, $g \in E(b, c)$, and $h \in E(c, d)$
$$\mathrm{trans}(a, b, d)(f, \mathrm{trans}(b, c, d)(g, h)) = \mathrm{trans}(a, c, d)(\mathrm{trans}(a, b, c)(f, g), h)$$

* for every vertex $a \in V$, $b \in V$ and edge $f \in E(a, b)$
$$\mathrm{trans}(a, b, b)(f, \mathrm{refl}(b)) = f$$

* for every vertex $a \in V$, $b \in V$ and edge $f \in E(a, b)$
$$\mathrm{trans}(a, a, b)(\mathrm{refl}(a), f) = f$$

This includes [[dagger categories]], where additionally

* for every vertex $a \in V$, $b \in V$ and edge $f \in E(a, b)$
$$\mathrm{sym}(a, b)(\mathrm{sym}(b, a)(f)) = f$$

* for every vertex $a \in V$, $b \in V$, $c \in V$ and edge $f \in E(a, b)$, $g \in E(b, c)$
$$\mathrm{sym}(a, c)(\mathrm{trans}(a, b, c)(f, g)) = \mathrm{trans}(c, b, a)(\mathrm{sym}(a, b)(f), \mathrm{sym}(b, c)(g))$$

* for every vertex $a \in V$
$$\mathrm{sym}(a, a)(\mathrm{refl}(a)) = \mathrm{refl}(a)$$

and [[groupoids]], where

* for every vertex $a \in V$, $b \in V$ and edge $f \in E(a, b)$
$$\mathrm{trans}(a, b, a)(f, \mathrm{sym}(a, b)(f)) = \mathrm{refl}(a)$$

* for every vertex $a \in V$, $b \in V$ and edge $f:E(a, b)$
$$\mathrm{trans}(b, a, b)(\mathrm{sym}(a, b)(f), f) = \mathrm{refl}(b)$$

Additionally, a setoid with one vertex is equivalent to a [[pointed set|pointed]] [[magma]] with an [[endofunction]]. 

## Thin setoids

Recall in graph theory that a loop directed pseudograph is **simple** or a **loop digraph** if for every vertex $a \in V$ and $b \in V$, the set of edges $E(a, b)$ is a [[subsingleton]]: for every edge $f \in E(a, b)$ and $g \in E(a, b)$, $f = g$. In the other definition, a loop directed pseudograph is a loop digraph if the functions $s:E \to V$ and $t:E \to V$ are [[jointly monic]]. 

A setoid is **thin** or **simple** if its underlying loop directed pseudograph is a loop digraph. In both cases, the pseudo-equivalence relation becomes an **[[equivalence relation]]**. The term "thin" originates from category theory, while the term "simple" originates from graph theory. 

A thin setoid is equivalently a [[thin category|thin]] [[dagger category]], or a dagger category [[enriched category|enriched]] in [[truth values]]. A thin setoid is also a thin [[groupoid]], or a groupoid enriched in truth values. 

Sometimes in the mathematical literature, setoids are thin by default. 

## Core of a setoid

For any setoid $A$, the [[core]] of $A$ is defined as the maximal [[subgroupoid]] $\mathrm{Core}(A)$ of $A$. 

More specifically, a subsetoid $G$ of a setoid $A$ is a setoid $G$ with an faithful injective-on-objects dagger functor $f:G \to A$. A subsetoid $G$ of $A$ is a subgroupoid if the pseudo-equivalence relation of $G$ additionally satisfy the groupoid equational axioms: 

* for every vertex $a \in V_G$, $b \in V_G$, $c \in V_G$, and $d \in V_G$ and edge $f \in E_G(a, b)$, $g \in E_G(b, c)$, and $h \in E_G(c, d)$
$$\mathrm{trans}(a, b, d)(f, \mathrm{trans}(b, c, d)(g, h)) = \mathrm{trans}(a, c, d)(\mathrm{trans}(a, b, c)(f, g), h)$$

* for every vertex $a \in V_G$, $b \in V_G$ and edge $f \in E_G(a, b)$
$$\mathrm{trans}(a, b, b)(f, \mathrm{refl}(b)) = f$$

* for every vertex $a \in V_G$, $b \in V_G$ and edge $f \in E_G(a, b)$
$$\mathrm{trans}(a, a, b)(\mathrm{refl}(a), f) = f$$

* for every vertex $a \in V_G$, $b \in V_G$ and edge $f \in E_G(a, b)$
$$\mathrm{trans}(a, b, a)(f, \mathrm{sym}(a, b)(f)) = \mathrm{refl}(a)$$

* for every vertex $a \in V_G$, $b \in V_G$ and edge $f:E_G(a, b)$
$$\mathrm{trans}(b, a, b)(\mathrm{sym}(a, b)(f), f) = \mathrm{refl}(b)$$

A subgroupoid $G$ of a setoid $A$ is a maximal subgroupoid if the dagger functor $f:G \to A$ is bijective-on-objects, and additionally if, for every other subgroupoid $H$ of $A$ with faithful injective-on-objects dagger functor $g:H \to A$, there is a unique faithful injective-on-objects dagger functor $h:H \to G$ such that $h \circ f = g$. 

## Category of setoids

Let the category [[Set|$Set$]] be defined as a [[category]] that is [[finitely complete category|finitely complete]] and [[well-pointed category|well-pointed]] (i.e. whose [[terminal object]] is a [[extremal epimorphism|extremal]] [[separator|generating object]]). This category of sets is not even a [[regular category]], let alone an [[exact category]], as can happen in certain [[foundations of mathematics]], such as bare [[set-level type theory|set-level]] [[Martin-Löf type theory]], or [[ZFC]] and [[ETCS]] without the [[powerset]] [[axiom]]. The category $Setoid$ of __setoids__ is then the [[exact completion|ex/lex completion]] of Set. 

More specifically, using the definition of setoid with two sets: if $(s_R, t_R):R\rightrightarrows X$ and $(s_S, t_S):S\rightrightarrows Y$ are two setoids, a morphism between them in $Setoid$ is defined to be a function $f:X\to Y$ with functions $f_1:R \to S$ with $s_S \circ f_1 = f \circ s_R$ and $t_S \circ f_1 = f \circ t_R$. Moreover, we declare two such functions $f,g:X\to Y$ to be *equal* if there exists a function $h:X\to S$ such that $s \circ h = f$ and $t \circ h = g$.  Because $(s_S, t_S):S\rightrightarrows Y$ is a pseudo-equivalence relation, this defines an actual [[equivalence relation]] on the morphisms $f:X\to Y$, which is compatible with composition; thus we have a well-defined category $Setoid$ of setoids, which is the ex/lex completion of $Set$.

We have a [[full and faithful functor]] $Set\to Setoid$ sending an object $X$ to the pseudo-equivalence relation $(s_X, t_X):X\rightrightarrows X$. One can then verify directly that $Setoid$ is exact, that this embedding preserves finite limits, and that it is universal with respect to lex functors from $Set$ into exact categories.

If the [[presentation axiom]] (a weak form of the full axiom of choice) holds in $Set$, as a subcategory of $Setoid$, $Set$ could be thought of as the category of [[completely presented sets]], the category of sets with a [[projective presentation]]. If the [[axiom of choice]] holds in $Set$, then $Set$ is equivalent to $Setoid$, as the axiom of choice implies that $Set$ is its own free exact completion, and $Set$ is equivalent to $Setoid$ because the free functor from $Set$ to $Setoid$ is an [[equivalence of categories]]. 

This construction could be generalized to any [[finitely complete category]] $C$, from which the category of [[setoid objects]] of $C$ is the [[ex/lex completion]] of $C$, and denoted as $C_{ex/lex}$. If every [[epimorphism]] in $C$ is additionally a [[split epimorphism]], then $C$ is its own free exact completion. 

## In type theory

Many [[set-level type theories]] use [[type|types]] which are [[0-truncated]] and thus [[h-sets]] by default because of the inclusion of [[uniqueness of identity proofs]] or [[axiom K]] to the rule system of the type theory. Sometimes, these type theories do not have [[quotient set|quotients]] and [[image factorizations]], and as a result, setoids are used instead of the native h-sets. 

In [[homotopy type theory]], and more generally in any [[intensional type theory]] where not all types are [[h-sets]], such as in a type theory without [[uniqueness of identity proofs]] or [[axiom K]], the notion of "setoid" bifurcates into multiple distinct notions. In analogy with [[category]], the definitions used above in this article could be called a **strict setoid**. When the vertex types are only required to be a [[type]] rather than a [[set]], then this defines a **[[presetoid]]**. There is also the notion of a **[[univalent setoid]]**, where equality of vertices is isomorphism of vertices in the core of a presetoid. 

## Related concepts

* [[equivalence relation]]
* [[setoid]]

## References

For setoids defined as a set with an pseudo-equivalence relation:

* {#Wilander12} [[Olov Wilander]], *Constructing a small category of setoids*, Mathematical Structures in Computer Science **22** 1 (2012) 103-121 &lbrack;[doi:10.1017/S0960129511000478](https://doi.org/10.1017/S0960129511000478), [pdf](http://www.diva-portal.org/smash/get/diva2:399799/FULLTEXT01.pdf)&rbrack;

* {#PalmgrenWilander14} [[Erik Palmgren]], [[Olov Wilander]], *Constructing categories and setoids of setoids in type theory*, Logical Methods in Computer Science, **10** 3 (2014) lmcs:964 &lbrack;[arXiv:1408.1364](https://arxiv.org/abs/1408.1364), <a href="https://doi.org/10.2168/LMCS-10(3:25)2014">doi:10.2168/LMCS-10(3:25)2014</a>&rbrack;

* {#EmmeneggerPalmgren20} [[Jacopo Emmenegger]], [[Erik Palmgren]], *Exact completion and constructive theories of sets*, J. Symb. Log. **85** 2  (2020) &lbrack;[arXiv:1710.10685](https://arxiv.org/abs/1710.10685), [doi:10.1017/jsl.2020.2](https://doi.org/10.1017/jsl.2020.2)&rbrack;

* {#Cipriano20} Cioffo Cipriano Junior, Def. 1.1.1 in: *Homotopy setoids and generalized quotient completion* &lbrack;[pdf](https://air.unimi.it/retrieve/d7ab68cc-fc12-4fe9-8a21-617deb888f36/phd_unimi_R12371.pdf), [[Cipriano-HomotopySetoids.pdf:file]]&rbrack;

[[!redirects pseudo-equivalence relation]]
[[!redirects pseudo-equivalence relations]]