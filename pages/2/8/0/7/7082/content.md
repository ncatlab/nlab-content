
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
=--
=--

# Equivalences in type theory
* table of contents
{:toc}

## Idea

In [[dependent type theory]] with [[axiom K]] or [[uniqueness of identity proofs]], the notion of **equivalence** corresponds roughly to the notion of [[bijection]] or [[one-to-one correspondence]] in [[set theory]]. 

In the context of dependent type theories without [[axiom K]] or [[uniqueness of identity proofs]], such as [[homotopy type theory]], **equivalence** corresponds to the notion of [[equivalence]] in [[groupoid|groupoid theory]] and the notion of [[homotopy equivalence]] in [[homotopy theory]]. These are sometimes called **[[weak equivalences]]**, but there is nothing [[weak equivalence|weak]] about them (in particular, they always have homotopy inverses). 

## Definition

We work in [[intensional type theory|intensional]] [[type theory]] with [[dependent sums]], [[dependent products]], and [[identity types]].  

### As functions with contractible fibers

Given types $A$ and $B$, a function $f:A \to B$, and an element $b:B$, the [[fiber type]] of $f$ at $b$ is the [[dependent sum type]] 

$$\mathrm{fiber}(f,b) \coloneqq \sum_{a:A} f(a) = b$$

the [[proposition]] that a type $C$ is a [[contractible type]] is

$$\mathrm{isContr}(C) \coloneqq \sum_{a:C} \prod_{b:C} a =_C b$$

and the [[proposition]] that a function $f$ has contractible fibers 

$$\mathrm{hasContrFibers}(f) \coloneqq \prod_{b:B} \mathrm{isContr}(\mathrm{fiber}(f,b))$$

We say $f$ is an **equivalence** if it comes with an witness $p:\mathrm{hasContrFibers}(f)$; that is, a function is an equivalence if all of its [[fiber types]] are [[contractible types]].

Given two types $A$ and $B$, the **type of equivalences** from $A$ to $B$ is the [[dependent sum type]]

$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{hasContrFibers}(f)$$

### As functions with a left and a right inverse

There is also another definition of an equivalence: a function which has both a left inverse and a right inverse:

$$\mathrm{hasLeftRightInv}(f) \coloneqq \left(\sum_{g:B \to A} \prod_{b:B} f(g(b)) =_B b\right) \times \left(\sum_{h:B \to A} \prod_{a:A} a =_A h(f(a))\right)$$

### Other variations

Three variations of this definition are, informally:

* $f\colon A\to B$ is an equivalence if there is a map $g\colon B\to A$ and homotopies $p\colon \prod_{a\colon A} (g(f(a)) = a)$ and $q\colon \prod_{b\colon B} (f(g(b)) = b)$ (a **[[homotopy equivalence]]**)

* $f\colon A\to B$ is an equivalence if there is the above data, together with a higher homotopy expressing one [[triangle identity]] for $f$ and $g$ (an **[[adjoint equivalence]]**).

* $f\colon A\to B$ is an equivalence if there are maps $g,h\colon B\to A$ and homotopies $p\colon \prod_{a\colon A} (g(f(a)) = a)$ and $q\colon \prod_{b\colon B} (f(h(b)) = b)$ (sometimes called a **homotopy isomorphism**).

By formalizing these, we obtain types $homotopyEquiv(f)$, $isAdjointEquiv(f)$, and $isHIso(f)$.  All four of these types are co-inhabited: we have a function from any one of them to any of the others.  Moreover, at least if we assume [[function extensionality]], the types $isAdjointEquiv(f)$ and $isHIso(f)$ are themselves *equivalent* to $hasContrFibers(f)$, and all three are [[h-propositions]].

This is not true for $homotopyEquiv(f)$, which is not in general an h-prop even with function extensionality.  However, often the most convenient way to show that $f$ is an equivalence is by exhibiting a term in $homotopyEquiv(f)$ (although such a term could just as well be interpreted to lie in $isHIso(f)$ with $h\coloneqq g$).

### As one-to-one correspondences

Let $\mathcal{U}$ be a [[universe]] and $A:\mathcal{U}$ and $B:\mathcal{U}$ be terms of the universe, and $R :A \times B \to \mathcal{U}$ be a [[correspondence]] between $A$ and $B$. We define the property of $R$ being **one-to-one** as follows:

