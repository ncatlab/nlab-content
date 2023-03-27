
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

### With a family of types

A **Tarski universe** or **universe à la Tarski** is simply a type $U$ with a type family $T$ whose dependent types $T(A)$ are indexed by terms $A:U$. The terms $A:U$ are usually called **$U$-small types**, or **small types** for short, and $T(A)$ is the **type of terms of $A$**. 

### With a type and a function

A **Tarski universe** or **universe à la Tarski** is a type $U$ of all $U$-small types with a type $T'$ of all terms, and a function $\mathrm{typeOf}:T' \to U$ which gets the associated type for every term $a:T'$. 

### Equivalence of definitions

From one direction, the individual dependent types $T(A)$ could be defined as the [[fiber type]] of $\mathrm{typeOf}$ at $A$
$$T(A) \coloneqq \mathrm{fiber}_{T', U}(\mathrm{typeOf},A)$$

From the other direction, the entire type of terms $T'$ is just the [[dependent sum type]] of all the type reflections of small types
$$T' \coloneqq \sum_{A:U} T(A)$$

We shall be using the first definition throughout this article, but everything could be translated into the second definition of a Tarski universe. 

## Tarski universes as models of type theory

The definitions above are already enough to build an internal model of dependent type theory inside the Tarski universe:

* The type $A \; \mathrm{type}$ is represented by the small type $A:U$
* The term $a:A$ is represented by the term $a:T(A)$ for small type $A:U$. 
* The type family $B$ indexed by the type $A \; \mathrm{type}$ is represented by the function $B:T(A) \to U$ for small type $A:U$
* The dependent type $a:A \vdash B \; \mathrm{type}$ is represented by the section $B(a):U$ for term $a:T(A)$ and small type $A:U$. 
* The section $a:A \vdash b:B$ is represented by the term $b:T(B(a))$ for term $a:T(A)$ and small type $A:U$. 

## Properties

### Univalence

There are two notions of equivalence in a Tarski universe $(U, T)$, equality $A =_U B$ and equivalence $T(A) \simeq T(B)$. By the properties of the [[identity type]], there is a canonical [[transport]] dependent function 
$$\mathrm{transport}^T:\prod_{A:U} \prod_{B:U} (A =_U B) \to T(A) \simeq T(B)$$
A Tarski universe is a **univalent Tarski universe** if for all terms $A:U$ and $B:U$ the function $\mathrm{transport}^T(A, B)$ is an [[equivalence of types]]
$$\prod_{A:U} \prod_{B:U} \mathrm{isEquiv}(\mathrm{transport}^T(A, B))$$

This is the extensionality principle for any Tarski universe $(U, T)$. 

Equivalently, by the [[fundamental theorem of identity types]], a Tarski universe is a **univalent Tarski universe** if it comes with a dependent function
$$t:\prod_{X:U} C(X, X, \mathrm{id}_X) \vdash J(t):\prod_{A:U} \prod_{B:U} \prod_{R:T(A) \simeq T(B)} C(A, B, R)$$
and a dependent function
$$t:\prod_{X:U} C(X, X, \mathrm{id}_X) \vdash \beta(t):\prod_{A:U} J(t, A, A, \mathrm{id}_A) =_{C(A, A, \mathrm{id}_A)} t(A)$$

When the Tarski universe is closed under [[identity types]], [[dependent sum types]], and [[dependent product types]] (see below for more on closure of Tarski universes under type formers), one is able to internalize the [[type of equivalences]] in the universe as $A \simeq_U B$. It can be proven that $T(A \simeq_U B)$ is equivalent to $T(A) \simeq T(B)$, and that the definition of univalence using transport is equivalent to the usual definition given by the internal [[type of equivalences]] and the canonical function $\mathrm{idtoequiv}$. See at [Univalence axiom#For Tarski universes](https://ncatlab.org/nlab/show/univalence+axiom#for_tarski_universes) for more details on this. 

#### Construction of univalent Tarski universes via a higher inductive type

Let $(U, T)$ be a Tarski universe. Then one could construct a univalent Tarski universe as the [[higher inductive type]] $(U', T')$ generated by

* a function $F:U \to U'$
* a function $G(A):T(A) \to T'(A)$ for all terms $a:U$
* a dependent function 
$$\mathrm{ua}_{U'}:\prod_{A:U} \prod_{B:U} \mathrm{isEquiv}(\mathrm{transport}^{T'}(A, B))$$ 

### Regularity and product-regularity

A univalent Tarski universe $(U, T)$ is **regular** if it is closed under [[dependent sum types]]: namely, for all $U$-small types $A:U$ and $U$-small type families $B:T(A) \to U$, the dependent sum type $\sum_{x:T(A)} T(B(x))$ is [[essentially small type|essentially $U$-small]]. Regular univalent Tarski universes are the type theoretic equivalent of [[regular cardinals]] in [[set theory]]. 

A univalent Tarski universe $(U, T)$ is **product-regular** if it is closed under [[dependent product types]]: namely, for all $U$-small types $A:U$ and $U$-small type families $B:T(A) \to U$, the dependent product type $\sum_{x:T(A)} T(B(x))$ is [[essentially small type|essentially $U$-small]]. Product-regular univalent Tarski universes are the type theoretic equivalent of [[product-regular cardinals]] in [[set theory]]. 

Since product-regularity implies that [[function types]] between $U$-small types are essentially $U$-small, and regularity implies that [[subtypes]] of essentially $U$-small types are essentially $U$-small, this implies that in a regular and product-regular universe, [[equivalence types]] between $U$-small types are essentially $U$-small, because equivalence types are [[subtypes]] of function types. In combination with [[univalence]], regularity and product-regularity implies that the [[identity types]] of $U$-small types are also essentially $U$-small. 

### Singletons

A Tarski universe $(U, T)$ satisfies the **axiom of singletons** if it is closed under the type of all $U$-small [[contractible types]]: namely, the dependent sum type $\sum_{A:U} \mathrm{isContr}(T(A))$ is [[essentially small type|essentially $U$-small]]:

$$\mathrm{axSingl}_U:\sum_{\mathbb{1}:U} T(\mathbb{1}) \simeq \sum_{A:U} \mathrm{isContr}(T(A))$$

### Empty type

A [[univalent Tarski universe]] satisfies the **[[axiom of empty set|axiom of empty type]]** if it is closed under the (weak) [[empty type]]: if the empty type $\mathbb{0}$ is essentially $U$-small. The axiom of empty type comes from the [[formation rule]] and the dependent universal property of the empty type, which are represented by the following elements:

* formation rules: $\mathbb{0}:U$

* dependent universal property:
$$\mathrm{up}_\mathbb{0}^U:\prod_{C:\mathbb{0} \to U} \exists!c:\prod_{x:\mathbb{0}} T(C(x)).T(\mathbb{1})$$
where $\exists!x:A.B(x)$ is the [[uniqueness quantifier]] for the [[type family]] $x:A \vdash B(x)$. 

By using [[dependent sum types]], these can be combined into a single element of the following type:

$$\mathrm{axempty}_U:\sum_{\mathbb{0}:U} \prod_{C:\mathbb{0} \to U} \exists!c:\prod_{x:\mathbb{0}} T(C(x)).T(\mathbb{1})$$

### Propositional resizing

A Tarski universe $(U, T)$ satisfies **[[propositional resizing]]** if it is closed under the [[type of propositions|type of all $U$-small propositions]]: namely, the dependent sum type $\sum_{A:U} \mathrm{isProp}(T(A))$ is [[essentially small type|essentially $U$-small]]:
$$\mathrm{propresize}_U:\sum_{\Omega:U} T(\Omega) \simeq \sum_{A:U} \mathrm{isProp}(T(A))$$

This is a version internal to the universe $U$ of having a [[type of all propositions]] in the type theory itself. While propositional resizing implies that the universe is [[impredicative]], it does not imply that the type theory as a whole is impredicative; the latter requires an actual [[type of all propositions]] in the type theory. 

### Infinity

A [[univalent Tarski universe]] satisfies the **[[axiom of infinity]]** if it is closed under the (weak) [[natural numbers type]]: if the natural numbers type $\mathbb{N}$ is essentially $U$-small. The axiom of infinity comes from the [[formation rule]], the [[introduction rules]], and the [[dependent universal property of the natural numbers]], which are represented by the following elements:

* formation rules: $\mathbb{N}:U$

* introduction rules: $0:T(\mathbb{N})$ and $s:T(\mathbb{N}) \to T(\mathbb{N})$

* dependent universal property:
$$\mathrm{up}_\mathbb{N}^U:\prod_{C:\mathbb{N} \to U} \prod_{c_0:T(C(0))} \prod_{c_s:\prod_{x:\mathbb{N}} T(C(x)) \to T(C(s(x)))} \exists!c:\prod_{x:\mathbb{N}} T(C(x)).(c(0) =_{T(C(0))} c_0) \times \prod_{x:\mathbb{N}} (c(s(x)) =_{T(C(s(x)))} c_s(c(x)))$$
where $\exists!x:A.B(x)$ is the [[uniqueness quantifier]] for the [[type family]] $x:A \vdash B(x)$. 

By using [[dependent sum types]], these can be combined into a single element of the following type:

$$\mathrm{axinf}_U:\sum_{\mathbb{N}:U} \sum_{0:T(\mathbb{N})} \sum_{s:T(\mathbb{N}) \to T(\mathbb{N})} \prod_{C:\mathbb{N} \to U} \prod_{c_0:T(C(0))} \prod_{c_s:\prod_{x:\mathbb{N}} T(C(x)) \to T(C(s(x)))} \exists!c:\prod_{x:\mathbb{N}} T(C(x)).(c(0) =_{T(C(0))} c_0) \times \prod_{x:\mathbb{N}} (c(s(x)) =_{T(C(s(x)))} c_s(c(x)))$$

### Replacement

A [[univalent Tarski universe]] satisfies the __[[axiom of replacement]]__ if for every [[essentially small type|essentially $U$-small]] type $A$, every [[locally small type|locally $U$-small]] type $B$, and every function $f:A \to B$, the [[image]] of $f$, $\mathrm{im}(f)$, is essentially $U$-small. 

### Choice operators and existence

A [[choice operator]] on a type is a function from its [[propositional truncation]] to the type itself, and represents the concept that if there exists an element of the set (i.e. the propositional truncation has an element), then the set itself has an element chosen by the choice operator. A Tarski universe satisfies the **[[type-theoretic axiom of existence]]** if every $U$-small type in the Tarski universe has a choice operator, represented by the following dependent function 
$$\varepsilon_U:\prod_{A:U} \vert T(A) \vert \to T(A)$$
$U$ satisfying the type-theoretic axiom of existence implies that $U$ satisfies [[axiom K]] or [[UIP]]. If $U$ is also univalent, then it is an [[h-groupoid]]. 

There is also a **[[set-theoretic axiom of existence]]**, which only requires the sets in the universe to have choice operators. This coincides with the [[axiom of existence]] in [[set theory]] and allows for non-set types in the Tarski universe like the [[circle type]] as well. This is represented by the following dependent function
$$\varepsilon_U:\prod_{A:U} \mathrm{isSet}(T(A)) \times \vert T(A) \vert \to T(A)$$

### Closure of Tarski universes under other type formers

There are many ways of defining type formers internally in a universe: 

* by an equivalence or definitional equality with an existing global type former for the entire type theory. 

* by translating the rules for the type former into internal structure on the universe - the [[formation rules]], the [[introduction rules]], and the dependent [[universal property]] of the structure. 

* by using the [[universal properties]] corresponding to the [[categorical semantics]] of the types

Using a definitional equality with an existing global type former for each type former results in a **strict Tarski universe**, while using equivalences for each type former results in a **weak Tarski universe**. There are also various Tarski universes where some type formers are strictly closed, and some type formers are only weakly closed, resulting in Tarski universes which are intermediate between strict Tarski universes and weak Tarski universes. 

### Tarski universes with all propositions

A Tarski universe $(U, T)$ **has all propositions** if given a type $A$ with a family of identities $x:A, y:A \vdash \tau_{-1}(x, y):x =_A y$, the universe $U$ comes with the structure of an element $A_U:U$ and an equivalence $\delta_A:T(A_U) \simeq A$. 

The rules for this condition on Tarski universes is as follows:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash \tau_{-1}(x, y):x =_A y}{\Gamma \vdash A_U:U} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash \tau_{-1}(x, y):x =_A y}{\Gamma \vdash \delta_A:T(A_U) \simeq A}$$

