
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $p : P \to X$ a [[surjective submersion]] of [[smooth manifold]]s and $k \in \mathbb{N}$, the order $k$- **jet bundle** $J_k P \to X$ is the bundle whose [[fiber]] over a point $x \in X$ is the space of equivalence classes of [[germ]]s of [[section]]s of $p$ where two germs are considered equivalent if their first $k$ [[derivative]]s coincide.

## Definition

### Concrete

(...)

### General abstract

We discuss a general abstract definition of jet bundles.

Let 

* $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] 

* equipped with [[infinitesimal cohesion]] 

  $$
    \mathbf{H} \stackrel{\hookrightarrow}{\stackrel{\overset{\Pi_{inf}}{\leftarrow}}{\stackrel{\overset{}{\to}}{\underset{}{\leftarrow}}}} \mathbf{H}_{th}
  $$ 

* and equipped with an [[(∞,2)-sheaf]] 

  [[Mod]] $\mathbf{H}^{op} \to $ [[Stab(∞,1)Cat]] 

  of [[quasicoherent (∞,1)-sheaves]]s.


For $X \in \mathbf{H}$, write $\mathbf{\Pi}_{inf}(X)$ for the corresponding [[de Rham space]] object.

The canonical morphism

$$
  i : X \to \mathbf{\Pi}_{inf}(X)
$$

induces a [[base change geometric morphism]]

$$
  \mathbf{H}/X 
   \stackrel{\overset{Jet := i_!}{\to}}{\stackrel{\overset{i^*}{\leftarrow}}{\underset{i_*}{\to}}}
  \mathbf{H}_{\mathbf{\Pi}_{inf}(X)}
 \,.
$$

Its extra [[left adjoint]]

$$
  Jet : 
  \mathbf{H}/X 
  \to 
  \mathbf{H}/\mathbf{\Pi}_{inf}(X)
$$

we call the _jet bundle [[(∞,1)-functor]]_ . 

+-- {: .num_defn}
###### Definition

A [[quasicoherent (∞,1)-sheaf]] on $X$ is a morphism of [[(∞,2)-sheaves]]

$$
  X \to Mod
  \,.
$$

We write

$$
  QC(X) := Hom(X, Mod)
$$

for the [[stable (∞,1)-category]] of [[quasicoherent (∞,1)-sheaves]].

A _[[D-module]]_ on $X$ is a morphism of [[(∞,2)-sheaves]]

$$
  \mathbf{\Pi}_{inf}(X) \to Mod
  \,.
$$

We write 

$$
  DQC(X) := Hom(\mathbf{\Pi}_{inf}(X), Mod)
$$

for the [[stable (∞,1)-category]] of D-modules.

=--

The **Jet algebra** functor is

$$
  (Jet \dashv F)
   :
   Alg_{\mathcal{D}(X)}
    \stackrel{\overset{Jet}{\leftarrow}}{\underset{F}{\to}}
   Alg_{\mathcal{O}(X)}
  \,.
$$

(...)

## Application 

Typical [[Lagrangian]]s in [[quantum field theory]] are defined on jet bundles. Their [[variational calculus]] is governed by [[Euler-Lagrange equation]]s.

## References

Text book references include

* G. Sardanashvily, _Fibre bundles, jet manifolds and Lagrangian theory_,  Lectures for theoreticians, [arXiv:0908.1886](http://xxx.lanl.gov/abs/0908.1886)

* Shihoko Ishii, _Jet schemes, arc spaces and the Nash problem_, [arXiv:math.AG/0704.3327](http://arXiv.org/abs/0704.3327)

* D. J. Saunders, _The geometry of jet bundles_, London Mathematical Society Lecture Note Series __142__, Cambridge Univ. Press 1989.

A discussion of jet bundles with an eye towards discussion of the [[variational bicomplex]] on them is in chapter 1, section A of

* Ian Anderson, _The variational bicomplex_ ([pdf](http://www.math.usu.edu/~fg_mp/Publications/VB/vb.pdf))
{#Anderson}


[[!redirects jet bundles]]