$$isOneToOne(R) \coloneqq \left(\prod_{a:A} \mathrm{isContr}\left(\sum_{b:B} R(a,b)\right)\right) \times \left(\prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} R(a,b)\right)\right)$$

We define the type of equivalences from $A$ to $B$ in $\mathcal{U}$ as 

$$(A \simeq_\mathcal{U} B)  \equiv \sum_{R : (A \times B) \to \mathcal{U}} isOneToOne(R)$$

By the [[type theoretic axiom of replacement]], the image of $R$ is $\mathcal{U}$-small, and thus $A \simeq_\mathcal{U} B$ is $\mathcal{U}$-small as well. 

One could also forego universes entirely and make this definition into rules of the type theory, as follows:

Formation rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Reflection rule for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash R:A \simeq B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \mathcal{T}(R)(x, y) \; \mathrm{type}}$$

Totality rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B \vdash \lambda(R)(y):\sum_{x:A} \mathcal{T}(R)(x, y)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A \vdash \rho(R)(x):\sum_{y:B} \mathcal{T}(R)(x, y)}$$

Uniqueness rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, y:B, u:\sum_{x:A} \mathcal{T}(R)(x, y) \vdash \eta_\lambda(R)(y)(u):\lambda_\tau(R)(y) =_{\sum_{x:A} \mathcal{T}(R)(x, y)} u}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, R:A \simeq B, x:A, u:\sum_{y:B} \mathcal{T}(R)(x, y) \vdash \eta_\rho(R)(x)(u):\rho_\tau(R)(x) =_{\sum_{y:B} \mathcal{T}(R)(x, y)} u}$$

This is valid so long as the dependent type theory has [[identity types]] and [[dependent sum types]]. By the [[principle of unique choice]], one could derive functions $f:A \to B$ and $g:B \to A$ given an equivalence $R:A \simeq B$, which are [[coherent inverse functions]] of each other and have [[contractible]] [[fibers]] each. 

### Rules for hasContrFibers

In any [[dependent type theory]] with [[identity types]], [[function types]], [[fiber types]], and [[isContr]] defined either through [[isProp]] or [[contraction types]], all of which could be defined without [[dependent product types]] or [[dependent sum types]], we can still define hasContrFibers by adding the formation, introduction, elimination, computation, and uniqueness rules for hasContrFibers

Formation rules for hasContrFibers types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B, y:B \vdash \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, y)) \; \mathrm{type}}{\Gamma \vdash \mathrm{hasContrFibers}_{A, B}(f) \; \mathrm{type}}$$

Introduction rules for hasContrFibers types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B, y:B \vdash b(y):\mathrm{isContr}(\mathrm{fiber}_{A, B}(f, y))}{\Gamma, f:A \to B \vdash \lambda x.b(x):\mathrm{hasContrFibers}_{A, B}(f)}$$

Elimination rules for hasContrFibers types:
$$\frac{\Gamma, f:A \to B \vdash p:\mathrm{hasContrFibers}_{A, B}(f) \quad \Gamma \vdash c:B}{\Gamma, f:A \to B \vdash p(a):\mathrm{hasContrFibers}_{A, B}(f)(c)}$$

Computation rules for hasContrFibers types:
$$\frac{\Gamma, f:A \to B, y:B \vdash b(y):\mathrm{isContr}(\mathrm{fiber}_{A, B}(f, y)) \quad \Gamma \vdash c:B}{\Gamma, f:A \to B \vdash \beta_\mathrm{hasContrFibers}:\lambda x.b(x)(c) =_{\mathrm{isContr}(\mathrm{fiber}_{A, B}(f, c))} b(c)}$$

Uniqueness rules for hasContrFibers types:
$$\frac{\Gamma, f:A \to B \vdash p:\mathrm{hasContrFibers}_{A, B}(f)}{\Gamma, f:A \to B \vdash \eta_\mathrm{hasContrFibers}:p =_{\mathrm{hasContrFibers}_{A, B}(f)} \lambda(x).p(x)}$$

### Rules for equivalence types

We work in a [[dependent type theory]] with [[identity types]], [[function types]], and some set of rules for isEquiv defined above which does not require [[dependent product types]] or [[dependent sum types]]. The type of equivalences $A \simeq B$ is given by the following rules:

