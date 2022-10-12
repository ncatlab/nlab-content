
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[intensional type theory]] and [[homotopy type theory]], there are typically two ways to construct a "type of small types". One way is by [[Russell universes]], where a [[term]] $A:U$ of a [[type universe]] $U$ is literally a [[type]] $A \; \mathrm{type}$. The alternative is by Tarski universes, where terms $A:U$ are not literally types, but rather the universe type $U$ comes with the additional structure of a [[type family]] $T$, such that the [[dependent type]] $T(A)$ represents the actual type. 
Usually universes are defined in [[intensional type theory]] and [[homotopy type theory]] using [[derivations]] and [[rules]], such as the type reflection rule 
$$\frac{\Gamma \vdash A:U}{\Gamma \vdash T(A) \; \mathrm{type}}$$
for Tarski universes. Furthermore, universes are usually defined as being closed under all type formers inside the type theory, regardless of the type theory. 

However, this approach of defining Tarski universes means that the notion of "Tarski universe" differs from type theory to type theory. By this approach, a Tarski universe in the bare intensional [[Martin-Löf type theory]], which has [[identity types]], [[dependent product types]], [[dependent sum types]], an [[empty type]], a [[unit type]], a [[booleans type]], and a [[natural numbers type]], would not be considered a Tarski universe in [[homotopy type theory]], since it is missing important type formers present in homotopy type theory, such as internal [[pushout types]], a [[torus type]], [[propositional truncations]], [[W-types]], and [[localizations]]. On the other hand, one could consider an even more spartan type theory which doesn't even have the [[unit type]], let alone the [[empty type]], the [[natural numbers type]], and the [[booleans type]], whose Tarski universes are thus consisting of only internal [[identity types]], [[dependent product types]], [[dependent sum types]]. 

All three notions of Tarski universe described above are in fact definable in all three versions of intensional type theory mentioned above, but Tarski universes are usually described as having, apart from addiitonal internal Tarski universes, exactly the internal type formers that the external type theory has. One usually doesn't consider Tarski universes with an internal [[James construction type]] in bare intensional Martin-Löf type theory, even though a Tarski universe closed under James constructions is definable in Martin-Löf type theory. On the other hand, in [[homotopy type theory]] the name "Tarski universe" isn't usually used for a universe only closed under [[identity types]], [[dependent product types]], [[dependent sum types]]. 

From a global perspective, however, all of these types should be considered Tarski universes, since they model some notion of type of small types, even though the small types in the universe do not behave as the external types in the type theory do. And that is how we approach Tarski universes in this article: Tarski universes are a very general notion encompassing all of the above notions of Tarski universe and more, and one could describe more specific versions of Tarski universes by adding additional structure and axioms to Tarski universes, in the same way one adds additional structure and axioms to an [[abelian group]] to get a [[ring]], a [[commutative ring]], a $R$-[[module]], a $R$-algebra, and an $R$-[[commutative algebra]]. We could then study in general Tarski universes and their properties as we do for abelian groups and rings. This requires a shift in the point of view of what Tarski universes are: Tarski universes are actual [[mathematical structure]] in intensional type theory, rather than being something in the [[foundations of mathematics]] to merely address [[size]] issues or do mathematics in. 

## Definition

A **Tarski universe** or **universe à la Tarski** is simply a type $U$ with a type family $T$ whose dependent types $T(A)$ are indexed by terms $A:U$. The terms $A:U$ are usually called **$U$-small types**, or **small types** for short. This is already enough to build an internal model of dependent type theory inside the Tarski universe:

* The type $A \; \mathrm{type}$ is represented by the small type $A:U$
* The term $a:A$ is represented by the term $a:T(A)$ for small type $A:U$. 
* The type family $B$ indexed by the type $A \; \mathrm{type}$ is represented by the function $B:T(A) \to U$ for small type $A:U$
* The dependent type $a:A \vdash B \; \mathrm{type}$ is represented by the section $B(a):U$ for term $a:T(A)$ and small type $A:U$. 
* The section $a:A \vdash b:B$ is represented by the term $b:T(B(a))$ for term $a:T(A)$ and small type$A:U$. 

Furthermore, there are two notions of equivalence in a Tarski universe $(U, T)$, equality $A =_U B$ and equivalence $T(A) \simeq T(B)$. By the properties of the [[identity type]], there is a canonical [[transport]] dependent function 
$$\mathrm{transport}^T:\prod_{A:U} \prod_{B:U} (A =_U B) \to T(A) \simeq T(B)$$
A Tarski universe is a **univalent Tarski universe** if for all terms $A:U$ and $B:U$ the function $\mathrm{transport}^T(A, B)$ is an [[equivalence of types]]
$$\prod_{A:U} \prod_{B:U} \mathrm{isEquiv}(\mathrm{transport}^T(A, B))$$

