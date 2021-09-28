
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[geometric quantization]] of a [[symplectic manifold]] $(X, \omega)$, a _Bohr-Sommerfeld leaf_ is a [[Lagrangian submanifold]] of $X$ on which not only the [[symplectic form]] $\omega$ vanishes, but on which also a given [[prequantum bundle|prequantization]] $\nabla$ of $\omega$ is trivializable. 

Therefore given a [[real polarization]] of $(X,\omega)$, hence a [[foliation]] by [[Lagrangian submanifolds]], the Bohr-Sommerfeld leaves form a discrete subset of the [[leaf space]]. The discreteness of this subset is essentially the formal incarnation of  "quantization" and this is what [[Niels Bohr|Bohr]] and [[Arnold Sommerfeld|Sommerfeld]] originally considered (in less abstract terms, the archetypical example was the harmonic oscillator as discussed [below](#HarmonicOscillator)).

(There is a correction to this picture, given by the fact that a [[quantum states]]/[[semiclassical states]], involve not just Lagrangian submanifolds/Bohr-Sommerfeld leaves, but moreover [[half-densities]] over these. These are to satisfy an additional condition, encoded by the _[[metaplectic correction]]_.)





## Definition


Let $(X,\omega)$ be a ([[presymplectic manifold|pre-]])[[symplectic manifold]] and $\nabla$ a [[prequantum bundle|prequatization]], hence a $U(1)$-[[principal connection]] on $X$ with [[curvature]] 2-form $F_\nabla = \omega$.

+-- {: .num_defn}
###### Definition

A [[Lagrangian submanifold]] $L \hookrightarrow X$ is a **Bohr-Sommerfeld leaf** if the restriction $\nabla|_L$ of the [[prequantum connection]] to $L$ is trivializable there, hence if its [[cohomology]] class vanishes in [[ordinary differential cohomology]]

$$
  [\nabla_L] = 0 \in H^2_{conn}(X)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

For every [[isotropic submanifold]], hence in particular every [[Lagrangian submanifold]], $L \hookrightarrow X$ the restriction $\nabla|_L$ is necessarily already a [[flat connection]]. As discussed there, flat connections are equivalently encoded in the [[holonomy]] of their [[parallel transport]]: a flat connection is trivializable as a connection precisely if its [[holonomy]] is trivial. Therefore a Bohr-Sommerfeld leaf is equivalently a Lagrangian submanifold $L$ such that $\nabla|_L$ has trivial holonomy. In this form the Bohr-Sommerfeld condition is usually stated in the literature.

=--

+-- {: .num_remark}
###### Remark

The Bohr-Sommerfeld condition is the natural lift of the [[Lagrangian subspace]]-condition to prequantum geometry:

When expressed in terms of [[smooth infinity-groupoid|smooth]] [[moduli stacks]] (see at _[[geometry of physics]]_ for background), the ([[presymplectic manifold|pre-]])[[symplectic manifold|symplectic structure]] is equivalently a map

$$
  \omega \;\colon\; X \to \Omega^2_{cl}
$$

and a prequantization $\nabla$ is equivalently a lift $\nabla$ in the diagram

$$
  \array{
    && \mathbf{B}U(1)_{conn}
    \\
    & {}^{\mathllap{\nabla}}\nearrow & \downarrow^{\mathrlap{F_{(-)}}}
    \\
    X &\stackrel{\omega}{\to}& \Omega^2_{cl}(X)
  }
  \,.
$$

The condition on an [[isotropic submanifold]] $L \hookrightarrow X$ is that the composite map

$$
  \omega|_L
  \;\colon\;
  \array{
    L &\hookrightarrow &  X &\stackrel{\omega}{\to}& \Omega^2_{cl}
  }
$$

is trivial in $H(L,\Omega^2_{cl}) = \Omega^2_{cl}(L)$ (and $L$ being Lagrangian means that it is maximal with this property). Then $L$ is Bohr-Sommerfeld if moreover the restriction of the prequantum lift

$$
  \nabla|_L
  \;\colon\;
  \array{
    L &\hookrightarrow &  X &\stackrel{\nabla}{\to}& \mathbf{B}U(1)_{conn}
  }
$$

is trivial in $H(L, \mathbf{B}U(1)_{conn}) = H^2_{conn}(X)$.

=--


## Examples

### Harmonic oscillator
 {#HarmonicOscillator}

For the single 1-dimensional [[Harmonic oscillator]], [[phase space]] is the [[symplectic manifold]] $\mathbb{R}^2$ equipped with the symplectic form

$$
  \omega = d_{dR} t \wedge d\theta
  \,,
$$

where on $\mathbb{R}^2- \mathbb{R}_+$ $(t, \theta)$ are the canonical [[polar coordinates]].

We may choose the trivial [[prequantum line bundle]] with [[connection on a bundle|connection]] given by the globally defined [[differential form|differential 1-form]]

$$
  \Theta := t \wedge d\theta
  \,.
$$

Then a [[polarization]] is given by the [[foliation]] whose [[leaves]] are the [[submanifolds]] of constant $t$.

The [[covariant derivative]] along any leaf acts as

$$
  (\nabla_\Theta \sigma)(t, \theta) 
  = (\frac{\partial}{\partial \theta} \sigma)(t, \theta)
  - i t \sigma(t, \theta)
 \,.
$$

The covariantly sections covariantly constat on a leaf hence must be of the form

$$
  \sigma(t, \theta) = a(t) \exp( i t \theta)
  \,.
$$

For this to be well-defined as a globally defined section on the whole leaf the condition

$$
  t = 2 \pi k \; \; k \in \mathbb{Z}
$$

has to hold. Hence the Bohr-Sommerfeld leaves here are the [[circles]] of radius $2 \pi k$ in $\mathbb{R}^2$.

## Properties

+-- {: .num_theorem}
###### Theorem
**(Guillemin-Sternberg)**

If a [[polarization]] of $X$ is a [[regular fibration]] with [[compact space|compact]] [[leaves]] over a [[simply connected]] base $B$, then the Bohr-Sommerfeld leaves form a discrete subset given by 

$$
  \{F_BS\} = \{
    p \in X | (f_1(p), \cdots, f_n(p)) \in \mathbb{Z}^n
  \}
$$

where the $\{f_i\}$ are global [[action coordinates]] on the base space $B$.

=--


+-- {: .num_theorem}
###### Theorem
**(Sniatycki)**

If the leaf space $B$ is [[Hausdorff space|Hausdorff]] and the projection $X \to B$ has [[compact space|compact]] fibers, then the [[dimension]] of the [[space of states (in geometric quantization)|space of quantum states]] is given by the number of Bohr-Sommerfeld leaves.

=--

## References

Named after [[Niels Bohr]] and [[Arnold Sommerfeld]].

For historical background see also

* Wikipedia, *[Old quantum theory](https://en.wikipedia.org/wiki/Old_quantum_theory)*.

Discussion in the modern formalism of [[geometric quantization]]:

* J. &#346;niatycki, _Wave functions relative to a real polarization_, Internat. J. Theoret. Phys., 14(4):277&#8211;288 (1975)

* J. &#346;niatycki, _Geometric Quantization and Quantum Mechanics_, volume 30 of Applied Mathematical Sciences. Springer-Verlag, New York (1980)

* Mark Hamilton, _Locally toric manifolds and singular Bohr-Sommerfeld leaves_

* Eva Miranda, _From action-angle coordinates to geometric quantization and back_ (2011) ([pdf](http://fdis2011.uni-jena.de/Talks/Eva%20Miranda.pdf))

[[!redirects Bohr-Sommerfeld leaves]]



[[!redirects BS-leaf]]
[[!redirects BS-leaves]]

[[!redirects Bohr-Sommerfeld quantization]]

[[!redirects Bohr-Sommerfeld condition]]
[[!redirects Bohr--Sommerfeld condition]]

[[!redirects Bohr–Sommerfeld condition]]
[[!redirects Bohr–Sommerfeld conditions]]
