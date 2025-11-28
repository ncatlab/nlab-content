
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

### Bridge types of arbitrary arity
  {#OfArbitraryArity}

More generally, one can consider **bridge types of [[arbitrary arity]]**. For an index type $I$, bridge types of [[arity]] $I$ are parameterized by an $I$-indexed family of elements of $A$; that is, 

$$\overline{x}:I \to A \vdash \mathrm{Br}_{I, A}(\overline{x}) \; \mathrm{type}$$

The $n$-ary bridge types are simply the case where the index type $I$ is the standard [[finite type]] with $n$ elements $\mathrm{Fin}(n) \coloneqq \sum_{m:\mathbb{N}} m \lt n$, due to the [[induction principle]] of the [[natural numbers type]]. 

## Properties

### Reflexivity

Bridge types are *reflexive* in that for all elements $x:A$, there is an element 

$$\mathrm{refl}_{I, A}(x):\mathrm{Br}_{I, A}(\lambda t.x)$$

where $\lambda t.x:I \to A$ is the [[constant function]] which always returns $x$. 

For $I \equiv \mathrm{bool}$ the [[type of booleans]], this yields the usual notion of reflexivity for binary bridge types $\mathrm{Br}_A(x, y)$, since by the [[induction principle]] of the [[type of booleans]], $\mathrm{Br}_{A, \mathrm{bool}}(\mathrm{rec}_{\mathrm{bool}, A}(x, y))$ is [[equivalence of types|equivalent]] to $\mathrm{Br}_A(x, y)$ and $\mathrm{rec}_{\mathrm{bool}, A}(x, x) \equiv \lambda t.x$. 

### Function application

In the same way that functions preserve [[identifications]] via [[function application to identifications]], functions preserve bridges via **function application to bridges** or the **action on bridges**. For all functions $\overline{x}:I \to A$ and $f:A \to B$, and bridges $p:\mathrm{Br}_{I, A}(\overline{x})$, there is a bridge $\mathrm{ap}(f, \overline{x}, p):\mathrm{Br}_{I, A}(f \circ \overline{x})$:

$$f:A \to B, \overline{x}:I \to A, p:\mathrm{Br}_{I, A}(\overline{x}) \vdash \mathrm{ap}(f, \overline{x}, p):\mathrm{Br}_{I, A}(f \circ \overline{x})$$

For $I \equiv \mathrm{bool}$ the [[type of booleans]] and $\overline{x} \equiv \mathrm{rec}_{\mathrm{bool}, A}(x, y)$, this yields the usual notion of the action on bridges on binary bridge types $\mathrm{Br}_A(x, y)$, since by the [[induction principle]] of the [[type of booleans]], $\mathrm{Br}_{A, \mathrm{bool}}(\mathrm{rec}_{\mathrm{bool}, A}(x, y))$ is [[equivalence of types|equivalent]] to $\mathrm{Br}_A(x, y)$. 

Function application to bridges satisfy many of the same [[judgmental equalities]] as function application to identifications. These include, for $f:A \to B$, $g:B \to C$, $\overline{x}:I \to A$, and $p:\mathrm{Br}_{I, A}(\overline{x})$,

$$\mathrm{ap}(\lambda x.x, \overline{x}, p) \equiv p:\mathrm{Br}_{I, A}(\overline{x})$$

$$\mathrm{ap}(\lambda t.x, \overline{x}, p) \equiv \mathrm{refl}_{I, A}(x):\mathrm{Br}_{I, A}(\overline{x})$$

$$\mathrm{ap}(g \circ f, \overline{x}, p) \equiv \mathrm{ap}(g, f \circ \overline{x}, \mathrm{ap}(f, \overline{x}, p)):\mathrm{Br}_{I, C}(g \circ f \circ \overline{x})$$

$$\mathrm{ap}(f, \lambda t.x, \mathrm{refl}_{I, A}(x)) \equiv \mathrm{refl}_{I, B}(f(x)):\mathrm{Br}_{I, B}(\lambda t.f(x))$$

## Heterogeneous bridge types

Similarly to [[heterogeneous identity types]], there are heterogeneous versions of bridge types as well. Given a type $A$ and a type family $(B(x))_{x:A}$ and an index type $I$ for the bridge types, the heterogeneous bridge type is a type family 

$$\overline{x}:I \to A, p:\mathrm{Br}_{I, A}(\overline{x}), \overline{y}:\prod_{i:I} B(\overline{x}(i)) \vdash \mathrm{hBr}_{I, A, B}(\overline{x}, p, \overline{y})$$

The usual version of a bridge type can be called **homogeneous** to contrast with heterogeneous bridge types. 

For $I \equiv \mathrm{bool}$ the [[type of booleans]], $\overline{x} \equiv \mathrm{rec}_{\mathrm{bool}, A}(x_0, x_1)$, and $\overline{y} \equiv \mathrm{ind}_{\mathrm{bool}, \lambda t.B(\overline{x}(t))}(y_0, y_1)$, this yields the usual notion of a heterogeneous bridge types $\mathrm{hBr}_{A, B}(x_0, x_1, p, y_0, y_1)$, since by the [[induction principle]] of the [[type of booleans]], we have an [[equivalence of types]] 

$$\mathrm{hBr}_{\mathrm{bool}, A, B}(\mathrm{rec}_{\mathrm{bool}, A}(x_0, x_1), p, \mathrm{ind}_{\mathrm{bool}, B}(y_0, y_1)) \simeq \mathrm{hBr}_{A, B}(x_0, x_1, p, y_0, y_1)$$

Like [[heterogeneous identity types]], there is also a version of the heterogeneous bridge type which can be defined as a [[dependent sum type]]

$$\overline{x}:I \to A, \overline{y}:\prod_{i:I} B(\overline{x}(i)) \vdash \mathrm{hBr}_{I, A, B}(\overline{x}, \overline{y}) \coloneqq \sum_{p:\mathrm{Br}_{I, A}(\overline{x})} \mathrm{hBr}_{I, A, B}(\overline{x}, p, \overline{y})$$

These heterogeneous bridge types can be called **fibered heterogeneous bridge types**, and the other kind can be called **indexed heterogeneous bridge types**, in parallel to [[heterogeneous identity types]]. 

### Relation to homogeneous bridge types

Let $C$ be a type. Then heterogeneous bridge types over the constant type family at $C$ are the same as homogeneous bridge types of $C$. 

$$\mathrm{hBr}_{A, \lambda t.C, I}(\overline{x}, p, \overline{y}) \equiv \mathrm{Br}_{I, C}(\overline{y})$$

Similarly, given an element $x:A$, heterogeneous bridge types over the constant function $\lambda t.x:I \to A$ and reflexivity $\mathrm{refl}_{I, A}(x)$ are the same as homogeneous bridge types of $B(x)$:

$$\mathrm{hBr}_{I, A, B}(\lambda t.x, \mathrm{refl}_{I, A}(x), \overline{y}) \equiv \mathrm{Br}_{I, B(x)}(\overline{y})$$

### Heterogeneous reflexivity

Given an element $x:A$ and $y:B(x)$, there is an element of the heterogeneous bridge type 

$$\mathrm{hrefl}_{I, A, B}(x, y):\mathrm{hBr}_{I, A, B}(\lambda t.x, \mathrm{refl}_{I, A}(x), \lambda t.y)$$

Since the heterogeneous bridge type $\mathrm{hBr}_{I, A, B}(\lambda t.x, \mathrm{refl}_{I, A}(x), \lambda t.y)$ is the same as the homogeneous bridge type $\mathrm{Br}_{I, B(x)}(\lambda t.y)$, heterogeneous reflexivity is the same as the homogeneous reflexivity term 
$$\mathrm{hrefl}_{I, A, B}(x, y) \equiv \mathrm{refl}_{I, B(x)}(y):\mathrm{Br}_{I, B(x)}(\lambda t.y)$$

### Dependent function application

In the same way that dependent functions preserve [[heterogeneous identifications]] via dependent function application to identifications, dependent functions preserve bridges via **dependent function application to bridges** or the **dependent action on bridges**. For all functions $\overline{x}:I \to A$ and dependent functions $f:\prod_{x:A} B(x)$, and bridges $p:\mathrm{Br}_{I, A}(\overline{x})$, there is a heterogeneous bridge $\mathrm{apd}(f, \overline{x}, p):\mathrm{hBr}_{I, A, B}(\overline{x}, p, \lambda t.f(\overline{x}(t)))$:

$$f:\prod_{x:A} B(x), \overline{x}:I \to A, p:\mathrm{Br}_{I, A}(\overline{x}) \vdash \mathrm{apd}(f, \overline{x}, p):\mathrm{hBr}_{I, A, B}(\overline{x}, p, \lambda t.f(\overline{x}(t)))$$

Dependent function application of bridges satisfies some of the same judgmental equalities as that of identifications. These include, for $f:\prod_{x:A} B(x)$ and $x:A$,

$$\mathrm{apd}(f, \lambda t.x, \mathrm{refl}_{I, A}(x)) \equiv \mathrm{refl}_{I, B(x)}(f(x)):\mathrm{hBr}_{I, A, B}(\lambda t.x, \mathrm{refl}_{I, A}(x), \lambda t.f(x))$$

## The walking bridge

Given a bridge type $\mathrm{Br}_{I, A}(\overline{x})$ indexed by functions $\overline{x}:I \to A$, the *walking bridge type* is a [[higher inductive type]] $\mathbb{I}_I$ generated by a function $\mathrm{pts}:I \to \mathbb{I}_I$ and a bridge $\mathrm{br}:\mathrm{Br}_{I, \mathbb{I}_I}(\mathrm{pts})$. 

The idea of the walking bridge is that every bridge in a bridge type $\mathrm{Br}_{I, A}(\overline{x})$ is given by a function $I \to A$ that factors through $\mathbb{I}_I$: 

$$I \to \mathbb{I}_I \to A$$

in the same way that [[identifications]] are given by a function $\mathrm{bool} \to A$ that factors through the [[interval type]] (the [[walking identification]]). 

### Inference rules

The [[inference rules]] of the walking bridge are as follows:

Formation rules for the walking bridge:
$$\frac{\Gamma \vdash I \; \mathrm{type}}{\Gamma \vdash \mathbb{I}_I \; \mathrm{type}}$$

Introduction rules for the walking bridge:
$$\frac{\Gamma \vdash I \; \mathrm{type}}{\Gamma \vdash \mathrm{pts}:I \to \mathbb{I}_I} \qquad \frac{\Gamma \vdash I \; \mathrm{type}}{\Gamma \vdash \mathrm{br}_I:\mathrm{Br}_{I, \mathbb{I}_I}(\mathrm{pts})}$$

Elimination rules for the walking bridge:
$$\frac{\Gamma \vdash I \; \mathrm{type} \quad \Gamma, x:\mathbb{I}_I \vdash C(x) \; \mathrm{type} \quad \Gamma\vdash c_\mathrm{pts}:\prod_{i:I} C(\mathrm{pts}(i)) \quad \Gamma \vdash c_\mathrm{br}:\mathrm{hBr}_{I, \mathbb{I}_I, C}(\mathrm{pts}, \mathrm{br}_I, c_\mathrm{pts})}{\Gamma, x:\mathbb{I}_I \vdash \mathrm{ind}_{\mathbb{I}_I}^C(c_\mathrm{pts}, c_\mathrm{br}, x):C(x)}$$

Computation rules for the walking bridge:
$$\frac{\Gamma \vdash I \; \mathrm{type} \quad \Gamma, x:\mathbb{I}_I \vdash C(x) \; \mathrm{type} \quad \Gamma\vdash c_\mathrm{pts}:\prod_{i:I} C(\mathrm{pts}(i)) \quad \Gamma \vdash c_\mathrm{br}:\mathrm{hBr}_{I, \mathbb{I}_I, C}(\mathrm{pts}, \mathrm{br}_I, c_\mathrm{pts})}{\Gamma, i:I \vdash \mathrm{ind}_\mathbb{I}^{C}(c_\mathrm{pts}, c_\mathrm{br}, i) \equiv c(i):C(\mathrm{pts}(i))}$$

$$\frac{\Gamma \vdash I \; \mathrm{type} \quad \Gamma, x:\mathbb{I}_I \vdash C(x) \; \mathrm{type} \quad \Gamma\vdash c_\mathrm{pts}:\prod_{i:I} C(\mathrm{pts}(i)) \quad \Gamma \vdash c_\mathrm{br}:\mathrm{hBr}_{I, \mathbb{I}_I, C}(\mathrm{pts}, \mathrm{br}_I, c_\mathrm{pts})}{\Gamma \vdash \mathrm{apd}(\mathrm{ind}_\mathbb{I}^{C}(c_\mathrm{pts}, c_\mathrm{br}), \mathrm{pts}, \mathrm{br}_I) \equiv c_\mathrm{br}:\mathrm{Br}_{I, \mathbb{I}_I}(\mathrm{pts})}$$

## Discrete types

Since bridge types are reflexive, we can define the [[diagonal]] as the [[function]]

$$\Delta_{I, A} \coloneqq \lambda x.(\lambda t.x, \mathrm{refl}_{I, A}(x)):A \to \sum_{\overline{x}:I \to A} \mathrm{Br}_{I, A}(\overline{x})$$

Let $\mathrm{Id}_{I, A}(\overline{x})$, indexed by functions $\overline{x}:I \to A$, denote the [[identity type#OfArbitraryArity|identity type]] of [[arity]] $I$. Binary identity types are equivalent to the usual [[identity type]] $\mathrm{Id}_A(x, y)$ by the [[recursion principle]] of the [[type of booleans]]. 

A type $A$ is **[[discrete]]** [[if and only if]] one of the following equivalent conditions holds:

* the diagonal $\Delta_{I, A}$ is an [[equivalence of types]].

* the canonical function $\mathrm{const}_{A, \mathbb{I}_I} \coloneqq \lambda a.\lambda i.a$ which takes elements in $A$ to constant functions $\mathbb{I}_I \to A$ out of the walking bridge is an [[equivalence of types]]. 

* the canonical inductively defined family of functions $\mathrm{Id}_{I, A}(\overline{x}) \to \mathrm{Br}_{I, A}(\overline{x})$ defined via [[identification elimination]] is an [[equivalence of types]] for all $\overline{x}:I \to A$. 

The second condition is essentially saying that the [[localization of a type|localization]] $L_{\mathbb{I}_I}(A)$ at the walking bridge $\mathbb{I}_I$ is equivalent to $A$ itself.

In a [[spatial type theory]] with a [[flat modality]] and [[sharp modality]], one can create a [[cohesive type theory]] by adding an [[axiom of cohesion]] for the walking bridge, that says that a type is discrete in the spatial sense $A \simeq \flat A$ if and only if a type is discrete in the bridge sense. The [[shape modality]] of the cohesive type theory $\esh \coloneqq L_{\mathbb{I}_I}$ is then given by localization at the walking bridge. 

The semantics of such a [[cohesive type theory]] for a finite type $I$ with $n$-elements is the [[cohesive (infinity,1)-topos]] of $n$-ary [[cubical objects]] in a base [[(infinity,1)-topos]] of cubically discrete objects. 

## Relativity

There is an analogue of the [[univalence axiom]] for [[type universes]] called **relativity** (see [Cavallo & Harper 2021](#CH21)), which uses bridge types instead of [[identity types]] and types of $n$-ary [[type families]] instead of [[types of equivalences]]. A universe is called **relativistic** if it satisfies the **axiom of relativity**:

\begin{definition}
Given an index type $I$ and bridge types $\mathrm{Br}_{I, A}(\overline{x})$, **relativity** for a [[type universe]] $U$ states that for all $I$-indexed type families $\overline{X}:I \to U$, there is an equivalence of types between the bridge type $\mathrm{Br}_{I, U}(\overline{X})$ and the type $\left(\prod_{i:I} \overline{X}(i)\right) \to U$ of $U$-small $I$-ary type families. 
\end{definition}

Special cases of relativity for when the index type $I \equiv \mathrm{Fin}(n)$ is the finite type with $n = 0$, $n = 1$, and $n = 2$ elements respectively:

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

A blog post from the [[Topos Institute]] on [[bridge types]] for the theory of version control: 

* [[David Jaz Myers]], *Structure-aware version control via observational bridge types*, [[Topos Institute]], 13 November 2024 ([web](https://topos.institute/blog/2024-11-13-structure-aware-version-control-via-observational-bridge-types/))

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

[[!redirects bridge type of arbitrary ariry]]
[[!redirects bridge types of arbitrary ariry]]

[[!redirects heterogeneous bridge]]
[[!redirects heterogeneous bridges]]

[[!redirects heterogeneous bridge type]]
[[!redirects heterogeneous bridge types]]

[[!redirects indexed heterogeneous bridge]]
[[!redirects indexed heterogeneous bridges]]

[[!redirects indexed heterogeneous bridge type]]
[[!redirects indexed heterogeneous bridge types]]

[[!redirects fibered heterogeneous bridge]]
[[!redirects fibered heterogeneous bridges]]

[[!redirects fibered heterogeneous bridge type]]
[[!redirects fibered heterogeneous bridge types]]

[[!redirects fibred heterogeneous bridge]]
[[!redirects fibred heterogeneous bridges]]

[[!redirects fibred heterogeneous bridge type]]
[[!redirects fibred heterogeneous bridge types]]

[[!redirects homogeneous bridge]]
[[!redirects homogeneous bridges]]

[[!redirects homogeneous bridge type]]
[[!redirects homogeneous bridge types]]

[[!redirects walking bridge]]
[[!redirects walking bridges]]

[[!redirects walking bridge type]]
[[!redirects walking bridge types]]

[[!redirects relativity axiom]]
[[!redirects axiom of relativity]]
