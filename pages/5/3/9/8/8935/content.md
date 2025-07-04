+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

> This entry is about the axiom K in [[type theory]]. For axiom K of [[modal logic]], see *[[axiom K (modal logic)]].

# Contents
* table of contents
{: toc}

## Idea 

In [[type theory]], the _axiom K_ is an [[axiom]] that when added to [[intensional type theory]] turns it into [[set-level type theory]]. In the language of [[homotopy type theory]], this means that all types are [[h-sets]]. Accordingly, axiom K is incompatible with the [[univalence axiom]].

Heuristically, the axiom asserts that each [[term]] of each [[identity type]] $Id_A(x,x)$ (of [[equivalences]] of a [[term]] $x \colon A$) is [[propositional equality|propositionally equal]] to the canonical [[reflexive relation|reflexivity]] equality proof $refl_x \colon Id_A(x,x)$.

Axiom K can also be called **loop induction** or **self-identification induction** in parallel to [[path induction]]. 

## Statement

$$
  K 
  \colon 
  \underset{A \colon Type}{\prod} 
  \underset{x \colon A}{\prod}
  \underset{P \colon Id_A(x,x) \to Type}{\prod} 
  \left(
     P(refl_A x)
     \to  
    \underset{h \colon Id_A(x,x)}{\prod} P(h)
  \right)
$$

If one doesn't have [[type universes]] in the type theory, then axiom K has to be expressed as an [[inference rule]], and thus is called the **K-rule**:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, p:\mathrm{Id}_A(x,x) \vdash P(x, p) \; \mathrm{type}}{\Gamma \vdash K_{A, P(-, -)}:\prod_{x:A} P(x, \mathrm{refl}_A(x)) \to \prod_{h:\mathrm{Id}_A(x,x)} P(x, h)}$$

The associated judgmental [[computation rule]] for the $K$-rule is

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, p:\mathrm{Id}_A(x,x) \vdash P(x, p) \; \mathrm{type}}{\Gamma, x:A, d:P(x, \mathrm{refl}_A(x)) \vdash K_{A, P(-, -)}(x, d, \mathrm{refl}_A(x)) \equiv d:P(x, \mathrm{refl}_A(x))}$$

### Using the circle type

One can, instead of using elements $x:A$ and self identifications $p:\mathrm{Id}_A(x,x)$, use a function $p:S^1 \to A$ from the [[circle type]] $S^1$ to express axiom K:

$$
  K^{\prime} 
  \colon 
  \underset{A \colon Type}{\prod} 
  \underset{x \colon A}{\prod}
  \underset{P \colon (S^1 \to A) \to Type}{\prod} 
  \left(
     P(\lambda i:S^1.x)
     \to  
    \underset{p:S^1 \to A}{\prod} P(p)
  \right)
$$

This states that the function type $S^1 \to A$ is a [[positive copy]] of $A$, and is equivalent to the other formulation of axiom K through the recursion principle of the [[circle type]]. 

If one doesn't have [[type universes]] in the type theory, then axiom K has to be expressed as an [[inference rule]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, p:S^1 \to A \vdash P(p) \; \mathrm{type}}{\Gamma \vdash K_{A, P(-)}^{\prime}:\prod_{x:A} P(\lambda i:S^1.x) \to \prod_{p:S^1 \to A} P(p)}$$

The associated judgmental [[computation rule]] for the above rule is

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, p:\mathrm{Id}_A(x,x) \vdash P(x, p) \; \mathrm{type}}{\Gamma, x:A, d:P(\lambda i:S^1.x) \vdash K_{A, P(-, -)}(x, d, \lambda i:S^1.x) \equiv d:P(\lambda i:S^1.x)}$$

## Properties

### Relation to $S^1$-localization

The negative analogue of axiom K is the [[axiom of S1-localization|axiom of $S^1$-localization]], which states that 
$$\mathrm{const}_{A, S^1} \equiv \lambda x:A.\lambda i:S^1.x:A \to (S^1 \to A)$$
is an [[equivalence of types]] or a definitional [[isomorphism]]. 

\begin{theorem}
Suppose that every type $A$ is definitionally $S^1$-local.

Then $S^1 \to A$ is a [[positive copy]] of $A$: given any type $A$, and any type family $C(p)$ indexed by loops $p:S^1 \to A$ in $A$, and given any dependent function $t:\prod_{x:A} C(\lambda i:S^1.x)$ which says that for all elements $x:A$, there is an element of the type defined by substituting the constant loop of $x:A$ into $C$, $C(\lambda i:S^1.x)$, one can construct a dependent function $K_A(t):\prod_{z:S^1 \to A} C(z)$ such that for all $x:A$, $K_A(t, \lambda i:S^1.x) \equiv t(x):C(\lambda i:S^1.x)$. 
\end{theorem}

