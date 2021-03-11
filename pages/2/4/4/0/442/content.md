+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

The notion of _Lawvere theory_ is a joint generalization of the notions of [[group]], [[ring]], [[associative algebra]], etc. 

In his [[Functorial Semantics of Algebraic Theories|1963 doctoral dissertation]], Bill Lawvere introduced a new categorical method for doing [[universal algebra]], alternative to the usual way of presenting an algebraic concept by means of its logical [[signature (in logic)|signature]] (with generating operations satisfying equational axioms). The rough idea is to define an [[algebraic theory]] as a [[category]] with finite [[product]]s and possessing a "generic algebra" (e.g., a generic [[group]]), and then define a [[model]] of that [[theory]] (e.g., a group) as a product-preserving [[functor]] out of that [[category]]. This type of category is what is nowadays called a _Lawvere algebraic theory_, or just Lawvere theory. 


## Definition
There are two related definitions of Lawvere theory in the literature. Both definitions are widely used and both have a substantial history. 
+-- {: .un_defn}
###### Definition A

A **Lawvere [[theory]]** or **finite-product theory** is (equivalently encoded by its [[syntactic category]] which is) a [[category]] $T$ with finite [[products]] in which every [[object]] is [[isomorphism|isomorphic]] to a finite cartesian power $x^n = x \times x \times \cdots \times x$ of a distinguished object $x$ (called the _generic object_ for the theory $T$). 

A _[[homomorphism]]_ of such theories $T \to T'$ is a product-preserving [[functor]]. 

=--

+-- {: .un_defn}
###### Definition B

Let $\mathbb{F}$ be the category of natural numbers and functions between them (a [[skeleton]] of the [[FinSet|category of finite sets]]). This category has canonical chosen [[coproducts]]. 

A **Lawvere [[theory]]** is a [[category]] $T$ with equipped with an [[identity-on-objects functor|identity-on-objects]] strictly [[power]]-preserving functor $J:\mathbb{F}^{\mathrm{op}} \to T$. (Power preservation is here equivalent to product preservation.)
=--

+-- {: .un_remark}
###### Remark

Clearly, if $T$ is part of a structure in the form of Definition B, then $T$ is of the form in Definition A, taking $x=J(1)$. See further remarks below. 

For $T$ a Lawvere theory, we are to think of the [[hom-set]] $T(n,1) := T(x^n, x)$ as the set of $n$-ary operations definable in the theory. For instance for $T$ the theory of [[abelian group]]s, $T(2,1)$ includes operations like $+ \colon (x, y) \mapsto x + y$, $- \colon (x, y) \mapsto x-y$, and $(x, y) \mapsto 2 x - 3 y$. For $0$-ary or nullary operations, we have $T(0,1) = \{0\}$. 

=--

+-- {: .un_defn}
###### Definition

A **[[model]]** of $T$ -- an **[[algebra over a Lawvere theory|algebra over the Lawvere theory]]** or simply **$T$-algebra** -- is a product-preserving [[functor]] 

$$
  A : T \to Set
  \,,
$$ 

and _homomorphism of $T$-algebras_ is a [[natural transformation]] between such functors. 

=--

+-- {: .un_remark}
###### Remark

Such a functor picks out a single [[set]] $U(A) := A(1)$ and picks for every $n$-ary abstract operation $\phi \in T(n,1)$ an actual $n$-ary operation on the elements of this set

$$
  A(\phi) : U(A)^n \to U(A)
$$

such that these operations are all compatible with each other in the way governed by the composition rules of morphisms in $T$.

When working with Definition B of Lawvere theory, it would be normal to require that $A$ _strictly_ preserves products.
=--


### Remarks

1. From some perspectives, Definition B violates the [[principle of equivalence]], although from another perspective it should be regarded as a basic structural definition that is equivalent in content to an [[clone|abstract clone]], or equivalently a [[relative monad]] over $\mathbb{F}$. 
On the other hand, given a structure of the form Definition A, we may choose a power of $x$ for each natural number, and thus derive an [[essentially surjective functor|essentially surjective]] product-preserving functor $\mathbb{F}^{op} \to T$, and then we can always factor this as an identity-on-objects functor to reach Definition B. 

