
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed Type Theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

*Simplicial type theory* is a [[cohesive homotopy type theory]] which is used to represent the internal logic of [[cohesive (infinity,1)-topos|cohesive]] [[locally cartesian closed (infinity,1)-category|locally cartesian closed $(\infty,1)$-categories]] of [[simplicial objects in an (infinity,1)-category|simplicial objects]] in a locally cartesian closed $(\infty,1)$-category. One can think of simplicial type theory as a [[synthetic mathematics|synthetic]] theory of [[simplicial anima]], since the [[cohesive (infinity,1)-topos]] $\mathrm{Ani}^{\Delta^\op}$ of [[simplicial anima]] is the characteristic example of a cohesive locally cartesian closed $(\infty,1)$-category of simplicial objects in a locally cartesian closed $(\infty,1)$-category. 

Simplicial type theory is used to construct various [[geometric shape for higher structures|geometric shapes]] [[internal logic|internally]], such as [[Segal types]] (i.e. [[Segal space]]-types), [[complete Segal types]] (i.e. [[complete Segal space]]-types), and covariant fibrations. 

## Definition

Simplicial type theory is a [[cohesive homotopy type theory]]: that is, a [[modal type theory]] with a [[sharp modality]], [[flat modality]], and [[shape modality]] [[adjoint triple]]

$$\esh \dashv \flat \dashv \sharp$$

The [[flat modality]] $\flat A$ represents the [[global sections]] [[(infinity,1)-functor]] which takes a [[simplicial anima]] and returns its [[core]] discrete [[anima]]. 

There are also two other modalities

* the [[op modality]] $A^\op$ which reverses all (higher) morphisms in a type. This modality is an [[involution]] on types (i.e. $(A^\op)^\op \simeq A)$), and types have the same core as its opposite $\flat A^\op \simeq \flat A$. The op modality represents the [[opposite simplicial anima]] [[(infinity,1)-functor]]. 

* the [[twisted arrow modality]] $A^\mathrm{tw}$ which represents the [[twisted arrow construction]] [[(infinity,1)-functor]] in [[simplicial anima]]. 

In addition, simplicial type theory comes with a designated [[bounded total order]] $\mathbb{I}$ called a *directed [[interval]]*, such that 

* there is an [[equivalence of types]] $\neg:\mathbb{I}^op \simeq \mathbb{I}$ which swaps $0$ for $1$ and $\max$ for $\min$,

* the [[booleans]] are the global points of $\mathbb{I}$: i.e. the unique endpoints-preserving [[monotonic function]] from the [[boolean domain]] $\mathbb{2}$ to $\mathbb{I}$ is an [[embedding of types]] and the unique endpoints-preserving monotonic function from $\mathbb{2}$ to $\flat \mathbb{I}$ is an [[equivalence of types]],

* the **axiom of simplicial [[axiom of cohesion|cohesion]]**: for all crisp types $A$, the $\flat$-counit $\flat(-):\flat A \to A$ is an [[equivalence of types]] if and only if the function $\mathrm{const}_{A, \mathbb{I}}$ which takes elements of $A$ to constant functions $\mathbb{I} \to A$ is an [[equivalence of types]]. 

