
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A __one-parameter group__ (of [[unitary operators]] in a [[Hilbert space]]) is a [[homomorphism of groups]]
$$\mathbf{R} \to U(H),$$
where $H$ is a [[Hilbert spaces]], [[U(H)|$U(H)$]] denotes its group of [[unitary operators]] and $\mathbf{R}$ the [[addition|additive]] group of [[real numbers]].

More generally, one can define __one-parameter [[semigroups]]__ of operators in a [[Banach space]] $X$ as homomomorphisms of [[monoids]]
$$\mathbf{R}_{\ge0} \to B(X),$$
where $B(X)$ denotes the semigroup of [[bounded operators]] $X\to X$.

Typically, we also require a [[continuous map|continuity]] condition such as continuity in the [[strong topology]].

## Stone theorem

Strongly continuous one-parameter unitary groups $(U_t)_{t\ge0}$ of operators in a Hilbert space $H$
are in [[bijection]] with [[self-adjoint operator|self-adjoint]] [[unbounded operators]] $A$ on $H$:

This bijection sends
$$
  A
    \mapsto 
  \big(
     t\mapsto \exp(itA)
  \big)
  \,.
$$

The operator $A$ is [[bounded operator|bounded]] if and only if $U$ is norm-continuous.

## Hille–Yosida theorem

Strongly continuous one-parameter semigroups $T$ of bounded operators on a [[Banach space]] $X$ (alias __$C_0$-semigroups__) satisfying $\|T(t)\|\le M\exp(\omega t)$ are in bijection with closed operators $A\colon X\to X$ with dense domain such that any $\lambda\gt \omega$ belongs to the resolvent set of $A$
and for any $\lambda\gt\omega$ we have
$$\|(\lambda I-A)^{-n}\|\le M (\lambda-\omega)^{-n}.$$

## References

[…]