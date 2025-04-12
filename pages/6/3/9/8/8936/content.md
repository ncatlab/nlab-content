[[!redirects axiom UIP]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundational axiom
+-- {: .hide}
[[!include foundational axiom - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

In [[dependent type theory]], _uniqueness of identity proofs_ or _UIP_ refers to a couple of different axioms and rules applicable to individual [[types]] to turn them into [[h-sets]], [[type families]] to turn them into [[families of sets]] (and in particular, [[universes]] to turn them into internal types of sets), as well as the type theory as a whole to turn it into an actual [[set-level type theory]], where all types are [[h-sets]]. Under certain conditions, uniqueness of identity proofs for universes is incompatible with the [[univalence axiom]], and uniqueness of identity proofs for the whole type theory is incompatible with the existence of a [[univalent universe]]. 

Heuristically, the axiom asserts that for each element $a:A$ and $b:A$, every two [[identification]] $p:\mathrm{Id}_A(a, b)$ and $q:\mathrm{Id}_A(a, b)$ of the [[identity type]] $\mathrm{Id}_A(a, b)$ are [[typal equality|typally equal]] to each other. This is equivalent to saying that every identity type $\mathrm{Id}_A(a, b)$ is an [[h-proposition]]. 

## Statement

There are multiple notions of uniqueness of identity proofs: for individual types, for type families and Tarski universes, and for the type theory itself. 

### For individual types

Given a type $A$, uniqueness of identity proofs is the axiom that for all elements $a:A$ and $b:A$ and identifications $p:\mathrm{Id}_A(a, b)$ and $q:\mathrm{Id}_A(a, b)$, there is an identification $\mathrm{UIP}_A(a, b, p, q):\mathrm{Id}_{\mathrm{Id}_A(a, b)}(p, q)$. This is the same as stating that there is a dependent function
$$\mathrm{UIP}_A:\prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} \prod_{q:\mathrm{Id}_A(a, b)} \mathrm{Id}_{\mathrm{Id}_A(a, b)}(p, q)$$

Uniqueness of identity proofs implies that $A$ is an [[h-set]], and can be used in the definition of an [[h-set]]. 

### For type families and universes

Uniqueness of identity proofs for type families $(A, B)$ says that given a type $A$ with a type family $B(a)$ indexed by elements $a:A$, the typal uniqueness of identity proofs holds for the dependent type $B(a)$ of every element of the index type $a:A$. This is the same as stating that there is a dependent function

$$\mathrm{UIP}_{A, B}: \prod_{a:A} \prod_{b:B(a)} \prod_{c:B(a)} \prod_{p:\mathrm{Id}_{B(a)}(b, c)} \prod_{q:\mathrm{Id}_{B(a)}(b, c)} \mathrm{Id}_{\mathrm{Id}_{B(a)}(b, c)}(p, q)$$

This definition of uniqueness of identity proofs could be used in the definition of [[family of sets]]. Since this definition applies to type families, this should probably be called the **familial uniqueness of identity proofs** to distinguish it from the uniqueness of identity proofs axiom above. 

Since every Tarski universe consists of a type $U$ of encodings and a type family $T$ representing the actual small types indexed by the type $U$, with addition structure representing the closure of $U$ under all type formers, the familial uniqueness of identity proofs definition works for Tarski universes as well, and this could equivalently be called the **Tarski universe uniqueness of identity proofs**. 

### As a rule in the type theory

Uniqueness of identity proofs could also be rewritten as a rule instead of an axiom, by making the hypotheses of the axioms into premises of the rule. This makes uniqueness of identity proofs applicable not only to universes, but to the entire type theory. In addition, one could use, in addition to [[typal equality]], either [[judgmental equality]] or [[propositional equality]], resulting in **judgmental uniqueness of identity proofs** and **propositional uniqueness of identity proofs**, with the original uniqueness of identity proofs axiom called **typal uniqueness of identity proofs**

In this manner, uniqueness of identity proofs then becomes the rules:

* Judgmental uniqueness of identity proofs

$$\frac{\Gamma \vdash A \; type \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash q:\mathrm{Id}_A(a, b)}{\Gamma \vdash p \equiv q:\mathrm{Id}_A(a, b)}$$

* Propositional uniqueness of identity proofs

$$\frac{\Gamma \vdash A \; type \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash q:\mathrm{Id}_A(a, b)}{\Gamma \vdash p =_{\mathrm{Id}_A(a, b)} q \; \mathrm{true}}$$

* Typal uniqueness of identity proofs

$$\frac{\Gamma \vdash A \; type \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash q:\mathrm{Id}_A(a, b)}{\Gamma \vdash \mathrm{UIP}_A(a, b, p, q):\mathrm{Id}_{\mathrm{Id}_A(a, b)}(p, q)}$$

Uniqueness of identity proofs is a [[axiom of set truncation]], and turns the type theory into a [[set-level type theory]]. Judgmental uniqueness of identity proofs holds in [[XTT]], where it follows from [[boundary separation]]. 

### Uniqueness of identity proofs for indexed heterogeneous identity types

There is also a notion of uniqueness of identity proofs for [[indexed heterogeneous identity types]] over a type $B$, which is given by the following rule:

* Judgmental uniqueness of identity proofs for indexed heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma \vdash  a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B \\
     \Gamma \vdash q:\mathrm{hId}_{B}(a, b, p, y, z) \quad \Gamma \vdash r:\mathrm{hId}_{B}(a, b, p, y, z)
    \end{array}
}{\Gamma \vdash q \equiv r:\mathrm{hId}_{B}(a, b, p, y, z)}$$

* Typal uniqueness of identity proofs for indexed heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma \vdash  a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B \quad \Gamma \vdash z:B \\
     \Gamma \vdash q:\mathrm{hId}_{B}(a, b, p, y, z) \quad \Gamma \vdash r:\mathrm{hId}_{B}(a, b, p, y, z)
    \end{array}
}{\Gamma \vdash \mathrm{UIP}_{B}(a, b, p, y, z, q, r):\mathrm{Id}_{\mathrm{hId}_{B}(a, b, p, y, z)}(q, r)}$$