Given a Tarski universe which has all propositions, the type $\sum_{A:U} \mathrm{isProp}(T(A))$ is the [[type of all propositions]]. This is a form of strong [[impredicativity]] in the type theory, as given a type $A$, the type $A \to \sum_{A:U} \mathrm{isProp}(T(A))$ is the [[power set]] on $A$. 

## Tarski subuniverses

Let $(U, T_U)$ be a Tarski universe. A Tarski universe $(V, T_V)$ is a **Tarski subuniverse** of $(U, T_U)$ if it comes with an [[embedding]] $t:V \hookrightarrow U$ and a dependent function
$$p:\prod_{a:V} T_U(t(a)) \simeq T_V(a)$$

This is equivalent to a family of Tarski universes $(U(i), T(i))$ indexed by terms $i:\mathbb{2}$ of the [[interval preorder]] $(\mathbb{2}, \leq_\mathbb{2})$, which comes with 

* a dependent function
$$t:\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} (a \leq_\mathbb{2} b) \to (U(a) \hookrightarrow U(b))$$

* a dependent function
$$q:\prod_{a:\mathbb{2}} \prod_{b:\mathbb{2}} \prod_{p:a \leq_\mathbb{2} b} \prod_{A:U(a)} T(a)(A) \simeq T(b)(t(a, b)(p)(A))$$
indicating that lifting each small type results in a type equivalent to the original small type. 

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

