
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

\tableofcontents

## Definition

In [[dependent type theory]], a **definitional isomorphism** or **defintional section-retraction** or **judgmental isomorphism** between two types $A$ and $B$ consists of functions $f:A \to B$ and $f^{-1}:B \to A$ such that given any term $x:A$, the term $f^{-1}(f(x))$ is [[judgmental equality|judgmentally equal]] to $x$ and given any term $y:B$, the term $f(f^{-1}(y))$ is definitionally equal to $y$.  In symbols, 
$$x:A \vdash f^{-1}(f(x)) \equiv x:A \quad \mathrm{and} \quad y:B \vdash f(f^{-1}(y)) \equiv y:B$$

If the dependent type theory has [[identity types]], definitional isomorphisms are, in particular, [[equivalences in type theory|equivalences]] since the [[homotopies]] and [[coherence law]] for (half-adjoint) equivalences are derivable from the judgmental equalities in definitional isomorphisms. 

One example of a definitional isomorphism in dependent type theory is the [[identity equivalence]], defined by two copies of the [[identity function]] $\lambda \chi.\chi$ and by the fact that the identity function is a definitional [[involution]], where $(\lambda \chi.\chi)((\lambda \chi.\chi)(x))$ reduces to $x$. 

Definitional isomorphisms are used to [[extensionality principle|characterize the identity types]] of various basic types such as [[dependent sum types]] and [[dependent product types]] in binary [[parametric dependent type theory|parametric]] [[observational type theory]] and [[higher observational type theory]]. 

In addition, definitional isomorphisms and definitional isomorphism types allow for easier proofs of the [[typal congruence rules]] of various types, since the judgmental equalities allow one to avoid [[transport]] hell that comes with the usual proofs of typal congruence rules using weak equivalences. See [[dependent product type#TypalCongruenceRules|dependent product type]] for an example of two sets of such proofs using definitional isomorphisms and weak equivalences respectively, the one using definitional isomorphisms is simpler than the one using weak equivalences. 

## Definitional isomorphism types

Given types $A$ and $B$, one could define the type of definitional isomorphisms between $A$ and $B$. These are given by the following [[inference rules]]:

Formation rule for definitional isomorphism types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \cong B \; \mathrm{type}}$$

Introduction rule for definitional isomorphism types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, y:B \vdash g(y):A \quad \Gamma, x:A \vdash g(f(x)) \equiv x:A \quad \Gamma, y:B \vdash f(g(y)) \equiv y:B}{\Gamma \vdash \mathrm{toDefIso}(x:A.f(x), y:B.g(y)):A \cong B}$$

Elimination rules for definitional isomorphism types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \cong B, x:A \vdash \overrightarrow{e}(x):B} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \cong B, y:B \vdash \overleftarrow{e}(x):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \cong B, x:A \vdash \overleftarrow{e}(\overrightarrow{e}(x)) \equiv x:A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \cong B, y:B \vdash \overrightarrow{e}(\overleftarrow{e}(y)) \equiv y:B}$$

Computation rules for definitional isomorphism types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, y:B \vdash g(y):A \quad \Gamma, x:A \vdash g(f(x)) \equiv x:A \quad \Gamma, y:B \vdash f(g(y)) \equiv y:B}{\Gamma, x:A \vdash \overrightarrow{\mathrm{toDefIso}(x:A.f(x), y:B.g(y))}(x) \equiv f(x):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B \quad \Gamma, y:B \vdash g(y):A \quad \Gamma, x:A \vdash g(f(x)) \equiv x:A \quad \Gamma, y:B \vdash f(g(y)) \equiv y:B}{\Gamma, y:B \vdash \overleftarrow{\mathrm{toDefIso}(x:A.f(x), y:B.g(y))}(y) \equiv g(y):A}$$

Uniqueness rules for definitional isomorphism types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, e:A \cong B \vdash \mathrm{toDefIso}(x:A.\overrightarrow{e}(x), y:B.\overleftarrow{e}(y)) \equiv e:A \cong B}$$

### Properties

In the presence of definitional isomorphism types and the [[inductively defined]] [[identity types]], [[transport]] can be defined as definitional isomorphism via the [[J-rule]], since the [[identity function]] or [[identity equivalence]] is a definitional isomorphism and thus one can apply the J-rule to reflexivity to get the identity as a definitional isomorphism:

$$x:A, y:A, p:x =_A y \vdash \mathrm{ind}_{\mathrm{Id}}^{A, B(x) \cong B(y)}(p):B(x) \cong B(y)$$ 


$$x:A \vdash \mathrm{ind}_{\mathrm{Id}}^{A, B(x) \cong B(x)}(\mathrm{refl}_A(x)) \equiv \mathrm{toDefIso}(\chi:A.\chi, \chi:A.\chi):B(x) \cong B(x)$$ 

However, the dependent type theory will no longer have [[decidable equality]] if it has definitional isomorphism types, as definitional isomorphism types allow one to include arbitrary definitional isomorphisms in [[contexts]]. In turn, this allows one to define [[fixed point]] operators, which are incompatible with decidable equality for dependent type theories. 

## Related concepts

* [[judgmental equality]]
* [[function]], [[function type]]
* [[equivalence of types]], [[equivalence type]]
* [[isomorphism]]

## References

Definitional isomorphism is called "definitional section-retraction" in:

* {#ACKS24} [[Thorsten Altenkirch]], [[Yorgo Chamoun]], [[Ambrus Kaposi]], [[Michael Shulman]], *Internal parametricity, without an interval*, Proceedings of the ACM on Programming Languages (POPL) **8** (2024) 2340-2369 &lbrack;[arXiv:2307.06448](https://arxiv.org/abs/2307.06448), [doi:10.1145/3632920](https://doi.org/10.1145/3632920)&rbrack;

The proof assistant [[Narya]] makes use of definitional isomorphisms to characterize identity/bridge types.

[[!redirects definitional isomorphism]]
[[!redirects definitional isomorphisms]]

[[!redirects definitional section-retraction]]
[[!redirects definitional section-retractions]]

[[!redirects judgmental isomorphism]]
[[!redirects judgmental isomorphisms]]

[[!redirects definitional isomorphism type]]
[[!redirects definitional isomorphism types]]

[[!redirects type of definitional isomorphisms]]
[[!redirects types of definitional isomorphisms]]

[[!redirects judgmental isomorphism type]]
[[!redirects judgmental isomorphism types]]

[[!redirects type of judgmental isomorphisms]]
[[!redirects types of judgmental isomorphisms]]