Formation rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B \vdash \mathrm{isEquiv}(f) \; \mathrm{type}}{\Gamma \vdash A \simeq B \; \mathrm{type}}$$

Introduction rules for equivalence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B \vdash p(f):\mathrm{isEquiv}(f) \quad \Gamma \vdash g:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}[g/f]}{\Gamma \vdash (g, p):A \simeq B}$$

Elimination rules for equivalence types:
$$\frac{\Gamma \vdash h:A \simeq B}{\Gamma \vdash \pi_1(h):A \to B} \qquad \frac{\Gamma \vdash h:A \simeq B}{\Gamma \vdash \pi_2(h):\mathrm{isEquiv}(\pi_1(h))}$$

Computation rules for equivalence types:
$$\frac{\Gamma, f:A \to B \vdash p(f):\mathrm{isEquiv}(f) \quad \Gamma \vdash g:A \to B}{\Gamma \vdash \beta_{\simeq 1}:\pi_1(g, p) =_{A \to B} g} \qquad \frac{\Gamma, f:A \to B \vdash p:\mathrm{isEquiv} \quad \Gamma \vdash g:A \to B}{\Gamma \vdash \beta_{\simeq 2}:\pi_2(g, p) =_{\mathrm{isEquiv}(\pi_1(g, p))} p}$$

Uniqueness rules for equivalence types:
$$\frac{\Gamma \vdash h:A \simeq B}{\Gamma \vdash \eta_\simeq:h =_{A \simeq B} (\pi_1(h), \pi_2(h))}$$

### Coinductive definition

Given two types $A$ and $B$ and two functions $f:A \to B$ and $g:B \to A$, $f$ and $g$ are inverses of each other if for every element $a:A$ and $b:A$, there is an equivalence of types between $f(a) =_B b$ and $a =_A g(b)$:

$$\mathrm{isInv}(f, g) \coloneqq \prod_{a:A} \prod_{b:B} (f(a) =_B b) \simeq (a =_A g(b))$$

This leads to a coinductive definition of the type of equivalences

$$A \simeq B \coloneqq \sum_{f:A \to B} \sum_{g:B \to A} \prod_{a:A} \prod_{b:B} (f(a) =_B b) \simeq (a =_A g(b))$$

### Strict equivalences

There is also a notion of **strict equivalence** between two types $A$ and $B$, where given functions $f:A \to B$ and $g:B \to A$ instead of having identity types between $g(f(a)) =_A a$ and similarly $b =_B f(g(b))$ making the pair of functions into [[quasi-inverse functions]], there are [[judgmental equalities]] $g(f(a)) \equiv a:A$ and $b \equiv f(g(b)):B$ or [[propositional equalities]] $g(f(a)) \equiv_A a \; \mathrm{true}$ and $b \equiv_B f(g(b)) \; \mathrm{true}$, making them into **judgmentally strict equivalences** and **propositionally strict equivalences** respectively. 

Judgmentally strict equivalences are used in defining [[Shulman univalent universes]] in [[higher observational type theory]]. 

## Properties

### Constructing the inverse function. 

For every equivalence, there is a function $g:B \to A$ which is an [[inverse function]]. 

The [[principle of unique choice]] implies that given a function $f:A \to B$, if for all $b:B$ the fiber of $f$ at $b$ is contractible, then for all $b:B$ there is an element $g(b):\mathrm{fiber}(f, b)$. 

$$\prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} f(a) =_A b\right) \to \prod_{b:B} \sum_{a:A} f(a) =_A b$$

The [[type theoretic axiom of choice]] then states that for all elements $b:B$ one has the structure of an element $a:A$ such that $f(a) =_A b$, then one has a function $g:B \to A$ such that $f(g(b)) =_A b$. 

$$\prod_{b:B} \sum_{a:A} f(a) =_A b \to \sum_{g:B \to A} \prod_{b:B} f(g(b)) =_A b$$

There is also another definition of contractible type, which uses the notion of [[center of contraction]]; namely, that a type $A$ is a contractible type if it comes with a element $a:A$ and a witness that for all elements $b:A$, $a =_A b$

$$\prod_{b:A} a =_A b$$