* the interval [[cohesive (infinity,1)-topos#A1ExhibitingCohesion|exhibits the cohesion]] of types: the shape modality is equivalent to [[localization of a type|localization]] at $\mathbb{I}$, $\esh A \simeq L_\mathbb{I}(A)$, 

* $n$-cubes detect continuity: for every crisp function $f::A \to B$, $f$ is $\sharp$-modal [[if and only if]] it lifts up against the $\flat$-counit $\flat(-):\flat(\mathrm{Fin}(n) \to \mathbb{I}) \to (\mathrm{Fin}(n) \to \mathbb{I})$ for all crisp natural numbers $n::\mathbb{N}$, where $\mathrm{Fin}(n) \coloneqq \sum_{i:\mathbb{N}} i \lt n$ is the crisp standard [[finite set]] with $n$ elements. 

* $\mathbb{I}$ is [[tiny object|tiny]]: the heterogeneous  [[path space]] [[modality]] $\prod_{i:\mathbb{I}} (-)(i)$ has an [[amazing right adjoint]] $(-)^{1/\mathbb{I}}$. 

* a [[Kock-Lawvere axiom|Kock-Lawvere]]-esque [[duality]] axiom: let $A$ be a finitely presented $\mathbb{I}$-algebra, in the sense that $A$ is a [[distributive lattice]] equivalent to the quotient of $\mathbb{I}[x_1 \ldots x_n]$ by finitely many relations, and let $\mathrm{hom}_{\mathbb{I}\mathrm{Alg}}(A, \mathbb{I})$ be the type of $\mathbb{I}$-algebra homomorphisms. Then the following function is an [[equivalence of types]]

$$\lambda a.\lambda f.f(a):A \to (\mathrm{hom}_{\mathbb{I}\mathrm{Alg}}(A, \mathbb{I}) \to \mathbb{I})$$

### Formalising the bounded total order

There are many different ways to formalize the bounded total order in simplicial type theory: 

* one could simply postulate in vanilla [[dependent type theory]] via inference rules and axioms a [[bounded total order]], as in [Gratzer, Weinberger, & Buchholtz 2024](#GWB24) and [Gratzer, Weinberger, & Buchholtz 2025](#GWB25). 

* one could use [[two-level type theory]] consisting of a non-fibrant layer, and then axiomatise a [[bounded total order]] in the non-fibrant layer 

* one could use [[type theory with shapes]] consisting of a non-fibrant layer of cubes which is a [[simple type theory]] and a non-fibrant layer of topes which is a [[propositional logic]] over the cube layer, and then define the [[bounded total order]] using the cube and tope layers, as in [Riehl & Shulman 2017](#RiehlShulman17). 

The first approach is simpler to define, while the latter two are easier to work with, since the equalities in the interval type are [[judgmental equalities]] rather than [[identifications]], so one doesn't have to deal with [[transport]] hell. 

In the latter two approaches, the [[function type]] $\mathbb{I} \to A$ used in the axiom of cohesion is usually defined as an [[extension type]], while the [[dependent function type]] $\prod_{i:\mathbb{I}} A(i)$ is usually defined as a [[dependent extension type]]. 

## Basic concepts in simplicial type theory

### Shapes in simplicial type theory

Let $\mathrm{Fin}(n) \coloneqq \sum_{i:\mathbb{N}} i \lt n$ be the canonical [[finite type]] with $n$ elements. Given the directed interval $\mathbb{I}$, the $n$-cubes are defined by the function type $\Box^n \coloneqq \mathrm{Fin}(n) \to \mathbb{I}$. 

Subshapes of the cubes could also be defined. 

* The $2$-simplex is defined as
$$\Delta^2 \coloneqq \sum_{t:\mathrm{Fin}(2) \to \mathbb{I}} t(0) \leq t(1)$$

* The horn $\Lambda^2_1$ is defined as
$$\Lambda^2_1 \coloneqq \sum_{t:\mathrm{Fin}(2) \to \mathbb{I}} (t(0) =_{\mathbb{I}} 0) \vee (t(1) =_{\mathbb{I}} 1)$$

Since $t(0) \leq t(1)$ implies $t(0) =_{\mathbb{I}} 0) \vee (t(1) =_{\mathbb{I}} 1)$ for all $t:\mathrm{Fin}(2) \to \mathbb{I}$, we have a canonical function 

$$(\mathrm{id}, P):\Delta^2 \to \Lambda^2_1$$

which is a pair consisting of the [[identity function]] on $\mathrm{Fin}(2) \to \mathbb{I}$ and a [[dependent function]] $P$ that takes the witness that $t(0) \leq t(1)$ to a witness that $(t(0) =_{\mathbb{I}} 0) \vee (t(1) =_{\mathbb{I}} 1)$. By precomposition, this leads to a function 

$$\lambda t.t \circ (\mathrm{id}, P):(\Delta^2 \to A) \to (\Lambda^2_1 \to A)$$

for all types $A$. 

### Morphisms

The [[morphisms]] between elements $x:A$ and $y:A$ in a type $A$ are defined in simplicial type theory as a [[tuple]] consisting of a function $f:\mathbb{I} \to A$ and two identifications $p_0:f(0) = x$ and $p_1:f(1) = y$. The type of morphisms is called a *[[hom-type]]* and is defined as the [[dependent sum type]]

$$\mathrm{hom}_A(x, y) \coloneqq \sum_{f:\mathbb{I} \to A} (f(0) = x) \times (f(1) = y)$$

Given an element $x:A$, the hom-type $\mathrm{hom}_A(x, x)$ has an [[identity morphism]] given by the tuple consisting of the [[constant function]] from $\mathbb{I}$ to $A$ at $x$ and two witnesses that $f(0) = x$ and $f(1) = x$ both derivable from the typal [[computation rules]] for [[function types]]. 

$$\mathrm{id}_A(x) \coloneqq (\lambda t.x, \beta_{\mathbb{I} \to A}^{t.x}(0), \beta_{\mathbb{I} \to A}^{t.x}(1)):\mathrm{hom}_A(x, x)$$

A *composite of morphisms* in a type $A$ is a function $f:\Delta^2 \to A$ from the [[2-simplex]] to $A$. A *pair of composable morphisms* in a type $A$ is a function $g:\Lambda^2_1 \to A$ from the [[horn]] $\Lambda^2_1$ to $A$. 

### Heterogeneous morphisms and covariant type families

Given a type $A$, elements $x:A$ and $y:A$, a function $f:\mathbb{I} \to A$, [[identifications]] $p_0:f(0) =_A x$ and $p_1:f(1) =_A y$ a type family $x:A \vdash B(x)$, and elements $u:B(x)$ and $v:B(y)$, a *[[heterogeneous morphism]]* is a [[tuple]] consisting of a [[dependent function]] $g:\prod_{i:\mathbb{I}} B(f(i))$ and two [[heterogeneous identifications]] 
$$q_0:g(0) =_{t.B(t)}^{(f(0), x, p_0)} u \; \mathrm{and} \; q_1:g(1) =_{t.B(t)}^{(f(1), y, p_1)} v$$ 
where the type $u =_{t.B(t)}^{(x, y, p)} v$ is the [[heterogeneous identity type]] over the type family $x:A \vdash B(x)$. 

The type of heterogeneous morphisms is called the *[[heterogeneous hom-type]]* and is defined as the [[dependent sum type]] 

$$\mathrm{hhom}_{t.B(t)}(x, y, f, p_0, p_1, u, v) \coloneqq \sum_{g:\prod_{i:\mathbb{I}} B(f(i))} (g(0) =_{t.B(t)}^{(f(0), x, p_0)} u) \times (g(1) =_{t.B(t)}^{(f(1), y, p_1)} v)$$ 

A *[[covariant type family]]* is a [[type family]] $x:A \vdash B(x)$ such that for all elements $x:A$, $y:A$, $f:\mathrm{hom}_A(x, y)$, and $u:B(x)$, [[uniqueness quantifier|there exists a unique]] element $v:B(y)$ with a [[heterogeneous morphism]]

$$\mathrm{isCovariant}(t:A.B(t)) \coloneqq \prod_{x:A} \prod_{y:A} \prod_{f:\mathrm{hom}_A(x, y)} \prod_{u:B(x)} \exists!v:B(y).\mathrm{hhom}_{t.B(t)}(x, y, f, p_0, p_1, u, v)$$

### Limits and colimits

Limits and colimits in [[simplicial type theory]] can be defined in an arbitrary type, rather than just the [[Segal types]]. 

Limits include:

* [[terminal object in simplicial type theory]]

* [[product in simplicial type theory]]

Colimits include:

* [[initial object in simplicial type theory]]

* [[coproduct in simplicial type theory]]

## $(\infty,1)$-category theory in simplicial type theory

Since [[simplicial type theory]] is a [[synthetic mathematics|synthetic]] theory of [[simplicial anima]], simplicial type theory is typically used in [[(infinity,1)-category theory]] to define [[Segal spaces]] (i.e. [[Segal types]]) and [[complete Segal spaces]] (i.e. [[complete Segal types]]).

### Segal types and complete Segal types

\begin{definition}
A *[[Segal type]]* is a type $A$ which satisfies the [[Segal condition]]: for every pair of composable morphisms, there exists a unique composite. That is, the canonical function which takes a composite of morphisms to its pair of composible morphisms is an [[equivalence of types]]

$$\mathrm{isEquiv}(\lambda t.t \circ (\mathrm{id}, P))$$ 
\end{definition}

As a result, in a [[Segal type]] $A$, for all elements $x:A$, $y:A$, and $z:A$, one can construct a [[composition]] operation on [[hom-types]] 

$$\lambda (g, f).g \circ f:\mathrm{hom}_A(y, z) \times \mathrm{hom}_A(x, y) \to \mathrm{hom}_A(x, z)$$

which by the uniqueness condition is automatically [[associative]] and [[unital]]. 

The opposite $A^\op$ of a Segal type $A$ is also a Segal type; that is, the opposite modality preserves the [[Segal condition]].

A [[morphism]] $f:\mathrm{hom}_A(x, y)$ between elements $x:A$ and $y:A$ in a type $A$ is an *[[isomorphism]]* if one can construct a morphism $g:\mathrm{hom}_A(y, x)$ such that $g \circ f = \mathrm{id}_A(x)$ and a morphism $h:\mathrm{hom}_A(y, x)$ such that $f \circ h = \mathrm{id}_A(y)$. 

The type of isomorphisms is given by the [[dependent sum type]]

$$\mathrm{iso}_A(x, y) \coloneqq \sum_{f:\mathrm{hom}_A(x, y)} \left(\sum_{g:\mathrm{hom}_A(y, x)} g \circ f = \mathrm{id}_A(x)\right) \times \left(\sum_{h:\mathrm{hom}_A(y, x)} f \circ h = \mathrm{id}_A(y)\right)$$

\begin{definition}
A *[[complete Segal type]]* is a Segal type which additionally is [[Rezk completion|complete]]: the canonical function which by the [[J rule]] takes an identification of elements $p:x =_A y$ to an isomorphism $J(\lambda t.\mathrm{id}_A(t), x, y, p):\mathrm{iso}_A(x, y)$ is an [[equivalence of types]] for all $x:A$ and $y:A$. 

$$\prod_{x:A} \prod_{y:A} \mathrm{isEquiv}(\lambda p.J(\lambda t.\mathrm{id}_A(t), x, y, p))$$ 
\end{definition}

The opposite $A^\op$ of a complete Segal type $A$ is also a complete Segal type; that is, the opposite modality preserves completeness.

Examples of complete Segal types include the interval $\mathbb{I}$, the $n$-cubes $\mathrm{Fin}(n) \to \mathbb{I}$, and the $n$-simplices inductively defined by 
 
$$\Delta^0 \coloneqq \mathrm{Fin}(0) \to \mathbb{I}$$

$$n:\mathbb{N} \vdash \Delta^{n + 1} \coloneqq \sum_{t:\mathrm{Fin}(n + 1) \to \mathbb{I}} \prod_{i:\mathrm{Fin}(n)} t(\pi_1(i)) \leq t(\pi_1(i + 1))$$

### Amazing covariance and directed univalent universes

A type $A$ is an **amazingly covariant type** if it satisfies the following predicate

$$\mathrm{isACov}(A) \coloneqq \mathrm{isCov}(i:\mathbb{I}.A^\eta \cdot i)^{1 / \mathbb{I}}$$

Let $(U, T)$ be a [[univalent Tarski universe]]. The [[directed univalence|directed univalent]] subuniverse $\mathcal{S} \hookrightarrow U$ is defined as the type of $U$-small amazingly covariant types:

$$\mathcal{S} \coloneqq \sum_{X:U} \mathrm{isACov}(T(X))$$

The directed univalent universe $\mathcal{S}$ is a [[finitely complete Segal type|finitely complete]] and [[finitely cocomplete Segal type|finitely cocomplete]] [[complete Segal type]]. 

## See also

* [[Reedy model structure]]

* [[bisimplicial set]]

* [[simplicial anima]]

* [[simplicial object in an (infinity,1)-category]]

* [[synthetic (infinity,1)-category theory|synthetic $(\infty,1)$-category theory]]

* [[parametric type theory]]

* [[cohesive homotopy type theory]]

* [[triangulated type theory]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Mike Shulman]], *A type theory for synthetic ∞-categories*, Higher Structures **1** 1 (2017) &lbrack;[arxiv:1705.07442](https://arxiv.org/abs/1705.07442), [published article](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/RiehlShulman)&rbrack;

* [[Jonathan Weinberger]], *A Synthetic Perspective on $(\infty,1)$-Category Theory: Fibrational and Semantic Aspects* $[$[arXiv:2202.13132](https://arxiv.org/abs/2202.13132)$]$

* Fredrik Bakke, *Segal Spaces in Homotopy Type Theory*. Master thesis $[$[no.ntnu:inspera:99217069:14871483	](https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2995704)$]$

* [[César Bardomiano Martínez]], *Limits and colimits of synthetic $\infty$-categories* $[$[arXiv:2202.12386](https://arxiv.org/abs/2202.12386)$]$

* [[Jonathan Weinberger]], *Strict stability of extension types* $[$[arXiv:2203.07194](https://arxiv.org/abs/2203.07194)$]$

* [[Jonathan Weinberger]], *Two-sided cartesian fibrations of synthetic $(\infty,1)$-categories* $[$[arXiv:2204.00938](https://arxiv.org/abs/2204.00938)$]$

* [[Jonathan Weinberger]], *Internal sums for synthetic fibered $(\infty,1)$-categories* $[$[arXiv:2205.00386](https://arxiv.org/abs/2205.00386)$]$

* [[David Jaz Myers]], [[Mitchell Riley]], *Commuting Cohesions* &lbrack;[arXiv:2301.13780](https://arxiv.org/abs/2301.13780)&rbrack;

* [[Mitchell Riley]], *A Type Theory with a Tiny Object* &lbrack;[arXiv:2403.01939](https://arxiv.org/abs/2403.01939)&rbrack;

* [[Jonathan Weinberger]], *Generalized Chevalley criteria in simplicial homotopy type theory*, [arXiv:2403.08190](https://arxiv.org/abs/2403.08190)

* {#Aberle24} [[C.B. Aberlé]], *Parametricity via Cohesion* &lbrack;[arXiv:2404.03825](https://arxiv.org/abs/2404.03825)&rbrack; 

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#GWB25} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *The Yoneda embedding in simplicial type theory* ([arXiv:2501.13229](https://arxiv.org/abs/2501.13229))

A talk on [[synthetic (infinity,1)-category theory]] in [[simplicial type theory]] and [[infinity-cosmos]] theory:

* [[Emily Riehl]], *The synthetic theory of infinity-categories vs the synthetic theory of infinity-categories*, [[Homotopy Type Theory Electronic Seminar Talks]], 1 March 2018, ([video](https://www.youtube.com/watch?v=ge-9m1SsEmc), [slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Riehl-2018-03-01-HoTTEST.pdf))

A [[proof assistant]] implementing simplicial type theory: 

* [[Rzk]] &lbrack;[github.com/fizruk/rzk](https://github.com/fizruk/rzk)&rbrack;

Formalization of the [[(infinity,1)-Yoneda lemma|$(\infty,1)$-Yoneda lemma]] via [[simplicial homotopy type theory]] (in [[Rzk]]):

* [[Nikolai Kudasov]], [[Emily Riehl]], [[Jonathan Weinberger]]. *Formalizing the $\infty$-categorical Yoneda lemma* (2023) &lbrack;[arXiv:2309.08340](https://arxiv.org/abs/2309.08340)&rbrack;


[[!redirects simplicial homotopy type theory]]

[[!redirects axiom of simplicial cohesion]]


