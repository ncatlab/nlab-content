
> This article contains a section on the notion of [[type universes]] being relativistic. For the notion of (the [[spacetime]] of) a [[universe]] in [[physics]] being relativistic, see [[special relativity]]. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], **bridge types** are a reflexive type family used in [[explicit parametricity]]. The elements of bridge types are called **bridges**. 

### Finitary bridge types

Finitary bridge types come in $n$-ary forms, for any natural number $n$. Examples include

* Unary bridge types $\mathrm{Br}_A(x)$, in [Bernardy & Moulin 2012](#BM12), [Bernardy, Coquand, & Moulin 2015](#BCM15), [Kolomatskaia & Shulman 2023](#KS23)

* Binary bridge types $\mathrm{Br}_A(x, y)$, in [Cavallo & Harper 2021](#CH21)

[[Narya]] has $n$-ary bridge types for $1 \leq n \leq 9$. 

Unlike identity types, binary bridge types do not have [[transport]]. 

### Infinitary bridge types

There are also bridge types which are not finitary. One such example of "infinitary" bridge types is the bridge types in the [[internal logic|internal]] [[dependent type theory]] of the [[topos of trees]]. 

### General case

More generally, one can consider, for an index type $I$, bridge types that are parameterized by an $I$-indexed family of elements of $A$; that is, 

$$\overline{x}:I \to A \vdash \mathrm{Br}_{A, I}(\overline{x}) \; \mathrm{type}$$

The $n$-ary bridge types are simply the case where the index type $I$ is the standard [[finite type]] with $n$ elements $\mathrm{Fin}(n) \coloneqq \sum_{m:\mathbb{N}} m \lt n$, due to the [[induction principle]] of the [[natural numbers type]]. 

## Properties

### Reflexivity

Bridge types are *reflexive* in that for all elements $x:A$, there is an element 

$$\mathrm{refl}_A(x):\mathrm{Br}_{A, I}(\lambda t.x)$$

where $\lambda t.x:I \to A$ is the [[constant function]] which always returns $x$. 

For $I \equiv \mathrm{bool}$ the [[type of booleans]], this yields the usual notion of reflexivity for binary bridge types $\mathrm{Br}_A(x, y)$, since by the [[induction principle]] of the [[type of booleans]], $\mathrm{Br}_{A, \mathrm{bool}}(\mathrm{rec}_{\mathrm{bool}, A}(x, y))$ is [[equivalence of types|equivalent]] to $\mathrm{Br}_A(x, y)$ and $\mathrm{rec}_{\mathrm{bool}, A}(x, x) \equiv \lambda t.x$. 

Since bridge types are reflexive, we can define the [[diagonal]] as the [[function]]

$$\lambda x.(\lambda t.x, \mathrm{refl}_A(x)):\sum_{\overline{x}:I \to A} \mathrm{Br}_{A, I}(\overline{x})$$

A type $A$ is **[[discrete]]** [[if and only if]] the diagonal is an [[equivalence of types]]. For binary bridge types where $I \equiv \mathrm{bool}$, discreteness is equivalent to saying that the canonical inductively defined family of functions $\mathrm{Id}_A(x, y) \to \mathrm{Br}_A(x, y)$ is an [[equivalence of types]] for all $x:A$ and $y:A$. 

### Function application

In the same way that functions preserve [[identifications]] via [[function application to identifications]], functions preserve bridges via **function application to bridges** or the **action on bridges**. For all functions $\overline{x}:I \to A$ and $f:A \to B$, and bridges $p:\mathrm{Br}_{A, I}(\overline{x})$, there is a bridge $\mathrm{ap}(f, \overline{x}, p):\mathrm{Br}_{A, I}(f \circ \overline{x})$:

$$f:A \to B, \overline{x}:I \to A, p:\mathrm{Br}_{A, I}(\overline{x}) \vdash \mathrm{ap}(f, \overline{x}, p):\mathrm{Br}_{A, I}(f \circ \overline{x})$$

For $I \equiv \mathrm{bool}$ the [[type of booleans]] and $\overline{x} \equiv \mathrm{rec}_{\mathrm{bool}, A}(x, y)$, this yields the usual notion of the action on bridges on binary bridge types $\mathrm{Br}_A(x, y)$, since by the [[induction principle]] of the [[type of booleans]], $\mathrm{Br}_{A, \mathrm{bool}}(\mathrm{rec}_{\mathrm{bool}, A}(x, y))$ is [[equivalence of types|equivalent]] to $\mathrm{Br}_A(x, y)$. 

Function application to bridges satisfy many of the same [[judgmental equalities]] as function application to identifications. These include, for $f:A \to B$, $g:B \to C$, $\overline{x}:I \to A$, and $p:\mathrm{Br}_{A, I}(\overline{x})$,

$$\mathrm{ap}(\lambda x.x, \overline{x}, p) \equiv p:\mathrm{Br}_{A, I}(\overline{x})$$

$$\mathrm{ap}(\lambda t.x, \overline{x}, p) \equiv \mathrm{refl}_A(x):\mathrm{Br}_{A, I}(\overline{x})$$

$$\mathrm{ap}(g \circ f, \overline{x}, p) \equiv \mathrm{ap}(g, f \circ \overline{x}, \mathrm{ap}(f, \overline{x}, p)):\mathrm{Br}_{C, I}(g \circ f \circ \overline{x})$$

$$\mathrm{ap}(f, \lambda t.x, \mathrm{refl}_A(x)) \equiv \mathrm{refl}_B(f(x)):Br_{B, I}(\lambda t.f(x))$$

## Relativity

There is an analogue of the [[univalence axiom]] for [[type universes]] called **relativity** (see [Cavallo & Harper 2021](#CH21)), which uses bridge types instead of [[identity types]] and types of $n$-ary [[type families]] instead of [[types of equivalences]]. A universe is called **relativistic** if it satisfies the **axiom of relativity**:

\begin{definition}
Given an index type $I$ and bridge types $\mathrm{Br}_{A, I}(\overline{x})$, **relativity** for a [[type universe]] $U$ states that for all $I$-indexed type families $\overline{X}:I \to U$, there is an equivalence of types between the bridge type $\mathrm{Br}_{U, I}(\overline{X})$ and the type $\left(\prod_{i:I} \overline{X}(i)\right) \to U$ of $U$-small $I$-ary type families. 
\end{definition}

Special cases of relativity for when the index type $I$ is the [[empty type]], the [[unit type]], and the [[type of booleans]] respectively:

* Nullary relativity of a [[type universe]] $U$, where $I \equiv \emptyset$ the [[empty type]], says that there is an [[equivalence of types]] between the bridge type $\mathrm{Br}_U$ and the type of types $(\mathrm{unit} \to U) \simeq U$, since the nullary product type is the [[unit type]]. 

* Unary relativity of a [[type universe]] $U$, where $I \equiv \mathrm{unit}$ the [[unit type]], says that there is an [[equivalence of types]] between the bridge type $\mathrm{Br}_U(A)$ and the type of type families $(\mathrm{Copy}(A) \to U) \simeq (A \to U)$, since the unary product type is the [[copy type]]. 

* Binary relativity of a [[type universe]] $U$, where $I \equiv \mathrm{bool}$ the [[type of booleans]], says that there is an [[equivalence of types]] between the bridge type $\mathrm{Br}_U(A, B)$ and the type of correspondences $((A \times B) \to U) \simeq (A \to B \to U)$. 

## Related concepts

* [[internal parametricity]]

* [[identity type]]

* [[hom type]]

* [[directed interval]]

* [[displayed coinductive type]]

* [[cubical type theory]]

* [[higher observational type theory]]

* [[displayed type theory]]

* [[symmetric cube category]]

## References

The terminology "bridge" is first used in this sense in

* [[Andreas Nuyts]], [[Andrea Vezzosi]], [[Dominique Devriese]], *Parametric quantifiers for dependent type theory*, Proceedings of the ACM on Programming Languages (ICFP) **1** (2017) 1-29 &lbrack;[doi:10.1145/3110276](https://doi.org/10.1145/3110276)&rbrack;

Bridge types first appear in an unary form, written as $x \in \llbracket A \rrbracket$ rather than $\mathrm{Br}_A(x)$, in

* {#BM12} [[Jean-Philippe Bernardy]] and [[Guilhem Moulin]]. 2012. *A Computational Interpretation of Parametricity.* In Proceedings of the 27th Annual IEEE Symposium on Logic in Computer Science, LICS 2012, Dubrovnik, Croatia, June 25-28, 2012. IEEE Computer Society, 135–144. &lbrack;[doi:10.1109/LICS.2012.25](https://doi.org/10.1109/LICS.2012.25)&rbrack;

An equivalent of univalence for unary bridge types appears (with inverse conditions given by the Pair-Pred and Surj-Typ equations) in

* {#BCM15} [[Jean-Philippe Bernardy]], [[Thierry Coquand]], and [[Guilhem Moulin]]. 2015. *A Presheaf Model of Parametric Type Theory.* In The 31st Conference on the Mathematical Foundations of Programming Semantics, MFPS 2015, Nijmegen, The Netherlands, June 22-25, 2015 (Electronic Notes in Theoretical Computer Science, Vol. 319), Dan R. Ghica (Ed.). Elsevier, 67–82. &lbrack;[doi:10.1016/j.entcs.2015.12.006](https://doi.org/10.1016/j.entcs.2015.12.006)&rbrack;

The equivalent of univalence for (binary) bridge types is called "relativity" in:

* {#CH21} [[Evan Cavallo]] and [[Robert Harper]]. 2021. *Internal Parametricity for Cubical Type Theory.* Log. Methods Comput. Sci. 17, 4 (2021). &lbrack;<a href="https://doi.org/10.46298/lmcs-17(4:5)2021">doi:10.46298/lmcs-17(4:5)2021</a>, [arXiv:2005.11290](https://arxiv.org/abs/2005.11290)&rbrack;

A unary bridge type called "display" and written as $A^d(x)$ instead of $\mathrm{Br}_A(x)$ appears in

* {#KS23} [[Astra Kolomatskaia]], [[Michael Shulman]], *Displayed Type Theory and Semi-Simplicial Types* &lbrack;[arXiv:2311.18781](https://arxiv.org/abs/2311.18781)&rbrack; 

A fibered version of bridge types is defined in:

* {#ACKS24} [[Thorsten Altenkirch]], [[Yorgo Chamoun]], [[Ambrus Kaposi]], [[Michael Shulman]], *Internal parametricity, without an interval*, Proceedings of the ACM on Programming Languages (POPL) **8** (2024) 2340-2369 &lbrack;[arXiv:2307.06448](https://arxiv.org/abs/2307.06448), [doi:10.1145/3632920](https://doi.org/10.1145/3632920)&rbrack;

Bridge types in [[Narya]]:

* *Observational higher dimensions*, [[Narya]] documentation. ([web](https://narya.readthedocs.io/en/latest/observational.html)) 

* *Parametricity*, [[Narya]] documentation. ([web](https://narya.readthedocs.io/en/latest/parametricity.html))

Some discussion of bridge types occurs in 

* {#CTZulip} *synthetic algebraic geometry vs continuation passing style*, Category Theory Zulip, [web](https://categorytheory.zulipchat.com/#narrow/channel/229199-learning.3A-questions/topic/synthetic.20algebraic.20geometry.20vs.20continuation.20passing.20style/with/526838004). 

[[!redirects bridge]]
[[!redirects bridges]]

[[!redirects bridge type]]
[[!redirects bridge types]]

[[!redirects unary bridge type]]
[[!redirects unary bridge types]]

[[!redirects binary bridge type]]
[[!redirects binary bridge types]]

[[!redirects n-ary bridge type]]
[[!redirects n-ary bridge types]]

[[!redirects heterogeneous bridge]]
[[!redirects heterogeneous bridges]]

[[!redirects heterogeneous bridge type]]
[[!redirects heterogeneous bridge types]]

[[!redirects relativity axiom]]
[[!redirects axiom of relativity]]