and likewise for indexed heterogeneous identity types over a type family $x:A \vdash B(x)$:

* Judgmental uniqueness of identity proofs for indexed heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash  a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \\
     \Gamma \vdash q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \quad \Gamma \vdash r:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)
    \end{array}
}{\Gamma \vdash q \equiv r:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)}$$

* Typal uniqueness of identity proofs for indexed heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash  a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \\
     \Gamma \vdash q:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \quad \Gamma \vdash r:\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)
    \end{array}
}{\Gamma \vdash \mathrm{UIP}_{x:A.B(x)}(a, b, p, y, z, q, r):\mathrm{Id}_{\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)}(q, r)}$$

## Properties

### Uniqueness of identity proofs and univalence

In this section we assume that the universe is a Tarski universe. Uniqueness of identity proofs is inconsistent with having a [[univalent type with a type family]] $(A, B)$ with at least one term $a:A$ where the dependent type $B(a)$ is provably not a proposition
$$\left(\prod_{p:B(a)}  \prod_{q:B(a)} \mathrm{Id}_{B(a)}(p, q)\right) \to \emptyset$$
because by univalence, $A$ is then provably not a set, which contradicts uniqueness of identity proofs. 
In particular, having a [[univalent universe]] $(U, T)$ in the type theory is inconsistent with uniqueness of identity proofs. 

The familial uniqueness of identity proofs axiom applied to Tarski universes implies that for all $A:U$ the type $T(A)$ is a set. This means the type reflection of the internal equivalences $T(A \simeq_U B)$ is an [[h-set]], and the [[univalence axiom]] then implies that $U$ is an [[h-groupoid]]. If $U$ has [[h-sets]] which can be proven not to be an [[h-proposition]], such as the [[booleans type]], then $U$ is provably not an [[h-set]]. 

However, unlike the case for uniqueness of identity proofs, the familial uniqueness of identity proofs and the univalence axiom for universes are inconsistent with each other only if the Tarski universe $U$ has objects which can be proven not to be an [[h-set]], such as internal univalent Tarski universes $V:U$ where the type $T(V)$ has terms $A:T(V)$ such that $T_V(A)$ is an [[h-set]] which is not an [[h-proposition]], such as the [[booleans type]]. As a result, $T(V)$ can be proven to not be a set, causing uniqueness of identity proofs for $U$ to be inconsistent with the existence of $V:U$ and univalence. 

## Related concepts

* [[axiom of set truncation]]

* [[axiom K]]

* [[boundary separation]]

* [[axiom of circle type localization]]

## References

* "[The groupoid interpretation of type theory](http://www.tcs.ifi.lmu.de/mitarbeiter/martin-hofmann/pdfs/agroupoidinterpretationoftypetheroy.pdf)" [PDF], by Martin Hofmann and Thomas Streicher, 1996.

Discussion in [[Coq]] is in

* Pierre Corbineau, _The K axiom  in Coq (almost) for free_ ([pdf](http://coq.inria.fr/files/adt-2fev10-corbineau.pdf)) 

For definitional UIP in [[XTT]]

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _Cubical syntax for reflection-free extensional equality_. In Herman Geuvers, editor, _4th International Conference on Formal Structures for Computation and Deduction (FSCD 2019)_, volume 131 of _Leibniz International Proceedings in Informatics (LIPIcs)_, pages 31:1-31:25. ([arXiv:1904.08562](https://arxiv.org/abs/1904.08562), [doi:10.4230/LIPIcs.FCSD.2019.31](https://doi.org/10.4230/LIPIcs.FCSD.2019.31))

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _A Cubical Language for Bishop Sets_, Logical Methods in Computer Science, 18 (1), 2022. ([arXiv:2003.01491](https://arxiv.org/abs/2003.01491)). 

[[!redirects uniqueness of identity proofs]]
[[!redirects UIP]]

[[!redirects judgmental uniqueness of identity proofs]]
[[!redirects propositional uniqueness of identity proofs]]
[[!redirects typal uniqueness of identity proofs]]

[[!redirects judgmental UIP]]
[[!redirects propositional UIP]]
[[!redirects typal UIP]]