\begin{proof}
$K_A(t)$ is defined to be

$$K_A(t) \equiv \lambda p:S^1 \to A.t(\mathrm{const}_{A, S^1}^{-1}(p))$$

and by the computation rules of loop types as negative copies, one has that for all $x:A$, 

$$\mathrm{const}_{A, S^1}^{-1}(\lambda i:\mathbb{I}.x) \equiv x$$

and so by definition of $\mathrm{ind}_{S^1 \to A}(t)$ and the judgmental congruence rules for substitution, one has

$$K_A(t, \lambda i:S^1.x) \equiv t(\mathrm{const}_{A, S^1}^{-1}(\lambda i:S^1.x)) \equiv t(x)$$
\end{proof}

\begin{theorem}
Suppose that for all types $A$, $S^1 \to A$ is a [[positive copy]] of $A$ through the function 
$$\mathrm{const}_{A, S^1} \equiv \lambda x:A.\lambda i:S^1.x:A \to (S^1 \to A)$$

Then Streicher's axiom K is true: given a type $A$ and given a type family $C(x, P)$ indexed by $x:A$ and $p:x =_A X$, and a dependent function $t:\prod_{x:A} C(x, \mathrm{refl}_A(x))$, one can construct a dependent function

$$K_A(t):\prod_{x:A} \prod_{p:x =_A X} C(x, p)$$

such that for all $x:A$, 

$$K_A(t, x, \mathrm{refl}_A(x)) \equiv t(x)$$
\end{theorem}

\begin{proof}
By the induction principle of [[positive copies]] on the type family $C(f(\mathrm{base}), \mathrm{ap}_f(\mathrm{loop}))$ indexed by $f:S^1 \to A$, we can construct a dependent function

$$K_A^{\prime}(t):\prod_{f:\mathbb{I} \to A} C(f(\mathrm{base}), \mathrm{ap}_f(\mathrm{loop}))$$

such that for all $x:A$,

$$K_A^{\prime}(t, \lambda i:S^1.x) \equiv t(x):C(x, \mathrm{refl}_A(x))$$ 

since by definition of constant function and reflexivity, one has

$$(\lambda i:\mathbb{I}.x)(\mathrm{base}) \equiv x \quad \mathrm{ap}_{\lambda i:\mathbb{I}.x}(\mathrm{loop}) \equiv \mathrm{refl}_A(x)$$

We define 

$$K_A(t, x, p) \equiv K_A^{\prime}(t, \mathrm{rec}_{S^1}^A(x, p))$$

since by circle recursion one has a path $\mathrm{rec}_{S^1}^A(x, p):S^1 \to A$ such that

$$\mathrm{rec}_{S^1}^{A}(x, p)(\mathrm{base}) \equiv x \quad \mathrm{ap}_{\mathrm{rec}_{S^1}^{A}(x, p)}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv p$$
\end{proof}

One has the following analogies between localization at a specific type and the type theoretic letter rule that it proves:

| localization rule | type theoretic letter rule |
|-------------------|----------------------------|
| [[I-localization|$\mathbb{I}$-localization]] | [[J-rule]] |
| [[S1-localization|$S^1$-localization]] | [[K-rule]] |

### Computational behavior

Unlike its logical equivalent [[axiom UIP]], axiom K can be endowed with computational behavior: $K(A,x,P,d,refl_A x)$ computes to $d$.  This gives a way to specify a computational propositionally extensional type theory.

This sort of computational axiom K can also be implemented with, and is sufficient to imply, a general scheme of function definition by pattern-matching.  This is implemented in the proof assistant [[Agda]].  (The flag `--without-K` alters Agda's pattern-matching scheme to a weaker version appropriate for [[intensional type theory]], including [[homotopy type theory]].)

## Related concepts

* [[axiom UIP]]

* [[axiom of S1-localization|axiom of $S^1$-localization]]

* [[J-rule]], [[interval type localization]] 

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
[[!redirects Streicher\'s axiom K]]
[[!redirects Axiom K (type theory)]]

[[!redirects K rule]]
[[!redirects Streicher's K rule]]
[[!redirects Streicher\'s K rule]]
[[!redirects K rule (type theory)]]

[[!redirects K-rule]]
[[!redirects Streicher's K-rule]]
[[!redirects Streicher\'s K-rule]]
[[!redirects K-rule (type theory)]]

[[!redirects self-identity induction]]
[[!redirects loop induction]]
[[!redirects self-identification induction]]
[[!redirects self-equality induction]]

[[!redirects self-identity elimination]]
[[!redirects loop elimination]]
[[!redirects self-identification elimination]]
[[!redirects self-equality elimination]]

[[!redirects self-identity computation]]
[[!redirects loop computation]]
[[!redirects self-identification computation]]
[[!redirects self-equality computation]]