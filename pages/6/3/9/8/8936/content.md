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

Uniqueness of identity proofs could also be rewritten as a rule instead of an axiom, by making the hypotheses of the axioms into premises of the rule. This makes uniqueness of identity proofs applicable not only to universes, but to the entire type theory. In addition, one could use [[judgmental equality]] in addition to [[typal equality]], resulting in **judgmental uniqueness of identity proofs**, with the original uniqueness of identity proofs axiom called **typal uniqueness of identity proofs**

In this manner, uniqueness of identity proofs then becomes the rules:

* Judgmental uniqueness of identity proofs

$$\frac{\Gamma \vdash A \; type \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash q:\mathrm{Id}_A(a, b)}{\Gamma \vdash p \equiv q:\mathrm{Id}_A(a, b)}$$

* Typal uniqueness of identity proofs

$$\frac{\Gamma \vdash A \; type \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_A(a, b) \quad \Gamma \vdash q:\mathrm{Id}_A(a, b)}{\Gamma \vdash \mathrm{UIP}_A(a, b, p, q):\mathrm{Id}_{\mathrm{Id}_A(a, b)}(p, q)}$$

Uniqueness of identity proofs is a [[axiom of set truncation]], and turns the type theory into a [[set-level type theory]]. Judgmental uniqueness of identity proofs holds in [[XTT]], where it follows from [[boundary separation]], and also in the [[Lean]] [[proof assistant]].  

If the dependent type theory has [[dependent product types]], [[type variables]], and [[impredicative polymorphism]], the typal uniqueness of identity proofs can be expressed as an axiom rather than an axiom schema:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{UIP}:\Pi A.\prod_{a:A} \prod_{b:A} \prod_{p:\mathrm{Id}_A(a, b)} \prod_{q:\mathrm{Id}_A(a, b)} \mathrm{Id}_{\mathrm{Id}_A(a, b)}(p, q)}$$

### As proposition equality reflection

The usual formulations of the uniqueness of identity proofs rely on the definition of a proposition as a type where all elements are [[identified]] with each other:

$$\mathrm{isProp}(A) \coloneqq \prod_{x:A} \prod_{y:A} \mathrm{Id}_A(x, y)$$

There is another definition of a proposition as a type $A$ with a function from $A$ to the type that signifies $A$ is a [[contractible type]]:

$$\mathrm{isProp}(A) \coloneqq A \to \mathrm{isContr}(A)$$

When applied to identity types in the inference rule for the [[uniqueness of identity proofs]], this leads to a propositional version of the judgmental [[equality reflection]] found in [[extensional type theory]] in the following sense:

In the [[propositions as some types]] interpretation of [[dependent type theory]], given a type $A$ and elements $x:A$ and $y:A$, the two elements are *[[propositionally equal]]* [[if and only if]] they are [[uniquely]] [[identified]]; that is, the identity type is a [[contractible type]]. 

$$(x = y) \simeq \mathrm{isContr}(\mathrm{Id}_A(x, y))$$

Since [[isContr]] is always a [[proposition]], the type of witnesses of propositional equality $x = y$ is always a [[relation]]. Indeed, this relation is also [[transitive relation|transitive]] and [[symmetric relation|symmetric]] and satisfies the [[principle of substitution]] and the [[identity of indiscernibles]]. However, it is only a [[reflexive relation]] if and only if [[axiom K]] holds for the type; i.e. if and only if the set is an h-set. 

By definition of $\mathrm{isProp}(\mathrm{Id}_A(x, y))$ as $\mathrm{Id}_A(x, y) \to \mathrm{isContr}(\mathrm{Id}_A(x, y))$, the **uniqueness of identity proofs** says that one can derive the uniqueness of identifications from every [[identification]], yielding a propositional version of the equality reflection rule:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:\mathrm{Id}_A(x, y)}{\Gamma \vdash \mathrm{UIP}_A(x, y, p):x = y}$$

This [[inference rule]] can thus be called **propositional equality reflection**. 

The relation between the [[uniqueness of identity proofs]] and the [[K rule]] becomes clearer in this formulation of the uniqueness of identity proofs: by the [[J rule]], it suffices to prove uniqueness of identity proofs for [[reflexivity]], and the [[K rule]] states that reflexivity is the [[center of contraction]] of the [[loop space type]] for all elements of $A$. 

## Properties

### Relation to the circle type

In this section, we assume that the [[circle type]] $S^1$ is inductively defined using two elements $\mathrm{left}:S^1$ and $\mathrm{right}:S^1$ and a two parallel identifications $\mathrm{upath}:\mathrm{left} =_{S^1} \mathrm{right}$ and $\mathrm{dpath}:\mathrm{left} =_{S^1} \mathrm{right}$, and that $S^1$ has judgmental [[computation rules]]. 

