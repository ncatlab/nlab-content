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
Fields are finitely [[first-order theory|first-order]] axiomatizable. An [[algebraically closed field]] is further axiomatized by infinitely many sentences which state that all polynomials with coefficients from the ring of integers of the [[prime field]] have a root. Once we additionally specify a characteristic $p$, $\mathsf{ACF}_p$ turns out to be complete, [[elimination of imaginaries|eliminates imaginaries]], is [[stability theory|stable]], and admits [[quantifier elimination]].

## Definition
$\mathsf{ACF}$ is the countable collection of sentences in the language $\mathcal{L}_{\operatorname{ring}}$ of rings given by:

$$\{\text{field axioms}\} + \left\{ (\exists x)[a_n x^n + \dots + a_0 = 0] \right\},$$

where the tuples $\overline{a}$ range over all finite tuples of integers (which are actually shorthand for the unit $1$ added to itself as many times as necessary (or the additive inverse of this)). 

We additionally specify a characteristic $p$ to obtain $\mathsf{ACF}_p$ by either saying that $1 + \dots \text{ (n times) } \dots + 1 \neq 0$ for all $n$, or that this does happen at $p$.

## Properties
* $\mathsf{ACF}$ has quantifier elimination. This amounts to a special case of Chevalley's direct image theorem from algebraic geometry.

* $\mathsf{ACF}$ is [[stability theory|stable]].

* $\mathsf{ACF}$ is _totally transcendental_: [[Morley rank]] is defined everywhere. In this setting Morley rank subsumes the usual Krull dimension of an algebraic variety.

* $\mathsf{ACF}$ is _uncountably categorical_: for each uncountable $\kappa$, models of $\mathsf{ACF}$ of size $\kappa$ must all be isomorphic. This fails at $\aleph_0$: $\mathbb{Q}^{\operatorname{alg}}$ has transcendence degree zero while there exist countable algebraically closed overfields of $\mathbb{Q}$ with infinite transcendence degree.

* $\mathsf{ACF}$ [[elimination of imaginaries|eliminates imaginaries]]. This means that its [[syntactic category]] $\mathbf{Def}(\mathsf{ACF})$ has effective [[internal congruence|internal congruences]], and has a good [[model-theoretic Galois theory|Galois theory]].

* It's easy to see that $\mathsf{ACF}$ [[elimination of imaginaries|codes]] all finite sets: if $R$ is a finite set of points inside a monster $\mathbb{M}$, its code is the tuple $c$ of coefficients for the polynomial

$$f(X) \overset{\operatorname{df}}{=} \displaystyle \prod_{r \in R} (X - R),$$

so that $c$ is fixed by an automorphism of $\mathbb{M}$ if and only if that automorphism permutes $R$.

## Related concepts
* [[the theory of differentially closed fields]]
## References
* Dave Marker, _Model Theory: An Introduction_.

[[!redirects ACF]]