1. Some people use 'finite-product theory' to mean any (small) category with [[finite products]], reserving 'Lawvere theory' to refer to finite product theories with the property that every object is isomorphic to a product of finitely many copies of a given object $x$. Finite-product theories $C$ can be regarded as a special case of [multisorted Lawvere theories](https://ncatlab.org/toddtrimble/published/multisorted+Lawvere+theories) (see below) where the set of sorts is $Ob(C)$ itself. Some, but not all, the above discussion generalizes to this case. 

1. As _finite-product theories_, Lawvere theories are at one end of a spectrum of [[theory|theories]] of differing logical strengths. For example, there are left exact theories, [[regular theory|regular theories]], geometric theories, and so on, which require for their interpretation categories of differing degrees of strength in their [[internal logic]]. See also [[classifying topos]].

1. If $C$ is a category with finite products, then a group (object) in $C$ may be defined as a product-preserving functor $T_{Grp} \to C$. For example, a topological group may be identified with a functor $T_{Grp} \to Top$, and a Lie group with a product-preserving functor $T_{Grp} \to Man$ into the category of smooth [[manifold]]s. An analogous statement holds for any finitary algebraic theory, when formulated in terms of its Lawvere theory $T$. 


### Variations

* A **multisorted** or multityped Lawvere theory for a given set of sorts $S$ is a category with finite products $C$ together with a function $i: S \to Ob(C)$ such that every object of $C$ is isomorphic to a finite product of objects of the form $i(S)$. An example is the theory for ring-module pairs, which may be regarded as a two-sorted theory in which one sort is interpreted as a ring and the other as a module over that ring. 

* An [[infinitary Lawvere theory]] allows for infinitary operations.  An example is the theory of [[suplattices]], where we have, for every [[cardinal number]] $n$, an operation to take the [[supremum]] of $n$ elements.  While Lawvere theories correspond to finitary monads on $Set$, infinitary Lawvere theories correspond to arbitrary monads.

* A [[Fermat theory]] is a Lawvere theory equipped with a notion of differentiation.

* A finite-product theory can also be presented without including all the products of the basic types as actual objects.  This yields the notion of [[cartesian multicategory]].

## Examples

### The theory of sets {#TheoryOfSets}

The tautological example of a Lawvere theory is the algebraic theory of _no_ operations. This is also called the **theory of equality**.

Its syntactic category is the category $\mathcal{S}$ on objects $n \in \mathbb{N}$ with morphisms generated by the projections $\pi_i : n \to 1$. This is the [[opposite category]] of the category [[FinSet]]

$$
  \mathcal{S} \simeq FinSet^{op}
  \,.
$$


This is the [[initial object]] in the category of Lawvere theories.


An algebra over this theory is just a bare [[set]]:

$$
  \mathcal{S} Alg \simeq Set
  \,.
$$

For $T$ any Lawvere theory, there is a canonical morphism $\mathcal{S} \to T$. On categories of algebras this induces the functor

$$
  U_T : T Alg \to \mathcal{S}Alg \simeq Set
  \,.
$$

This sends each algebra to its _underlying set_ . For more on this see the section [Free T-algebras](#FreeAlgebras) below.



### The theory of groups

We consider here the theory of [[group]]s (defined however you like). To get the corresponding Lawvere theory $T$, let $F(n)$ (for any natural number $n \geq 0$) be a free group on $n$ generators, and define the Lawvere theory $T_{Grp}$ to be the category [[opposite category|opposite]] to the category of free groups $F(n)$ and group homomorphisms. The generic object $x$ of $T_{Grp}$ is taken to be $F(1)$. 

The category of free groups has finite coproducts since $F(m) + F(n) \cong F(m+n)$ (in other words, the inclusion 

$$FreeGroup \hookrightarrow Group$$ 

creates coproducts in $FreeGroup$), so $T_{Grp}$ has finite products, and we have $F(n) = x^n$ in $T_{Grp}$. Any group $G$ defines a product-preserving functor 

$$T_{Grp} = FreeGroup^{op} \hookrightarrow Group^{op} \stackrel{\hom(-, G)}{\to} Set$$ 

since contravariant hom-functors take coproducts to products. Thus any group gives a model of $T_{Grp}$. 

The other direction is more interesting. Let 

$$M: T_{Grp} \to Set$$ 

be a model of $T_{Grp}$, i.e., a product-preserving functor. We will define a group structure on $G = M(x)$, the underlying set of the group. 

To understand this, let's consider how group multiplication would be defined. The idea is that $x$ in $T_{Grp}$ is a "generic group", so we first need to understand how multiplication works there. The idea is that the product 
in the generic group 
$$m: x^2 \to x^1$$ 
corresponds to a homomorphism 
$$F(1) \to F(2)$$
which by freeness corresponds to an element $1 \to F(2)$, and the element we are after should be the product $a b$ of the generators $a, b$ of the free group $F(2) = F(a, b)$. The generators $a, b$ themselves correspond to the two coproduct inclusions 
$$i_1: F(1) \to F(1) + F(1) = F(2) \qquad i_2: F(1) \to F(1) + F(1) = F(2)$$ 

Then, since $M$ is assumed to [[exact functor|preserve products]], we obtain a map 
$$G \times G = M(x) \times M(x) \cong M(x^2) \stackrel{M(m)}{\to} M(x) = G$$ 
and this defines the group multiplication on $G$. The group identity and group inversion on $G$ are defined by following similar recipes. 

It may be checked that the notion of homomorphism of $T_{Grp}$-models (as defined above) coincides with the usual notion of group homomorphism. In summary, the category of groups is equivalent to the category of models of $T_{Grp}$. 

In particular, any hom-functor 

$$\hom_{T_{Grp}}(x^n, -): T_{Grp} \to Set$$ 

preserves products, and so defines a group. This group is precisely the free group on $n$ generators, and a little thought shows that the $n$ generators correspond to the natural transformations 
$$\hom_{T_{Grp}}(x, -) \to \hom_{T_{Grp}}(x^n, -)$$
induced by the $n$ projection maps $x^n \to x$. 

All of the discussion above for the case of groups generalizes to any finitary [[algebraic theory]] (i.e., any single-sorted theory whose signature consists of function symbols of finite arity, subject to universally quantified equational axioms). In summary: 

* The Lawvere theory $T$ is the category opposite to the category of free algebras on finitely many generators, 

* The category of algebras is in turn equivalent to the category of product-preserving functors $T \to Set$, and 

* The free algebras are retrieved as the representable functors $T \to Set$. 

As discussed in the article on [[operad|operads]], the notion of Lawvere theory may also be formulated in terms of operads relative to the theory of [[cartesian monoidal category|cartesian monoidal categories]]. 

### Other examples
 {#OtherExamples}

Most of the standard structures that are considered in [[algebra]] indeed are models of algebraic/Lawvere theories in the precise sense. The following list gives a few familiar examples and a few not so familiar ones, but there are many more. Beware though that there are also some familiar examples that seem to be algebraic but are not, these we discuss [below](#SomeNonExamples).

* For $k$ a [[field]], the category of _free $k$-associative algebras_ is the (syntactic category of the) theory of ordinary [[associative algebras]] over $k$.

* for $G$ a fixed [[group]], then $G$-[[actions]] ([[permutation representations]]) are an example of algebras over a Lawvere theory

* for $R$ a fixed [[ring]], then $R$-[[modules]] are an example

* for $k$ a [[field]], then [[Lie algebras]] over $k$ are an example

* The category of say [[distributive lattices]] is the category of algebras of a Lawvere theory. So is the category of [[Heyting algebras]]. 

* The category [[CartSp]] is the (syntactic category of the) theory of [[smooth algebras]] (as used in [[synthetic differential geometry]]). This is also a [[Fermat theory]]. 

* The terminal Lawvere theory has exactly one morphism $f \colon m \to n$ for each $m,n$. Since there is a unique morphism between each pair of objects, each object is in fact isomorphic. Thus, this theory is a terminal category. Algebras of the terminal Lawvere theory are terminal sets, singletons.  


### Characterization of examples
 {#CharacterizationOfExamples}

If $T$ is any [[theory]] given by a [[signature]] consisting of finitary [[operations]] (but no [[relations]]) on a single [[sort]], and a set of [[axioms]] all of which are [[universal quantifier|universally quantified]] [[equations]] between terms, then a model of $T$ can be described as an algebra of a Lawvere theory. 

This includes most cases arising in a typical undergraduate course in modern algebra, as the examples [above](#OtherExamples) suggest.

There are also well-known criteria for a category of single-sorted structures $C$, with underlying set-functor $U: C \to Set$, to be the category of algebras of a Lawvere theory. 

+-- {: .num_theorem #RecognizingAConcreteCategoryAsAlgebrasOverALawvereTheory} 
###### Theorem 

A [[concrete category]] $U \colon C \to Set$ is a category of algebras over a Lawvere theory precisely if $U$ 

1. is [[monadic functor|monadic]] 

1. is _finitary_ in that it preserves [[filtered colimits]]. 

=-- 

Another characterization is:

+-- {: .num_example #BirkhoffHSP}
###### Theorem 
**([[Birkhoff's HSP theorem]])**

Suppose given a [[language]] $L$ generated by a set of (single-sorted) finitary operations, and a [[class]] $C$ of [[structures]] for $L$. Then $C$ is the class of models for a set of universally quantified equations between terms of $L$ if and only if 

1. (H) The class is closed under homomorphic [[images]], 

1. (S) The class is closed under subalgebras, 

1. (P) The class is closed under taking products. 

=--




### Some non-examples 
 {#SomeNonExamples}

Here are some notable examples of mathematical structures that look algebraic, but are not models of an algebraic theory in the present sense: 

* The class of [[fields]] is not the class of algebras of a Lawvere theory. 

* Neither is the class of [[integral domains]]. 

This might seem obvious since multiplicative inversion in fields is not a global operation, or otherwise the cancellation law of multiplication in integral domains is not a universally quantified axiom (since we have to make an exception of $0$). But one should be careful that there isn't some sneaky alternative axiomatization for these structures which counters these objections! 

The first clause in Theorem \ref{RecognizingAConcreteCategoryAsAlgebrasOverALawvereTheory} already rules out fields, since $U$ in that case will create [[limits]] in $C$, but the category of fields does not even have [[products]]. Similarly for [[integral domains]]. 

The second clause in Theorem \ref{RecognizingAConcreteCategoryAsAlgebrasOverALawvereTheory} suggests another type of non-example: 

* The category $SLat$ of [[sup-lattices]] is not the category of algebras of a (finitary) Lawvere theory. 

There is a whole class of infinitary sup-operations for sup-lattices (one for every arity = cardinal), but again one may wonder how one rules out any alternative finitary axiomatizations. But this is fairly clear by invoking the second clause and considering the following example: if $U: SLat \to Set$ created filtered colimits, then the countable copower $\mathbb{N} \cdot \mathbf{2}$ of 2-element sup-lattices (which turns out to be the power set $P(\mathbb{N})$ with its usual order) would be the filtered colimit (in fact a union) over finite subsets $S$ of finite copowers $S \cdot \mathbf{2}$, hence a countable union of finite sup-lattices, which is clearly impossible. 



## Properties


### Coequalizers of $T$-algebras

+-- {: .un_def}
###### Definition (congruence)
{#congruence}

Let $T$ be a Lawvere theory and $A$ a $T$-algebra. A **[[congruence]]**  on $A$  is an [[equivalence relation]] on the set $A(1)$ such that whenever for all $n \in \mathbb{N}$ whenever any $(a_i \in A(1))_{i=1}^n$ and $(b_i \in A(1))_{i=1}^n$ are pairwise eqivalent, $a_i \sim b_i$, then also for every operation $f \in T(n,1)$ the results are equivalent: $f(a_1, \cdot, a_n) \sim f(b_1, \cdots , b_n)$.

=--

+-- {: .un_lemma}
###### Observation/Definition

For $A$ a $T$-algebra and for every [[relation]] $R \subset A(1) \times A(1)$ there is a smallest [congruence](#congruence) on $A$ containing $R$. Write $\langle R \rangle \subset A(1) \times A(1)$ for this smallest congruence.

=--

+-- {: .un_prop}
###### Proposition

For $A$ a $T$-algebra and $C$ a congruence on $A$, the relation $A/C(f) \subset (A/C)^n \times A/C$ induced by $A(f)$ for each $f : \in T(n,1)$ are functions and define a $T$-algebra structure on $A(1)/C$.

=--

+-- {: .un_prop}
###### Proposition

For $f,g : A \to B$ two morphisms of $T$-algebras, the canonical morphism
$B \to B/\langle \f(a)\sim g(a) | a \in A(1)\rangle$ is the [[coequalizer]] of $f$ and $g$.

=--




### Free $T$-algebras and underlying sets {#FreeAlgebras}


Write $\mathcal{S}$ for the (syntactic category of the) algebraic theory of sets (described [above](#TheoryOfSets)). Then for $T$ any other (syntactic category of a) Lawvere theory, there is a canonical morphism

$$
  i_T :  \mathcal{S} \to T
  \,.
$$

By precomposition with $i_T$ we obtain a corresponding functor on $T$-algebras, which we write

$$
  U_T : T Alg \to Set
$$

and call the **underlying set** functor.

+-- {: .un_lemma}
###### Lemma

The functor $U_T$ has a [[left adjoint]] $F_T : Set \to T Alg$.

=--

This is a standard example of a [[free functor]], called the **free $T$-algebra functor**.

+-- {: .proof}
###### Proof

For $S \in $ [[Set]], let $F_T(S)$ be the $T$-algebra whose underlying set is the set of formal expressions $\{f(s_1, \cdots, s_n) | f \in T(n,1), s_i \in S\}$ with the evident composition operation. 

=--


+-- {: .un_lemma}
###### Observation


For $S = (n) \in$ [[FinSet]] a _finite set_ with $n$ elements , the free $T$-algebra on $S$ is just the [[representable functor|representable]]

$$
  F_T(S) = T(n,-) : T \to Set
  \,.
$$

The adjunction isomorphism

$$
  T Alg(F_T(S), A) \simeq Set(S, U_T(A)) \simeq  (A(1))^n \simeq A(n)
$$

is in this case just the [[Yoneda lemma]].

$$
  T Alg(T(n,-),A) \simeq A(n)
  \,.
$$

Notice that this extends to a functor

$$
  F_T(-) : FinSet \to T Alg
$$

which is the composite

$$
  F_T(-) : FinSet \stackrel{i_T^{op}}{\to} T^{op}
  \stackrel{j}{\to}
  T Alg
$$

of the [[Yoneda embedding]] with the opposite of the canonical functor
$i_T : FinSet^{op} \simeq \mathcal{S} \to T$ from the theory of sets,
described [above](#TheoryOfSets).

More generally, for $S \in Set$ not necessarily finite, let
$Sub(S)$ be the [[poset]] of finite subsets of $S$ and their inclusions.

Then $F_T(S)$ is the [[filtered colimit]] of the representables 
corresponding to the finite subsets

$$
  F_T(S) \simeq {\lim_{\to}}_{{n \in Sub(S)}} T(n,-)
  \,.
$$

As discussed [below](#CoLimitsOfTAlgebras), these filtered colimits of $T$-algebras are computed objectwise.

=--




### Adjunctions of relatively free $T$-algebras {#AdjCatAlgs}


The following establishes that more generally any morphism of Lawvere theories leads to an adjunction between their categories of algebras. 


Let $T_1$ and $T_2$ be Lawvere theories and $f : T_1 \to T_2$ a morphism. Write
$f^* : T_2 Alg \to T_1 Alg $ for the functor on categories of algebras induced by precomposition with $f$.

+-- {: .un_lemma}
###### Lemma

The functor $f^*$ has a [[left adjoint]] $f_* : T_1 Alg \to T_2 Alg$.

=--

+-- {: .proof}
###### Proof

Here is an elementary proof:

Let $F_{T_i} \dashv U_{T_i}$ be the two [free algebra/underlying-set adjunctions](#FreeAlgebras). For $A$ a $T_1$-algebra there is a $T_1$-[congruence](#congruence) $\Gamma$ such that

$$
  A \simeq F_{T_1} U_{T_1}(A) / \Gamma
  \,.
$$ 

Since for any set $S$ we have $U_{T_1} F_{T_1}(S) \subset U_{T_2} F_{T_2}(S)$ it follows that $\Gamma \subset T_{T_2} F_{T_2} U_{T_1}(A)$. For $\langle \Gamma \rangle$ the smallest $T_2$-congruence containing $\Gamma$ we have that $F_{T_2} U_{T_1}(A) / \langle \Gamma \rangle$ is a $T_2$-algebra. 

This one checks is  $f_* A$.


Here is a more high-powered way to obtain this using the [[monad]]s $K_i$ whose algebras are $T_i$-algebras:

for $A$ a $T_1$-algebra let $f_* A  := K_2 \circ_{K_1} A$ the the evident reflexive [[coequalizer]] 

$$
  K_2 K_1 A \stackrel{\to}{\to} K_2 A \to K_2 \circ_{K_1} A
$$ 

in $T_2 Alg$.

=--

### Limits and colimits of $T$-algebras {#CoLimitsOfTAlgebras}

+-- {: .un_prop}
###### Proposition

For $T$ a Lawvere theory, the category $T Alg$ has all small [[limit]]s and [[colimit]]s. 

The [[limit]]s and the [[filtered colimit]]s in $T Alg$ are computed pointwise.


=--

## An open problem

A [[Higman's embedding theorem|famous result by G. Higman]] in group theory says that a finitely generated group can be embedded in a finitely presented group precisely if it has a presentation whose defining relations are a recursively enumerable set of words. Clearly, this question can be asked for every similar algebraic theory and it has been in fact conjectured by the group theorist W. Boone that the same result holds more generally for every single-sorted algebraic theory.  While in fact the conjecture is not true for all single-sorted algebraic theories (see [[Boone conjecture]] for further details), as was known by Soviet mathematicians, the general question "In which algebraic categories does (an analogue of) Higman's embedding theorem hold?" is still interesting. In fact, it has been urged by [[F. W. Lawvere]] on several occasions that this [[Boone conjecture]] should be settled by the category theory community.

## Related concepts

* [[algebraic theory]] / [[generalized algebraic theory]] / **Lawvere theory** /  [[2-Lawvere theory]] [[(∞,1)-algebraic theory]]

* [[enriched Lawvere theory]]

* [[globular theory]]

* [[lambda theory]]

* [[monad]] / [[(∞,1)-monad]]

* [[operad]] / [[(∞,1)-operad]]

* [[PRO]]

* [[PROP]]

* [[C-systems]]

* [[Boone conjecture]]

* [[Freyd category]]

## References

The origin of the categorical formulation of [[algebraic theories]] as Lawvere theories is in

* [[William Lawvere]], [[Functorial Semantics of Algebraic Theories]] , Ph.D. thesis Columbia University (1963).  Published with an author's comment and a supplement in: Reprints in Theory and Applications of Categories **5** (2004) pp 1--121. ([abstract](http://www.tac.mta.ca/tac/reprints/articles/5/tr5abs.html))

The concept was then streamlined in

* [[Samuel Eilenberg]], J. B. Wright, _Automata in General Algebras_ , Information and Control **11** (1967) pp.452-470.

Also still worthwhile reading are the following early papers:

* [[Gavin Wraith]], _Algebraic Theories_ , Aarhus Lecture Notes Series no.22 (1969). ([pdf, 3,7MB](http://homepages.inf.ed.ac.uk/s0894694/scans/wraith-algebraic-theories.pdf))

* [[Gavin Wraith]], _Algebras over Theories_ , Colloquium Mathematicum **XXIII** no.2 (1971) pp.181-190. ([pdf](https://eudml.org/doc/archive%5Cdsc_569f%5Cdsc_40fc%5C/bwmeta1.element.desklight-374f9cbc-939c-4bdb-8b0c-c21872987c9a/full-text/cm23_2_01.pdf))

An early textbook treatment was in

* {#Pareigis70} [[Bodo Pareigis]], _Categories and Functors_ , New York: Academic Press 1970. (chap. 3; [link](https://epub.ub.uni-muenchen.de/7244/))

Modern textbook treatments are

* [[Francis Borceux]], _Handbook of categorical algebra 2 -- Categories and structures_ , Encyclopedia of Mathematics and its Applications, Cambridge UP 1994. (chap. 3)

* M. C. Pedicchio,  F. Rovatti, _Algebraic Categories_ , pp.269-310 in Pedicchio, Tholen (eds.), _Categorical Foundations_ , Encyclopedia of Mathematics and its Applications **97**, Cambridge UP 2004.

A recent monograph is

* [[Jiri Adamek|J. Adámek]], [[Jiri Rosicky|J. Rosicky]], [[Enrico Vitale|E. M. Vitale]], _Algebraic Theories - a Categorical Introduction to General Algebra_ , Cambrige UP 2010. ([draft](http://www.iti.cs.tu-bs.de/~adamek/algebraic_theories.pdf))

The concept of an internal algebraic theory in topos theory is dicussed in

* [[Peter Johnstone]], [[Gavin Wraith]], _Algebraic theories in toposes_ , pp.141-242 in LNM **661** Springer Heidelberg 1978. 

* [[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977. (Dover reprint 2014; sec. 6.4, pp.190-198)

For a comparison with the concept of monads see

* [[Martin Hyland]], [[John Power]], _The Category Theoretic Understanding of Universal Algebra: Lawvere Theories and Monads_ , Electronic Notes in Theor. Comp. Sci. **172** (2007) pp.437-458. ([preprint](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2007/hp07.pdf))

[[distributive law|Distributive laws]] for algebraic theories are discussed in

* [[Eugenia Cheng]], _Distributive laws for Lawvere theories_ , arXiv:1112.3076 (2011). ([abstract](http://arxiv.org/abs/1112.3076))

Voevodsky proves an equivalence between Lawvere theories and l-bijective [[C-systems]] here:

* [[Vladimir Voevodsky]] {#Voevodsky},  Lawvere theories and C-systems, arXiv:1512.08104 (2015). ([abstract](http://arxiv.org/abs/1512.08104))

Other references are

* M. Jibladze, T. Pirashvili, _Cohomology of Algebraic Theories_ , J. Algebra **137** no.2 (1991) pp.253&#8211;296.

* [[Steve Lack]], [[Jiri Rosicky]], _Notions of Lawvere theory_ , arXiv:0810.2578. ([abstract](http://arxiv.org/abs/0810.2578))

* [[Enrico Vitale]], _Localization of Algebraic Categories_ , JPAA **108** (1996) pp.315-320.

* [[Enrico Vitale]], _Localization of Algebraic Categories 2_ , JPAA **133** (1998) pp.317-326.

Lawvere theories, and finitary monads, are identified with certain [[enriched categories]] and the passage from one to the other with a [[cocompletion]], in

* [[Richard Garner]], *Lawvere theories, finitary monads and Cauchy-completion*, 2013, [arxiv](https://arxiv.org/abs/1307.2963)

* [[Richard Garner]] and [[John Power]], *An enriched view on the extended finitary monad--Lawvere theory correspondence*, 2017, [arxiv](https://arxiv.org/abs/1707.08694)


[[!redirects lawvere theory]]
[[!redirects Lawvere theory]]
[[!redirects Lawvere theories]]
[[!redirects finitary Lawvere theory]]
[[!redirects finitary Lawvere theories]]

[[!redirects finite-product theory]]
[[!redirects finite-product theories]]
[[!redirects finite product theory]]
[[!redirects finite product theories]]
[[!redirects finite-products theory]]
[[!redirects finite-products theories]]
[[!redirects finite products theory]]
[[!redirects finite products theories]]