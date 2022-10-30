
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The generalization of the concept of [[homotopy group]] from [[homotopy theory]] and [[stable homotopy theory]] to [[equivariant homotopy theory]] and [[equivariant stable homotopy theory]].

## Definition

### Via genuine $G$-spectra

Consider [[genuine G-spectra]] modeled on [[G-universe]] $U$.

For a _finite_ based [[G-CW complex]] $X$ and base [[topological G-space]] $Y$, write

$$
  \{X,Y\}_G \coloneqq \underset{\longrightarrow}{\lim}_{V \subset U} [\Sigma^V X, \Sigma^V Y]_G
$$

for the [[colimit]] over $G$-[[homotopy classes]] of maps between [[suspensions]] $\Sigma^V X \coloneqq S^V \wedge X$, where $V$ runs through the indexing spaces in the universe and $S^V$ denotes its [[representation sphere]].

([May 96, IX.2 def. 2.1](#May96))

The equivariant stable homotopy groups of $X$ are

$$
  \pi_V^G(\Sigma^\infty_G X) \coloneqq \{S^V,X\}_G
  \,.
$$

([May 96, IX.2 remark 2.4](#May96))

And for subgroups $H \subset G$

$$
  \pi_V^H(\Sigma^\infty_G X) \coloneqq \{G/H_+ \wedge S^V,X\}_G
  \,.
$$


### Via orthogonal spectra and $G$-equivariant maps

Let $G$ be a [[finite group]]. For $X$ a $G$-[[equivariant spectrum]] modeled as an [[orthogonal spectrum]] with $G$-[[action]], then for $k \in \mathbb{N}$ the $k$th equivariant homotopy group of $X$ is the [[colimit]]

$$
  \pi_k^G(X)
  \coloneqq
  \underset{\longrightarrow_{\mathrlap{n}}}{\lim} [S^{n \rho_G}, (\Omega^k X)(n \rho_G)]_H
  \,,
$$

where

* $\rho_G$ denotes the [[fundamental representation]] of $G$

* $n \rho_G = (\rho_G)^{\oplus_n}$;

* $S^{n \rho_G}$ is its [[representation sphere]];

* $X(n \rho_G)$ is the value of $X$ in [[RO(G)-degree]] $n\rho_G$;

* $[-,-]_G$ is the set of [[homotopy classes]] of $G$-equivariant maps of pointed [[topological G-spaces]].

(e.g. [Schwede 15, section 3](#Schwede15))

More generally for $H \hookrightarrow G$ a [[subgroup]] then one writes $\pi_\bullet^H(X)$ for the $H$-equivariant subgroups of $X$ with $X$ regarded now as an $H$-[[equivariant spectrum]], via restriction of the action.

(e.g. [Schwede 15, p. 16](#Schwede15))

### Via fixed point spectra

Equivalently, the $k$th $G$-equivariant homotopy group of a $G$-equivariant spectrum $X$ is the plain $k$th homotopy group of its [[fixed point spectrum]] $F^G X$

$$
  \pi_k^G(X) \simeq \pi_k(F^G X)
  \,.
$$

(e.g. [Schwede 15, prop. 7.2](#Schwede15))

## Examples

### Of equivariant suspension spectra

For $X$ a [[pointed topological space|pointed]] [[topological G-space]], then by the discussion [there](equivariant+suspension+spectrum#ROGDegrees)) the formula for the equivariant homotopy groups of its [[equivariant suspension spectrum]] $\Sigma^\infty_G X$ reduces to

$$
  \pi_k^G(\Sigma^\infty_G X)
  \coloneqq
  \underset{\longrightarrow_n}{\lim} [S^{n \rho_g}, (\Omega^k X)\wedge S^{n \rho_G}]_G
  \,,
$$

Specifically for the [[equivariant sphere spectrum]], see _[here](equivariant+sphere+spectrum#EquivariantHomotopyGroups)_.

## Properties

### Relation to Mackey functors

As $H$-varies over the [[subgroups]] of a $G$-[[equivariant spectrum]], the $H$-equivariant homotopy groups organize into a [[Mackey functor]] 

$$
  \underline{\pi}_\bullet(X)
  \colon
  G/H \mapsto \pi^H_\bullet(X)
  \,.
$$

(e.g. [Schwede 15, p. 16 and section 4](#Schwede15))

(...)

### Equivariant stable Whitehead theorem

The equivariant version of the stable [[Whitehead theorem]] holds:

a mpa of $G$-spectra $f \colon E \longrightarrow F$ is a [[weak equivalence]] (e.g. an $RO(G)$-degree-wise [[weak homotopy equivalence]] of [[topological G-spaces]] in the [model via indexing on all representations](#IndexedOnAllRepresentations)) precisely it if induces [[isomorphisms]] $\pi_\bullet(f) \colon \pi_\bullet(E) \longrightarrow \pi_{\bullet}(F)$ on all [[equivariant homotopy group]] [[Mackey functors]].
 
([Greenlees-May, theorem 2.3](#GreenleesMay))


## References


* {#GreenleesMay} [[John Greenlees]], [[Peter May]], section 2 of _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

* {#May96} [[Peter May]], section IX.4 of _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comeza&#732;na, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/alaska1.pdf))


* {#Schwede15} [[Stefan Schwede]], _[[Lectures on Equivariant Stable Homotopy Theory]]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))


[[!redirects equivariant homotopy groups]]