Since the fiber of $f$ at $b$ is contractible, $g(b)$ is the [[center of contraction]] for the fiber of $f$ at $b$. 

Thus, for all elements $a:A$ and $b:B$ and a witness $q(a, b):f(a) =_B b$, there is a witness $r(a, b, q(a, b)):a =_A g(b)$. Since the type $a =_A g(b)$ doesn't depend on $q(a, b)$, by the rules of [[function types]], the latter condition is the same as for all elements $a:A$ and $b:B$, a function $r(a, b):f(a) =_B b \to a =_A g(b)$. 

...

still to prove: that the function above is an equivalence of types for all $a:A$ and $b:B$. 

## Semantics
 {#Semantics}

We discuss the [[categorical semantics]] of equivalences in homotopy type theory.

Let $\mathcal{C}$ be a [[locally cartesian closed category]] which is a [[model category]], in which the (acyclic cofibration, fibration) [[weak factorization system]] has [[stable path objects]], and acyclic cofibrations are preserved by pullback along fibrations between fibrant objects.  (We ignore questions of coherence, which are not important for this discussion.) For instance $\mathcal{C}$ could be a [[type-theoretic model category]].

### Of $hasContrFibers(-)$

+-- {: .num_prop }
###### Proposition

For $A, B$ two [[cofibrant object|cofibrant]]-[[fibrant objects]] in $\mathcal{C}$,
a morphism $f\colon A\to B$ is a [[weak equivalence]] or equivalently a [[homotopy equivalence]] in $\mathcal{C}$ precisely when the interpretation of $hasContrFibers(f)$ has a [[generalized element|global point]] $* \to hasContrFibers(f)$.

=--

+-- {: .proof}
###### Proof

For $f\colon A\to B$, the [[categorical semantics]] of the [[dependent type]]

$$
  b\colon B 
   \;\vdash\; 
  hfiber(f,b)\colon Type
$$ 

is by the rules for the [[categorical semantics|interpretation]] of [[identity types]] and [[substitution]]
the [[mapping path space]] construction $P f$, given by the [[pullback]]

$$
  \array{
    [b : B \vdash  hfiber(f,b)] &\coloneqq & P f  &\to& A
    \\
    && \downarrow && \downarrow^{\mathrlap{f}}
    \\
    && B^I &\to& B
    \\
    && \downarrow
    \\
    && B
  }
$$

which, by the [[factorization lemma]], is one way to factor $f$ as an [[acyclic cofibration]] followed by a [[fibration]]

$$
  f : A \stackrel{\simeq}{\to} P f \to B
  \,.
$$

By definition and the semantics of [[contractible types]], therefore, if $A$ and $B$ are cofibrant, then $isEquiv(f)$ has a [[global element]] 

$$
  * \to \prod_{b} isContr(hfiber(f,b))
$$


precisely when in this factorization, the fibration $P f \to B$ is an acyclic fibration.  (See for instance ([Shulman, page 49](http://www.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=49)) for more details.)


But by the [[2-out-of-3 property]], this is equivalent to $f$ being a weak equivalence --- and hence a homotopy equivalence, since it is a map between fibrant-cofibrant objects.


=--

+-- {: .num_remark #InterpretationIfIsEquivAsDependentType}
###### Remark

In the above we fixed one function $f : A \to X$. But the type $hasContrFibers$ is actually a [[dependent type]]

$$
  f : A \to B \vdash hasContrFibers(f)
$$

on the [[function type|type of all functions]]. To obtain the [[categorical semantics]] of this general dependent $hasContrFibers$-construction, first notice that the interpretation of

$f : A \to B,\; a : A,\; b : B \;\vdash\; (f(a) = b)  \colon Type$

is by the rules for interpretation of [[identity types]], [[evaluation]] and [[substitution]] the left vertical morphism in the [[pullback]] [[diagram]]

$$
  \array{  
    Q &\to&  B^I
    \\
    \downarrow && \downarrow
    \\
    [A,B] \times A \times B &\stackrel{(eval, id_B)}{\to}& B \times B
  }
  \,,
$$

where $eval : [A, B] \times A \to B$ is the [[evaluation map]] for the [[internal hom]].
This means that the interpretation of further [[dependent sum]] yielding $hfib$

$$
  f : A \to B,\; b : B 
   \; \vdash \;  
  \left(
    \sum_{a : A } (f(a) = b) 
  \right)
  \colon Type
$$

is the composite left vertical morphism in

$$
  \array{  
    Q &\to& B^I
    \\
    \downarrow && \downarrow
    \\
    [A,B] \times A \times B &\stackrel{(eval, id_B)}{\to}& B \times B
    \\
    \downarrow^{\mathrlap{p_{1,3}}}
    \\
    [A,B] \times B
  }
$$

=--

### Of $Equiv(-)$


(...)


## Related concepts

* **isEquiv**

* [[isContr]]

* [[isProp]]

* [[homotopy equivalence]]

  * [[weak homotopy equivalence]]

  * [[stable weak homotopy equivalence]]

## References

An introduction to equivalence in homotopy type theory is in 

* [[Andrej Bauer]], _A seminar on HoTT equivalences_ ([blog post](http://homotopytypetheory.org/2011/12/07/a-seminar-on-hott-equivalences/))

and basic ideas are also indicated from [slide 60 of part 2](https://home.sandiego.edu/~shulman/hottminicourse2012/02hott.pdf#page=60), [slide 49 of part 3](https://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=49) of 

* [[Mike Shulman]], _Minicourse in homotopy type theory_ (2012) ([web](https://home.sandiego.edu/~shulman/hottminicourse2012/))
 {#Shulman}

[[Coq]] code for homotopy equivalences is at

* [HoTT repository](https://github.com/HoTT/HoTT/blob/master/theories/Basics/Equivalences.v)

For equivalences as one-to-one correspondences in homotopy type theory, see

* Mike Shulman, Towards a Third-Generation HOTT Part 1 ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))


[[!redirects type of equivalences]]
[[!redirects types of equivalences]]
[[!redirects equivalence of types]]
[[!redirects equivalences of types]]

[[!redirects strict equivalence]]
[[!redirects strict equivalences]]

[[!redirects judgmentally strict equivalence]]
[[!redirects judgmentally strict equivalences]]

[[!redirects propositionally strict equivalence]]
[[!redirects propositionally strict equivalences]]

[[!redirects isEquiv]]

[[!redirects equivalence in homotopy type theory]]
[[!redirects equivalences in homotopy type theory]]
[[!redirects equivalence in type theory]]
[[!redirects equivalences in type theory]]
[[!redirects equivalence in HoTT]]
[[!redirects equivalences in HoTT]]

[[!redirects adjoint equivalence in homotopy type theory]]
[[!redirects adjoint equivalences in homotopy type theory]]
[[!redirects adjoint equivalence in type theory]]
[[!redirects adjoint equivalences in type theory]]
[[!redirects adjoint equivalence in HoTT]]
[[!redirects adjoint equivalences in HoTT]]

[[!redirects weak equivalence in homotopy type theory]]
[[!redirects weak equivalences in homotopy type theory]]
[[!redirects weak equivalence in type theory]]
[[!redirects weak equivalences in type theory]]
[[!redirects weak equivalence in HoTT]]
[[!redirects weak equivalences in HoTT]]

[[!redirects strict equivalence in homotopy type theory]]
[[!redirects strict equivalences in homotopy type theory]]
[[!redirects strict equivalence in type theory]]
[[!redirects strict equivalences in type theory]]
[[!redirects strict equivalence in HoTT]]
[[!redirects strict equivalences in HoTT]]

[[!redirects judgmentally strict equivalence in homotopy type theory]]
[[!redirects judgmentally strict equivalences in homotopy type theory]]
[[!redirects judgmentally strict equivalence in type theory]]
[[!redirects judgmentally strict equivalences in type theory]]
[[!redirects judgmentally strict equivalence in HoTT]]
[[!redirects judgmentally strict equivalences in HoTT]]

[[!redirects propositionally strict equivalence in homotopy type theory]]
[[!redirects propositionally strict equivalences in homotopy type theory]]
[[!redirects propositionally strict equivalence in type theory]]
[[!redirects propositionally strict equivalences in type theory]]
[[!redirects propositionally strict equivalence in HoTT]]
[[!redirects propositionally strict equivalences in HoTT]]

[[!redirects homotopy isomorphism]]
[[!redirects h-isomorphism]]