### Reflective and coreflective Tarski subuniverses

(Section under construction see [[reflective subuniverse]] for the [[Russell universe]] variant for the time being)

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

## Examples

The [[empty type]], [[unit type]], [[boolean domain]], and [[FinSet]] are all regular univalent Tarski universes. The [[types of propositions]] in a type theory are univalent Tarski universes: they model a dependent type theoretic model of [[propositional logic]] with [[function types]], [[product types]], [[disjunction]] [[higher inductive types]], [[empty type]], and [[unit type]]. 

Every [[concrete category]] and every [[concrete dagger category]] is a Tarski universe, as given a concrete category or concrete dagger category $C$ by definition for each object $A:Ob(C)$ there is an [[h-set]] $El(A)$. This includes models of [[Mike Shulman]]'s [[SEAR]], which is a concrete [[power allegory]], as well as [[ETCS with elements]], which is a concrete [[elementary topos]]. 

## See also

For universes as a replacement for type judgments, see

* [[Russell universe]]

Regarding the general notion of types of small types, see 

* [[type universe]]

Other mathematical structures and their univalent counterparts:

* [[preorder]], [[partial order]]
* [[precategory]], [[univalent category]]
* [[dagger precategory]], [[univalent dagger category]]
* [[locally univalent bicategory]], [[univalent bicategory]]

