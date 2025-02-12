
> under construction

#Contents#
* table of contents
{:toc}

## Idea

For $\mathbf{B} = Sh_\infty(CRing_\infty^{op}, et)$ the [[(∞,1)-topos]] of [[E-∞ geometry]], let

$$
  \mathbf{H} \coloneqq Sh_\infty(SmoothMfd, \mathbf{B})
$$

be the [[(∞,1)-category of (∞,1)-sheaves]] on the [[site]] of [[smooth manifolds]] with values in $\mathbf{B}$.

An [[object]] in this $\mathbf{H}$ combines the properties of a [[smooth ∞-groupoid]] and an object in [[E-∞ geometry]], hence might be called a "smooth $E_\infty$-groupoid".

It is useful to regard this as a [[cohesive (∞,1)-topos]] over $\mathbf{B}$

$$
  \mathbf{H}
  \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  \mathbf{B}
  \,.
$$

As such this appears for instance in the discussion at 

* [[differential algebraic K-theory]]

* [[equivariant elliptic cohomology]].

## Constructions

### Multiplicative group

Write 

$$
  \mathbb{G}_m \in \mathbf{B}
$$

for the sheaf which sends each ring to its [[∞-group of units]]

$$
  \mathbb{G}_m \;\colon\; R \mapsto R^\times
  \,.
$$

This is the canonical group object in $\mathbf{B}$. The [[mapping stacks]] into it are the [[Picard ∞-stacks]].

(...)


For [[E-∞ rings]] over the [[complex numbers]], hence [[E-∞ algebras]] over $\mathbb{C}$, the [[multiplicative group]]

$$
  \mathbb{G}_m = \mathbb{C}^\times
$$

naturally carries both the structure of an object in [[smooth ∞-groupoids]] and in [[E-∞ geometry]], which may be combined to the structure of a smooth $E_\infty$-groupoid.

For $U \in SmthMfd$ and $A \in CRing_\infty(\mathbb{C})$ let $\mathbb{G}_m \in \mathbf{H}$ be given by

$$
  \mathbb{G}_m \;\colon\; (U,A) \mapsto GL_1(A)\otimes C^\infty(U,\mathbb{C}^\times)
  \,,
$$

where on the right we have the [[∞-groupoid]] underlying the [[abelian ∞-group]] which is the [[tensor product]] of the [[∞-group of units]] of $A$ with the [[abelian group]] of non-vanishing complex-valued [[smooth functions]] on $X$.



[[!redirects smooth E-∞-groupoid]]

[[!redirects smooth E-infinity-groupoids]]
[[!redirects smooth E-∞-groupoids]]

[[!redirects smooth E-∞ groupoid]]
[[!redirects smooth E-∞ groupoids]]

[[!redirects smooth E-infinity groupoid]]
[[!redirects smooth E-infinity groupoids]]

[[!redirects smooth E∞ groupoid]]
[[!redirects smooth E∞ groupoids]]

[[!redirects smooth E∞-groupoid]]
[[!redirects smooth E∞-groupoids]]
