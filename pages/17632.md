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
Fields are finitely [[first-order theory|first-order]] axiomatizable. An [[algebraically closed field]] is further axiomatized by infinitely many sentences which state that all non-constant polynomials have a root. Once we additionally specify a characteristic $p$, $\mathsf{ACF}_p$ turns out to be complete, [[elimination of imaginaries|eliminates imaginaries]], is [[stability theory|stable]], and admits [[quantifier elimination]].

## Definition
$\mathsf{ACF}$ is the countable collection of sentences in the language $\mathcal{L}_{\operatorname{ring}}$ of rings given by:

$$\{\text{field axioms}\} + \left\{ (\forall a_0, \ldots, a_{n-1}) (\exists x)[x^n + \sum_{i=0}^{n-1} a_i x_i = 0] \right\},$$

where $n = 1, 2, \ldots$. 

We can additionally specify a characteristic $p$ to obtain $\mathsf{ACF}_p$ by either adding the axioms $\{ 1 \ne 0 , 1+1 \ne 0 , \cdots \}$ to get $\mathsf{ACF}_0$ or adding the axiom $\underbrace{1+\cdots+1}_\text{$p$ terms} = 0$ to get $\mathsf{ACF}_p$ (where $p$ is prime).

## Properties
* $\mathsf{ACF}$ has quantifier elimination. This amounts to a special case of Chevalley's direct image theorem from algebraic geometry.

* $\mathsf{ACF}$ is [[stability theory|stable]].

* $\mathsf{ACF}$ is _totally transcendental_: [[Morley rank]] is defined everywhere. In this setting Morley rank subsumes the usual Krull dimension of an algebraic variety.

* $\mathsf{ACF}$ is _uncountably categorical_: for each uncountable $\kappa$, models of $\mathsf{ACF}$ of size $\kappa$ must all be isomorphic. This fails at $\aleph_0$: $\mathbb{Q}^{\operatorname{alg}}$ has transcendence degree zero while there exist countable algebraically closed overfields of $\mathbb{Q}$ with infinite transcendence degree.

* $\mathsf{ACF}$ [[elimination of imaginaries|eliminates imaginaries]]. This means that its [[syntactic category]] $\mathbf{Def}(\mathsf{ACF})$ has effective [[internal congruence|internal congruences]], and has a good [[model-theoretic Galois theory|Galois theory]].

* It's easy to see that $\mathsf{ACF}$ [[elimination of imaginaries|codes]] all finite sets: if $R$ is a finite set of points inside a monster $\mathbb{M}$, its code is the tuple $c$ of coefficients for the polynomial

$$f(X) \overset{\operatorname{df}}{=} \displaystyle \prod_{r \in R} (X - r),$$

so that $c$ is fixed by an automorphism of $\mathbb{M}$ if and only if that automorphism permutes $R$.

## Related concepts
* [[theory of differentially closed fields]]

* [[quantifier elimination]]

* [[stable theory]]

* [[Morley rank]]

## References
* Dave Marker, _Model Theory: An Introduction_.

[[!redirects ACF]]