## References

Historical review of [[Alfred Tarski]]'s original notion in [[set theory]]:

* [[Ralf Krömer]], §6.4.5 in: *Tool and object: A history and philosophy of category theory*, Science Networks. Historical Studies **32** (2007) &lbrack;[doi:10.1007/978-3-7643-7524-9](https://doi.org/10.1007/978-3-7643-7524-9)&rbrack;

The terminology "universe &agrave; la Tarski" --- and now in the context of [[type universes]] for [[Martin-Löf dependent type theory]] --- is due to:

* [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]): p. 48 in: _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;


Further discussion:

* {#Hofmann95} [[Martin Hofmann]], *Universes*, section 2.3.5 in: *Syntax and semantics of dependent types*, Chapter 2 in: _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh (1995), Distinguished Dissertations, Springer (1997) &lbrack;[ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]], [doi:10.1007/978-1-4471-0963-1](https://doi.org/10.1007/978-1-4471-0963-1)&rbrack;

See also:

* {#Luo12} [[Zhaohui Luo]], *Notes on Universes in Type Theory*, 2012 ([pdf](http://www.cs.rhul.ac.uk/home/zhaohui/universes.pdf))

* {#Gallozzi14} [[Cesare Gallozzi]], *Constructive Set Theory from a Weak Tarski Universe*, MSc thesis (2014) ([arXiv:1411.5591](http://xxx.tau.ac.il/abs/1411.5591))

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* {#UFP13} *Homotopy Type Theory: Univalent Foundations of Mathematics*,
The Univalent Foundations Program, Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

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

[[!redirects regular Tarski universe]]
[[!redirects regular Tarski universes]]
[[!redirects regular universe a la Tarski]]
[[!redirects regular universes a la Tarski]]

[[!redirects regular univalent Tarski universe]]
[[!redirects regular univalent Tarski universes]]
[[!redirects regular univalent universe a la Tarski]]
[[!redirects regular univalent universes a la Tarski]]

[[!redirects product-regular Tarski universe]]
[[!redirects product-regular Tarski universes]]
[[!redirects product-regular universe a la Tarski]]
[[!redirects product-regular universes a la Tarski]]

[[!redirects product-regular univalent Tarski universe]]
[[!redirects product-regular univalent Tarski universes]]
[[!redirects product-regular univalent universe a la Tarski]]
[[!redirects product-regular univalent universes a la Tarski]]

[[!redirects inaccessible Tarski universe]]
[[!redirects inaccessible Tarski universes]]
[[!redirects inaccessible universe a la Tarski]]
[[!redirects inaccessible universes a la Tarski]]

[[!redirects inaccessible univalent Tarski universe]]
[[!redirects inaccessible univalent Tarski universes]]
[[!redirects inaccessible univalent universe a la Tarski]]
[[!redirects inaccessible univalent universes a la Tarski]]

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

[[!redirects judgmentally Tarski]]
[[!redirects judgmentally a la Tarski]]
[[!redirects judgmental Tarski universe]]
[[!redirects judgmental Tarski universes]]
[[!redirects judgmentally Tarski universe]]
[[!redirects judgmentally Tarski universes]]
[[!redirects judgmentally a la Tarski universe]]
[[!redirects judgmentally a la Tarski universes]]

[[!redirects judgmentally strict Tarski universe]]
[[!redirects judgmentally strict Tarski universes]]

[[!redirects propositionally Tarski]]
[[!redirects propositionally a la Tarski]]
[[!redirects propositional Tarski universe]]
[[!redirects propositional Tarski universes]]
[[!redirects propositionally Tarski universe]]
[[!redirects propositionally Tarski universes]]
[[!redirects propositionally a la Tarski universe]]
[[!redirects propositionally a la Tarski universes]]

[[!redirects propositionally strict Tarski universe]]
[[!redirects propositionally strict Tarski universes]]

[[!redirects typally Tarski]]
[[!redirects typally a la Tarski]]
[[!redirects typal Tarski universe]]
[[!redirects typal Tarski universes]]
[[!redirects typally Tarski universe]]
[[!redirects typally Tarski universes]]
[[!redirects typally a la Tarski universe]]
[[!redirects typally a la Tarski universes]]

[[!redirects typally strict Tarski universe]]
[[!redirects typally strict Tarski universes]]

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
