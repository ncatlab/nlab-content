
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

In [[homotopy type theory]], the notion of **equivalence** is an internalization of the notion of [[equivalence]] or [[homotopy equivalence]].

These are sometimes called **[[weak equivalences]]**, but there is nothing [[weak equivalence|weak]] about them (in particular, they always have homotopy inverses). 


## Definition

We work in [[intensional type theory|intensional]] [[type theory]] with [[dependent sums]], [[dependent products]], and [[identity types]].  

+-- {: .num_defn}
###### Definition

For $f\colon A\to B$ a [[term]] of [[function type]]; we define new [[dependent types]] as follows:

the [[homotopy fiber type]]

$$
  f \colon A \to B, b\colon B \vdash hfiber(f,b) \coloneqq \sum_{a\colon A} (f(a) = b)
$$

and the [[proposition]] that the homotopy fiber type is a (dependently) [[contractible type]]:

$$
  f \colon A \to B 
   \vdash 
   isEquiv(f) \coloneqq \prod_{b\colon B} isContr(hfiber(f,b))
  \,.
$$

We say $f$ is an **equivalence** if $isEquiv(f)$ is an [[inhabited type]].

=--

That is, a function is an equivalence if all of its [[homotopy fiber types]] are [[contractible types]] (in a way which depends continuously on the base point).

+-- {: .num_defn}
###### Definition

For $X, Y : Type$ two [[types]], the **type of equivalences** from $X$ to $Y$ is the [[dependent sum]]

$$
  Equiv(X,Y)
  =
  (X \stackrel{\simeq}{\to}Y)
  \coloneqq
  \sum_{f : (X \to Y)}
  isEquiv(f)
  \,.
$$

=--


Three variations of this definition are, informally:

* $f\colon A\to B$ is an equivalence if there is a map $g\colon B\to A$ and homotopies $p\colon \prod_{a\colon A} (g(f(a)) = a)$ and $q\colon \prod_{b\colon B} (f(g(b)) = b)$ (a **[[homotopy equivalence]]**)

* $f\colon A\to B$ is an equivalence if there is the above data, together with a higher homotopy expressing one [[triangle identity]] for $f$ and $g$ (an **[[adjoint equivalence]]**).

* $f\colon A\to B$ is an equivalence if there are maps $g,h\colon B\to A$ and homotopies $p\colon \prod_{a\colon A} (g(f(a)) = a)$ and $q\colon \prod_{b\colon B} (f(h(b)) = b)$ (sometimes called a **homotopy isomorphism**).

By formalizing these, we obtain types $homotopyEquiv(f)$, $isAdjointEquiv(f)$, and $isHIso(f)$.  All four of these types are co-inhabited: we have a function from any one of them to any of the others.  Moreover, at least if we assume [[function extensionality]], the types $isAdjointEquiv(f)$ and $isHIso(f)$ are themselves *equivalent* to $isEquiv(f)$, and all three are [[h-propositions]].

This is not true for $homotopyEquiv(f)$, which is not in general an h-prop even with function extensionality.  However, often the most convenient way to show that $f$ is an equivalence is by exhibiting a term in $homotopyEquiv(f)$ (although such a term could just as well be interpreted to lie in $isHIso(f)$ with $h\coloneqq g$).

### As one-to-one correspondences ###
Let $\mathcal{U}$ be a [[universe]] and $A:\mathcal{U}$ and $B:\mathcal{U}$ be terms of the universe, and $R :A \times B \to \mathcal{U}$ be a [[correspondence]] between $A$ and $B$. We define the property of $R$ being **one-to-one** as follows:

$$isOneToOne(R) \coloneqq \left(\prod_{a:A} \mathrm{isContr}\left(\sum_{b:B} R(a,b)\right)\right) \times \left(\prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} R(a,b)\right)\right)$$

We define the type of equivalences from $A$ to $B$ in $\mathcal{U}$ as 

$$(A \simeq_\mathcal{U} B)  \equiv \sum_{R : (A \times B) \to \mathcal{U}} isOneToOne(R)$$

### Rules for isEquiv

In any [[dependent type theory]] with [[identity types]], [[function types]], [[fiber types]], and [[isContr]] defined either through [[isProp]] or [[contraction types]], all of which could be defined without [[dependent product types]] or [[dependent sum types]], we can still define isEquiv by adding the formation, introduction, elimination, computation, and uniqueness rules for isEquiv

Formation rules for isEquiv types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B, y:B \vdash \mathrm{isContr}(\mathrm{fiber}_{A, B}(f, y)) \; \mathrm{type}}{\Gamma \vdash \mathrm{isEquiv}_{A, B}(f) \; \mathrm{type}}$$

Introduction rules for isEquiv types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B, y:B \vdash b(y):\mathrm{isContr}(\mathrm{fiber}_{A, B}(f, y))}{\Gamma, f:A \to B \vdash \lambda x.b(x):\mathrm{isEquiv}_{A, B}(f)}$$

Elimination rules for isEquiv types:
$$\frac{\Gamma, f:A \to B \vdash p:\mathrm{isEquiv}_{A, B}(f) \quad \Gamma \vdash c:B}{\Gamma, f:A \to B \vdash p(a):\mathrm{isEquiv}_{A, B}(f)(c)}$$

Computation rules for isEquiv types:
$$\frac{\Gamma, f:A \to B, y:B \vdash b(y):\mathrm{isContr}(\mathrm{fiber}_{A, B}(f, y)) \quad \Gamma \vdash c:B}{\Gamma, f:A \to B \vdash \beta_\mathrm{isEquiv}:\lambda x.b(x)(c) =_{\mathrm{isContr}(\mathrm{fiber}_{A, B}(f, c))} b(c)}$$

Uniqueness rules for isEquiv types:
$$\frac{\Gamma, f:A \to B \vdash p:\mathrm{isEquiv}_{A, B}(f)}{\Gamma, f:A \to B \vdash \eta_\mathrm{isEquiv}:p =_{\mathrm{isEquiv}_{A, B}(f)} \lambda(x).p(x)}$$

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

## Semantics
 {#Semantics}

We discuss the [[categorical semantics]] of equivalences in homotopy type theory.

Let $\mathcal{C}$ be a [[locally cartesian closed category]] which is a [[model category]], in which the (acyclic cofibration, fibration) [[weak factorization system]] has [[stable path objects]], and acyclic cofibrations are preserved by pullback along fibrations between fibrant objects.  (We ignore questions of coherence, which are not important for this discussion.) For instance $\mathcal{C}$ could be a [[type-theoretic model category]].

### Of $isEquiv(-)$

+-- {: .num_prop }
###### Proposition

For $A, B$ two [[cofibrant object|cofibrant]]-[[fibrant objects]] in $\mathcal{C}$,
a morphism $f\colon A\to B$ is a [[weak equivalence]] or equivalently a [[homotopy equivalence]] in $\mathcal{C}$ precisely when the interpretation of $isEquiv(f)$ has a [[generalized element|global point]] $* \to isEquiv(f)$.

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

In the above we fixed one function $f : A \to X$. But the type $isEquiv$ is actually a [[dependent type]]

$$
  f : A \to B \vdash isEquiv(f)
$$

on the [[function type|type of all functions]]. To obtain the [[categorical semantics]] of this general dependent $isEquiv$-construction, first notice that the interpretation of

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

[[!redirects homotopy isomorphism]]
[[!redirects h-isomorphism]]