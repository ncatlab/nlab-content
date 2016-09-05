+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
In [[model theory]], the _definable closure_ of a subset of a model is a way of "generating a substructure" around that subset. The _algebraic closure_ of a subset always contains the definable closure and generalizes the usual [[algebraic closure]] of fields.

## Definition

Let $A$ be a small parameter set (i.e. a subset) of a [[monster model]] $\mathbb{M} \models T.$ The _definable closure_ $\operatorname{dcl}(A)$ of $A$ is the set of all tuples $b \in \mathbb{M}$ such that there exists a formula $\varphi(x,y)$ and a tuple $a$ from $A$ such that $b$ is the unique solution to $\varphi(a,y)$, i.e. $\varphi(\mathbb{M}_x,y) = \{b\}$.

To obtain the _algebraic closure_ $\operatorname{acl}(A)$ of $A$, we relax "unique solution" to "one of finitely many."

## Inside a monster
Inside a sufficiently saturated and homogeneous model $\mathbb{M}$, tuples $b$ are definable over $A$ if and only if they are fixed by the stabilizer $\operatorname{Aut}(\mathbb{M}/A)$ of $A$, and are algebraic over $A$ if and only if they have finite orbit under $\operatorname{Aut}(\mathbb{M}/A).$

_Proof._ To see nonobvious direction of the first claim, try the contrapositive: if every formula in the [[type (in model theory)|type]] of $b$ fails to uniquely pick out $b$, then the type of some $b'$ which is not $b$ but has the same type as $b'$ is finitely consistent, therefore realized, and by homogeneity there is an automorphism interchanging $b$ and $b'$.

To see the nonobvious direction of the second claim, try the contrapositive again: if $b$ isn't algebraic over $A$, then every formula in its type over $A$ is infinite, in particular all conjunctions of finite fragments of its type. So we can iteratively obtain infinitely many disjoint realizations of its type, and again by homogeneity these must all lie in the same orbit. $\square$

Saturation ensures that infinite definable sets become big---as big as the universe $\mathbb{M}$, while finite sets stay the same size, because the theory knows exactly how big they are.

## Examples
* In $\mathsf{ACF}_p$, the definable closure inside a monster $\mathbb{M}$ of a subset $A$ is the [[perfect field|perfect hull]] of $\mathbb{F}(A)$, where $\mathbb{F}$ is $\mathbb{Q}$ for $p = 0$ or the [[prime field]] of the characteristic $p > 0$, and algebraic closure coincides with the [[separable closure]].

* In the theory of an infinite set without structure, definable and algebraic closures coincide, and are trivial.

* In the relational structure consisting of the disjoint union of the cycle graphs of length $n$ for each $n \geq 1$, $\operatorname{dcl}(\emptyset)$ is just the cycle graph of length $1$, while $\operatorname{acl}(\emptyset)$ is the entire structure.

## Related concepts
* [[type (in model theory)]]
* [[model-theoretic Galois theory]]

## References
* Lou van den Dries, _An Introduction to Model-Theoretic Stability_.
* Dave Marker, _Model Theory: An Introduction_.

[[!redirects model-theoretic algebraic closure]]
[[!redirects definably closed]]
[[!redirects definable closure]]