This is the extensionality principle for any Tarski universe $(U, T)$. 

When the Tarski universe is closed under [[identity types]], [[dependent sum types]], and [[dependent product types]] (see below for more on closure of Tarski universes under type formers), one is able to internalize the [[type of equivalences]] in the universe as $A \simeq_U B$. It can be proven that $T(A \simeq_U B)$ is equivalent to $T(A) \simeq T(B)$, and that the definition of univalence using transport is equivalent to the usual definition given by the internal [[type of equivalences]] and the canonical function $\mathrm{idtoequiv}$. See at [Univalence axiom#For Tarski universes](https://ncatlab.org/nlab/show/univalence+axiom#for_tarski_universes) for more details on this. 

## Construction of univalent Tarski universes via a higher inductive type

Let $(U, T)$ be a Tarski universe. Then one could construct a univalent Tarski universe as the [[higher inductive type]] $(U', T')$ generated by

* a function $F:U \to U'$
* a function $G(A):T(A) \to T'(A)$ for all terms $a:U$
* a dependent function 
$$\mathrm{ua}_{U'}:\prod_{A:U} \prod_{B:U} \mathrm{isEquiv}(\mathrm{transport}^{T'}(A, B))$$ 

## Essentially small Tarski universes

A Tarski universe $(V, T_V)$ inside of a Tarski universe $(U, T_U)$ consists of a term $V:U$ and a function $T_V:T_U(V) \to U$. 

Given a Tarski universe $(U, T_U)$, a Tarski universe $(V, T_V)$ is essentially $U$-small if it comes with 

* a term $V':U$ 

* a function $T_{V'}:T_U(V') \to U$

* an equivalence 
$$\mathrm{smallType}:V \simeq T_U(V')$$

* a dependent function 
$$\mathrm{smallFamily}:\prod_{A:V} T_V(A) \simeq T_U(T_{V'}(\mathrm{smallType}(A)))$$

Equivalently, the entire structure could be regarded as a family of Tarski universes $(U(a), T(a))$ indexed by terms $a:\mathbb{2}$ of the [[interval preorder]] $(\mathbb{2}, \leq_\mathbb{2})$, which comes with 

* a dependent function 
$$U':\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} \prod_{p:a \leq_\mathbb{2} b} \left((b \leq_\mathbb{2} a) \to \emptyset\right) \to U(b)$$

* a dependent function 
$$T':\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} \prod_{p:a \leq_\mathbb{2} b} \left((b \leq_\mathbb{2} a) \to \emptyset\right) \to \left(T(b)(U'(a, b, p)) \to U(b)\right)$$

* an dependent function 
$$\mathrm{smallType}:\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} \prod_{p:a \leq_\mathbb{2} b} \left((b \leq_\mathbb{2} a) \to \emptyset\right) \to \left(U(a) \simeq T(b)(U'(a, b, p))\right)$$

* a dependent function 
$$\mathrm{smallFamily}:\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} \prod_{p:a \leq_\mathbb{2} b} \left((b \leq_\mathbb{2} a) \to \emptyset\right) \to \prod_{A:U(a)} T(a)(A) \simeq T(b)(T'(a, b, p)(\mathrm{smallType}(a, b, p)(A)))$$

## Tarski subuniverses

Let $(U, T_U)$ be a Tarski universe. A Tarski universe $(V, T_V)$ is a **Tarski subuniverse** of $(U, T_U)$ if it comes with an [[embedding]] $t:V \hookrightarrow U$ and a dependent function
$$p:\prod_{a:V} T_U(t(a)) \simeq T_V(a)$$

This is equivalent to a family of Tarski universes $(U(i), T(i))$ indexed by terms $i:\mathbb{2}$ of the [[interval preorder]] $(\mathbb{2}, \leq_\mathbb{2})$, which comes with 

* a dependent function
$$t:\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} (a \leq_\mathbb{2} b) \to (U(a) \hookrightarrow U(b))$$

* a dependent function
$$q:\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} \prod_{p:a \leq_\mathbb{2} b} \prod_{A:U(a)} T(a)(A) \simeq T(b)(t(a, b)(p)(A))$$
indicating that lifting each small type results in a type equivalent to the original small type. 

## Hierarchy of Tarski universes

Let $P$ be a [[preorder]]. Then, a $P$-indexed hierarchy of Tarski universes is a type family $U$ such that for all indices $a:P$, there is a Tarski universe $(U(a), T(a))$, such that for all indices $a:P$ and $b:P$ and witnesses $p:a \leq_P b$, the Tarski universe $(U(a), T(a))$ is an essentially $U(b)$-small Tarski subuniverse of the Tarski universe $(U(b), T(b))$. 

