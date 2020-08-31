
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[topological space]]/[[simplicial set]]/[[homotopy type]]/[[infinity-groupoid]] $X$ is _nilpotent_ if 

1. its [[fundamental group]] is a [[nilpotent group]] 

1. the canonical [[action]] of $\pi_1(X)$ on all the higher [[homotopy groups]] $\pi_{n \geq 2}(X)$ is nilpotent. 

The first condition means that $\pi_1(X)$ is isomorphic to an iterated [[central extension]] of [[abelian groups]].

The second condition means that each $\pi_{n  \geq 2}(X)$ admits a [[sequence]] of [[subgroups]]

$$
  \ast = G_k \hookrightarrow \cdots \hookrightarrow G_1  = \pi_n(X)
$$

such that for all $i$

1. $G_{i+1} \hookrightarrow G_i$ is a [[normal subgroup]];

1. the [[quotient]] $G_i/G_{i+1}$ is an [[abelian group]];

1. each $G_i$ is closed under the action of $\pi_1(X)$;

1. the induced action on $G_i/G_{i+1}$ is trivial.

This implies that given any element $a \in \pi_{n \geq 2}(X)$, then after acting on it at most $k$ times with elements from $\pi_1(X)$ the result is [[zero]].

## Properties

Nilpotency is involved in sufficient conditions for many important constructions in ([[stable homotopy theory|stable]]) [[homotopy theory]], see for instance at 

* [[localization of a space]];

* [[fracture theorem]].

## Related concepts

* [[finite homotopy type]]

* [[p-local homotopy type]]

* [[p-complete homotopy type]]

\linebreak

* [[rational homotopy theory]]

  * [[Sullivan model]]

  * [[rational fiber lemma]]


## References

See the references at _[[nilpotent topological space]]_

Review includes

* {#Riehl14} [[Emily Riehl]], def. 14.4.9 in _Categorical homotopy theory_, new mathematical monographs 24, Cambridge University Press 2014 (published version)

See also 

* Wikipedia, _[Nilpotent space](https://en.wikipedia.org/wiki/Nilpotent_space)_

[[!redirects nilpotent homotopy types]]

[[!redirects nilpotent space]]
[[!redirects nilpotent spaces]]

[[!redirects nilpotent spectrum]]
[[!redirects nilpotent spectra]]
 