\begin{theorem}
Suppose that the [[circle type]] has an identification $\mathrm{UIP}:\mathrm{upath} = \mathrm{dpath}$. Then the uniqueness of identity proof holds. 
\end{theorem}

\begin{proof}
For all types $A$, terms $x:A$ and $y:A$, and identifications $p:x =_A y$ and $q:x =_A y$, by the recursion principle of the strict circle type defined this way, we have the function $\mathrm{rec}_{S^1}(x, y, p, q):S^1 \to A$ such that 

$$\mathrm{rec}_{S^1}(x, y, p, q)(\mathrm{left}) \equiv x \qquad \mathrm{rec}_{S^1}(x, y, p, q)(\mathrm{right}) \equiv y$$ 
$$\mathrm{ap}_{\mathrm{rec}_{S^1}^A(x, y, p, q)}(\mathrm{left}, \mathrm{right}, \mathrm{upath}) \equiv p \qquad \mathrm{ap}_{\mathrm{rec}_{S^1}^A(x, y, p, q)}(\mathrm{left}, \mathrm{right}, \mathrm{dpath}) \equiv q$$ 
By applying $\mathrm{ap}_{\mathrm{rec}_{S^1}(x, y, p, q)}(\mathrm{left}, \mathrm{right})$ to $\mathrm{UIP}$, we have the identification 
$$\mathrm{ap}_{\mathrm{ap}_{\mathrm{rec}_{S^1}(x, y, p, q)}(\mathrm{left}, \mathrm{right})}(\mathrm{upath}, \mathrm{dpath}, \mathrm{UIP}):\mathrm{ap}_{\mathrm{rec}_{S^1}(x, y, p, q)}(\mathrm{left}, \mathrm{right}, \mathrm{upath}) = \mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{left}, \mathrm{right}, \mathrm{dpath})$$
which reduces down to 
$$\mathrm{ap}_{\mathrm{ap}_{\mathrm{rec}_{S^1}(x, y, p, q)}(\mathrm{left}, \mathrm{right})}(\mathrm{upath}, \mathrm{dpath}, \mathrm{UIP}):p = q$$
which is precisely the [[uniqueness of identity proofs]] for type $A$. 
\end{proof}

\begin{theorem}
Suppose that the two parallal identifications of the strict circle type are [[judgmentally equal]] to each other of the base of the circle $\mathrm{upath} \equiv \mathrm{dpath}:\mathrm{left} =_{S^1} \mathrm{right}$. Then the [[judgmental uniqueness of identity proofs]] holds.
\end{theorem}

\begin{proof}
For all types $A$, terms $x:A$ and $y:A$, and identifications $p:x =_A y$ and $q:x =_A y$, by the recursion principle of the strict circle type defined this way, we have the function $\mathrm{rec}_{S^1}(x, y, p, q):S^1 \to A$ such that 

$$\mathrm{rec}_{S^1}(x, y, p, q)(\mathrm{left}) \equiv x \qquad \mathrm{rec}_{S^1}(x, y, p, q)(\mathrm{right}) \equiv y$$ 
$$\mathrm{ap}_{\mathrm{rec}_{S^1}^A(x, y, p, q)}(\mathrm{left}, \mathrm{right}, \mathrm{upath}) \equiv p \qquad \mathrm{ap}_{\mathrm{rec}_{S^1}^A(x, y, p, q)}(\mathrm{left}, \mathrm{right}, \mathrm{dpath}) \equiv q$$ 
By the [[congruence rules]] of [[judgmental equality]] applied to the [[function]] $\mathrm{ap}_{\mathrm{rec}_{S^1}(x, y, p, q)}(\mathrm{left}, \mathrm{right})$ to $\mathrm{UIP}$, we have the judgmental equality 
$$p \equiv \mathrm{ap}_{\mathrm{rec}_{S^1}(x, y, p, q)}(\mathrm{left}, \mathrm{right}, \mathrm{upath}) \equiv \mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{left}, \mathrm{right}, \mathrm{dpath}) \equiv q$$
which is precisely the [[judgmental uniqueness of identity proofs]] for type $A$. 
\end{proof}

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

* [[circle type]]

* [[axiom of circle type localization]]

* [[equality reflection]]

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
[[!redirects definitional uniqueness of identity proofs]]
[[!redirects propositional uniqueness of identity proofs]]
[[!redirects typal uniqueness of identity proofs]]

[[!redirects judgmental UIP]]
[[!redirects definitional UIP]]
[[!redirects propositional UIP]]
[[!redirects typal UIP]]

[[!redirects proof irrelevance]]

[[!redirects judgmental proof irrelevance]]
[[!redirects definitional proof irrelevance]]
[[!redirects propositional proof irrelevance]]
[[!redirects typal proof irrelevance]]

[[!redirects propositional equality reflection]]
[[!redirects propositional equality reflection rule]]
[[!redirects propositional equality reflection rules]]