Expanded out, the family of Tarski universes $(U(a), T(a))$ indexed by terms $a:P$ additionally come with

* a dependent function 
$$U':\prod_{a:P} \prod_{b:P} \prod_{p:a \leq_P b} \left((b \leq_P a) \to \emptyset\right) \to U(b)$$

* a dependent function 
$$T':\prod_{a:P} \prod_{b:P} \prod_{p:a \leq_P b} \left((b \leq_P a) \to \emptyset\right) \to \left(T(b)(U'(a, b, p)) \to U(b)\right)$$

* an dependent function 
$$\mathrm{smallType}:\prod_{a:P} \prod_{b:P} \prod_{p:a \leq_P b} \left((b \leq_P a) \to \emptyset\right) \to \left(U(a) \simeq T(b)(U'(a, b, p))\right)$$

* a dependent function 
$$\mathrm{smallFamily}:\prod_{a:P} \prod_{b:P} \prod_{p:a \leq_P b} \left((b \leq_P a) \to \emptyset\right) \to \prod_{A:U(a)} T(a)(A) \simeq T(b)(T'(a, b, p)(\mathrm{smallType}(a, b, p)(A)))$$

* a dependent function
$$t:\prod_{a:P} \prod_{b:P} (a \leq_P b) \to (U(a) \hookrightarrow U(b))$$

* a dependent function
$$q:\prod_{a:P} \prod_{b:P} \prod_{p:a \leq_P b} \prod_{A:U(a)} T(a)(A) \simeq T(b)(t(a, b)(p)(A))$$

Usually, hierarchies of Tarski universes are indexed by the type of [[natural numbers]]. A type theory may have multiple hierarchies of type universes. 

## Closure of Tarski universes under type formers

There are many ways of defining type formers internally in a universe: 

* by an equivalence or definitional equality with an existing global type former for the entire type theory. 

* by translating the rules for the type former into internal structure on the universe

* by using the [[universal properties]] corresponding to the [[categorical semantics]] of the types

Using a definitional equality with an existing global type former for each type former results in a **strict Tarski universe**, while using equivalences for each type former results in a **weak Tarski universe**. There are also various Tarski universes where some type formers are strictly closed, and some type formers are only weakly closed, resulting in Tarski universes which are intermediate between strict Tarski universes and weak Tarski universes. 

### Empty type

Suppose that the type theory has an already existing empty type $\emptyset \; \mathrm{type}$. Then a Tarski universe is **weakly closed under the empty type** if there exists a term $\emptyset_U:U$ and an equivalence $\mathrm{smallemptytype}:T(\emptyset_U) \simeq \emptyset$. A Tarski universe is **strongly closed under the empty type** if there is a definitional equality $T(\emptyset_U) \equiv \emptyset$. 

If the type theory does not have an already existing empty type, then a Tarski universe is **closed under the empty type** if there exists a term $\emptyset_U:U$ and for all functions $C:T(\emptyset_U) \to U$ and terms $p:T(\emptyset_U)$ there is a term $\mathrm{ind}_\emptyset^C(p):T(C(p))$, and for all other terms $u(p):T(C(p))$ there is an [[identification]] $\eta_\emptyset(p, u):u(p) =_{T(C(p))} \mathrm{ind}_\emptyset^C(p)$. 

### Unit type

Suppose that the type theory has an already existing unit type $\mathbb{1} \; \mathrm{type}$. Then a Tarski universe is **weakly closed under the unit type** if there exists a term $\mathbb{1}_U:U$ and an equivalence $\mathrm{smallunittype}:T(\mathbb{1}_U) \simeq \mathbb{1}$. A Tarski universe is **strongly closed under the unit type** if there is a definitional equality $T(\mathbb{1}_U) \equiv \mathbb{1}$. 

### Booleans type

Suppose that the type theory has an already existing booleans type $\mathbb{2} \; \mathrm{type}$. Then a Tarski universe is **weakly closed under the booleans type** if there exists a term $\mathbb{2}_U:U$ and an equivalence $\mathrm{smallbooleanstype}:T(\mathbb{2}_U) \simeq \mathbb{2}$. A Tarski universe is **strongly closed under the booleans type** if there is a definitional equality $T(\mathbb{2}_U) \equiv \mathbb{2}$. 

### Natural numbers type

Suppose that the type theory has an already existing natural numbers type $\mathbb{N} \; \mathrm{type}$. Then a Tarski universe is **weakly closed under the natural numbers type** if there exists a term $\mathbb{N}_U:U$ and an equivalence $\mathrm{smallnaturalnumberstype}:T(\mathbb{N}_U) \simeq \mathbb{N}$. A Tarski universe is **strongly closed under the natural numbers type** if there is a definitional equality $T(\mathbb{N}_U) \equiv \mathbb{N}$. 

### Identity types

### Dependent function types

### Dependent sum types

## Modalities and comodalities

A **[[modal operator]]** on a Tarski universe $(U, T)$ is just an [[endofunction]] $L:U \to U$. Given a Tarski universe, the **modal unit family** is a family of functions
$$\eta:\prod_{L:U \to U}\prod_{A:U} T(A) \to T(L(A))$$
and the **comodal counit family** is a family of functions 
$$\epsilon:\prod_{L:U \to U}\prod_{A:U} T(L(A)) \to T(A)$$
Given a modal operator $L:U \to U$, $\eta(L)$ is called the **modal unit** of $L$ and $\epsilon(L)$ is called the **comodal counit** of $L$. A small type $A:U$ is **$L$-modal** if the function 
$$\eta(L)(A):T(A) \to T(L(A))$$
is an [[equivalence of types]], and **$L$-comodal** if the function 
$$\epsilon(L)(A):T(L(A)) \to T(A)$$
is an equivalence of types. 

A **[[modality]]** is...

...and a **[[comodality]]** is...

## Reflective and coreflective Tarski subuniverses

(Section under construction see [[reflective subuniverse]] for the [[Russell universe]] variant for the time being)

## Examples

The [[types of propositions]] in a type theory are univalent Tarski universes: they model a dependent type theoretic model of [[propositional logic]] with [[function types]], [[product types]], [[disjunction]] [[higher inductive types]], [[empty type]], and [[unit type]]. 

Every [[concrete category]] and every [[concrete dagger category]] is a Tarski universe, as given a concrete category or concrete dagger category $C$ by definition for each object $A:Ob(C)$ there is an [[h-set]] $El(A)$. This includes models of [[Mike Shulman]]'s [[SEAR]], which is a concrete [[power allegory]], as well as [[ETCS with elements]], which is a concrete [[elementary topos]]. 

## See also

Regarding the general notion of types of small types, see 

* [[type universe]]

Other mathematical structures and their univalent counterparts:

* [[preorder]], [[partial order]]
* [[precategory]], [[univalent category]]
* [[dagger precategory]], [[univalent dagger category]]
* [[locally univalent bicategory]], [[univalent bicategory]]

## References

* {#Hofmann} [[Martin Hofmann]], section 2.1.6 of *Syntax and semantics of dependent types* ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.8985))

* {#Luo12} [[Zhaohui Luo]], *Notes on Universes in Type Theory*, 2012 ([pdf](http://www.cs.rhul.ac.uk/home/zhaohui/universes.pdf))

* {#Gallozzi14} [[Cesare Gallozzi]], *Constructive Set Theory from a Weak Tarski Universe*, MSc thesis (2014) ([arXiv:1411.5591](http://xxx.tau.ac.il/abs/1411.5591))

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf)) (478 pages)

* {#RSS17} [[Egbert Rijke]], [[Mike Shulman]], [[Bas Spitters]], _[[Modalities in homotopy type theory]]_ ([arXiv:1706.07526](https://arxiv.org/abs/1706.07526))

[[!redirects a la Tarski]]
[[!redirects Tarski universe]]
[[!redirects Tarski universes]]
[[!redirects universe a la Tarski]]
[[!redirects universes a la Tarski]]
[[!redirects univalent Tarski universe]]
[[!redirects univalent Tarski universes]]
[[!redirects univalent universe a la Tarski]]
[[!redirects univalent universes a la Tarski]]

[[!redirects weakly Tarski]]
[[!redirects weakly a la Tarski]]
[[!redirects weak Tarski universe]]
[[!redirects weak Tarski universes]]
[[!redirects weakly Tarski universe]]
[[!redirects weakly Tarski universes]]
[[!redirects weakly a la Tarski universe]]
[[!redirects weakly a la Tarski universes]]

[[!redirects strictly Tarski]]
[[!redirects strictly a la Tarski]]
[[!redirects strict Tarski universe]]
[[!redirects strict Tarski universes]]
[[!redirects strictly Tarski universe]]
[[!redirects strictly Tarski universes]]
[[!redirects strictly a la Tarski universe]]
[[!redirects strictly a la Tarski universes]]

[[!redirects type with a type family]]
[[!redirects univalent type with a type family]]

[[!redirects Tarski universe hierarchy]]
[[!redirects hierarchy of Tarski universes]]

[[!redirects weak Tarski universe hierarchy]]
[[!redirects hierarchy of weak Tarski universes]]
[[!redirects weakly Tarski universe hierarchy]]
[[!redirects hierarchy of weakly Tarski universes]]

[[!redirects strict Tarski universe hierarchy]]
[[!redirects hierarchy of strict Tarski universes]]
[[!redirects strictly Tarski universe hierarchy]]
[[!redirects hierarchy of strictly Tarski universes]]