+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

*Disambiguation: For axiom K as a principle of [[modal logic]], see [[axiom K (modal logic)]]*

# Contents
* table of contents
{: toc}

## Idea 

In [[intensional type theory]], _axiom K_ refers to a couple of different axioms and rules applicable to individual [[types]] to turn them into [[h-sets]], [[type families]] to turn them into [[families of sets]] (and in particular, [[universes]] to turn them into internal types of sets), as well as the type theory as a whole to turn it into an actual [[set-level type theory]], where all types are [[h-sets]]. Under certain conditions, axiom K for universes is incompatible with the [[univalence axiom]], and axiom K for the whole type theory is incompatible with the existence of a [[univalent universe]]. 

Heuristically, the axiom asserts that each [[term]] of each [[identity type]] $x =_A x$ (of [[equivalences]] of a [[term]] $x:A$) is [[propositional equality|propositionally equal]] to the canonical [[reflexive relation|reflexivity]] equality proof $refl_A(x):x =_A x$. 

## Statement

There are multiple notions of axiom K: for individual types, for type families and Tarski universes, and for the entire type theory itself. 

### For individual types

The following definition is adapted from theorem 7.2.1 of the [[HoTT book]].  Given a type $A$, axiom K is the axiom that for all elements $a:A$ and identifications $p:a =_A a$, there is an identification $K(a, p):p =_{a =_A a} \mathrm{refl}_A(a)$. This is the same as stating that there is a dependent function
$$K_A: \prod_{a:A} \prod_{p:a =_A a} p =_{a =_A a} \mathrm{refl}_A(a)$$

Axiom K implies that $A$ is an [[h-set]], and can be used in the definition of an [[h-set]]. Since this axiom K applies to types, it should probably be called the **typal axiom K** to distinguish it from other axioms K.

### For type families and universes

Axiom K for type families $(A, B)$ says that given a type $A$ with a type family $B(a)$ indexed by elements $a:A$, the typal axiom K holds for the dependent type $B(a)$ of every element of the index type $a:A$. This is the same as stating that there is a dependent function

$$K_{A, B}: \prod_{a:A} \prod_{b:B(a)} \prod_{p:b =_{B(a)} b} p =_{b =_{B(a)} b} \mathrm{refl}_{B(a)}(b)$$

This definition of axiom K could be used in the definition of [[family of sets]]. Since this definition applies to type families, this should probably be called the **familial axiom K** to distinguish it from the typal axiom K above. 

Since every Tarski universe consists of a type $U$ of encodings and a type family $T$ representing the actual small types indexed by the type $U$, with addition structure representing the closure of $U$ under all type formers, the familial axiom K definition works for Tarski universes as well, and this could equivalently be called the **Tarski universe axiom K**. 

### For the entire type theory

In the same manner that [[uniqueness of identity proofs]] could be expressed as a rule instead of an [[axiom]], Axiom K could also be rewritten as a rule instead of an axiom, by making the hypotheses of the axioms into premises of the rule. This makes axiom K applicable not only to universes, but to the entire type theory. In this manner, axiom K then becomes the rule

$$
\frac{\Gamma\vdash A\; type \quad \Gamma\vdash a : A \quad  \quad \Gamma \vdash p : a =_A a}{
  \Gamma\vdash K : p =_{a =_A a} refl_A(a)}
$$

This should probably be called the **K rule** rather than axiom K, since it is no longer an axiom. 

Adding this rule to the type theory turns it into a [[set-level type theory]]. 

### Definitional K

There is also a version of the K rule called the **definitional K rule** which uses [[definitional equality]] instead of the [[identity type]]. It is given by the following rule
$$
\frac{\Gamma\vdash A\; type \quad \Gamma\vdash a : A \quad  \quad \Gamma \vdash p : a =_A a}{
  \Gamma\vdash p \equiv refl_A(a):a =_A a}
$$
Similarly to the typal K rule, adding the definitional K rule to a type theory turns it into a [[set-level type theory]]. The definitional K rule holds in [[XTT]], where it follows from the definitional UIP rule, which in turn follows from [[boundary separation]]. 

## Properties

### Axiom K and univalence

In this section we assume that the universe is a Tarski universe. The K rule is inconsistent with having a [[univalent type with a type family]] $(A, B)$ with at least one term $a:A$ where the dependent type $B(a)$ is provably not a proposition
$$\left(\prod_{p:B(a)}  \prod_{q:B(a)} p =_{B(a)} q\right) \to \emptyset$$
because by univalence, $A$ is then provably not a set, which contradicts the K rule. 
In particular, having a [[univalent universe]] $(U, T)$ in the type theory is inconsistent with the K rule. 

The familial axiom K applied to Tarski universes implies that for all $A:U$ the type $T(A)$ is a set. This means the type reflection of the internal equivalences $T(A \simeq_U B)$ is an [[h-set]], and the [[univalence axiom]] then implies that $U$ is an [[h-groupoid]]. If $U$ has [[h-sets]] which can be proven not to be an [[h-proposition]], such as the [[booleans type]], then $U$ is provably not an [[h-set]]. 

However, unlike the case for the K rule, the familial axiom K and the univalence axiom for universes are inconsistent with each other only if the Tarski universe $U$ has objects which can be proven not to be an [[h-set]], such as internal univalent Tarski universes $V:U$ where the type $T(V)$ has terms $A:T(V)$ such that $T_V(A)$ is an [[h-set]] which is not an [[h-proposition]], such as the [[booleans type]]. As a result, $T(V)$ can be proven to not be a set, causing axiom K for $U$ to be inconsistent with the existence of $V:U$ and univalence. 

### Computational behavior

Unlike its logical equivalent [[axiom UIP]], axiom K can be endowed with computational behavior: $K(A,x,P,d,refl_A x)$ computes to $d$.  This gives a way to specify a computational set-level type theory.

This sort of computational axiom K can also be implemented with, and is sufficient to imply, a general scheme of function definition by pattern-matching.  This is implemented in the proof assistant [[Agda]].  (The flag `--without-K` alters Agda's pattern-matching scheme to a weaker version appropriate for [[intensional type theory]], including [[homotopy type theory]].)

## Related concepts

* [[uniqueness of identity proofs]]

* [[boundary separation]]

## References

The axiom K was introduced in 

* [[Thomas Streicher]], _Investigations into intensional type theory_ Habilitation thesis (1993) ([pdf](http://www.mathematik.tu-darmstadt.de/~streicher/HabilStreicher.pdf))

For a review and discussion of the implementation in [[Coq]], see

* Pierre Corbineau, _The K axiom  in Coq (almost) for free_ ([pdf](http://coq.inria.fr/files/adt-2fev10-corbineau.pdf)) 

Discussion in the context of [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

around theorem 7.2.1

[[!redirects Streicher axiom K]]
[[!redirects Streicher's axiom K]]
[[!redirects Streicher's axiom K]]
[[!redirects Streicher\'s axiom K]]
[[!redirects Axiom K (type theory)]]

[[!redirects K rule]]
[[!redirects definitional K rule]]
[[!redirects definitional K]]