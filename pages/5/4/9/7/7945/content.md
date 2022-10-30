
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### Integrated

Given a [[symplectic manifold]] $(X,\omega)$, there is the group of [[Hamiltonian symplectomorphisms]] $HamSympl(X,\omega)$ [[action|acting]] on $X$. If $(X,\omega)$ is [[prequantum line bundle|prequantizable]] this lifts to the group of [[quantomorphisms]], both of them covering the [[diffeomorphisms]] of $X$:

[[quantomorphisms]] $\to$ [[Hamiltonian symplectomorphisms]] $\to$ [[diffeomorphisms]] .

A _Hamiltonian action_ of a [[Lie group]] $G$ on $(X,\omega)$ is an [[action]] by [[quantomorphisms]], hence a [[Lie group]] [[homomorphism]] $\hat \phi : G \to Quant(X, \omega)$

$$
  \array{
     && Quant(X, \omega)
     \\
     & {}^{\mathllap{\hat \phi}}\nearrow & \downarrow
     \\
     G &\stackrel{\phi}{\to}& HamSympl(X, \omega)
     \\
     & {}_{\mathllap{}}\searrow & \downarrow
     \\
     && Diff(X) 
  }
  \,.
$$

See ([Brylinski, prop. 2.4.10](#Brylinski)).

### Differentially

In the literature this is usually discussed at the [[infinitesimal object|infinitesimal]] level, hence for the corresponding  [[Lie algebras]]:

[[smooth functions]]+[[Poisson bracket]] $\to$ [[Hamiltonian vector fields]] $\to$ [[vector fields]]

Now an (infinitesimal) **Hamiltonian action** is a Lie algebra [[homomorphism]] $\mu : \mathfrak{g} \to (C^\infty(X), \{-,-\})$

$$
  \array{
     && (C^\infty(X),\{-,-\})
     \\
     & {}^{\mathllap{\mu}}\nearrow & \downarrow
     \\
     \mathfrak{g} &\stackrel{}{\to}& HamVect(X, \omega)
     \\
     & {}_{\mathllap{}}\searrow & \downarrow
     \\
     && Vect(X) 
  }
  \,.
$$

Dualizing, the homomorphism $\mu$ is equivalently a linear map

$$
  \tilde \mu : X \to \mathfrak{g}^*
$$

which is a homomorphism of [[Poisson manifolds]]. This is called the **[[moment map]]** of the (infinitesimal) Hamiltonian $G$-action.

**Warning** The lift from $\phi$ to $\hat \phi$ above, hence from the _existence_ of [[Hamiltonians]] to an actual _choice_ of Hamiltonians is in general indeed a choice. There may be different choices. In the literature the difference between $\hat \phi$ and $\phi$ (or of their Lie theoretic analogs) is not always clearly made.


## Properties

### Characterization

By ([Atiyah-Bott](#AtiyahBott)), the action of a Lie algebra on a symplectic manifold is Hamiltonian if and only if the symplectic form has a (basic, closed) extension to [[equivariant de Rham cohomology]].

## Related concepts

* [[moment map]]

* [[symplectic quotient]]

## References

A comprehensive account is in (see around section 2.1)

* [[Viktor Ginzburg]], [[Victor Guillemin]], Yael Karshon, _Moment maps, cobordisms and Hamiltonian group actions_ ([pdf](http://kolxo3.tiera.ru/M_Mathematics/MD_Geometry%20and%20topology/MDdg_Differential%20geometry/Ginzburg.pdf))

The perspective on Hamiltonian actions in terms of maps to extensions, infinitesimally and integrally, is made explicit in prop. 2.4.10 of

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes and geometric quantization_, Birkh&#228;user (1993)
 {#Brylinski}

The characterization in  [[equivariant cohomology]] is due to 

* [[Michael Atiyah]], [[Raoul Bott]], _The moment map and equivariant cohomology_, Topology, Vol 23, No. 1 (1984) ([pdf](https://www.math.sunysb.edu/~mmovshev/MAT570Spring2008/BOOKS/atiyahbott_moment.pdf))
 {#AtiyahBott}

Generalization to Hamiltonian actions by a [[Lie algebroid]] (instead of just a [[Lie algebra]]) is discussed in

* Rogier Bos, _Geometric quantization of Hamiltonian actions of Lie algebroids and Lie groupoids_ ([arXiv:math.SG/0604027](http://arxiv.org/abs/math.SG/0604027))
 {#Bos}

$\,$

$\,$

$\,$

$\,$

$\,$

$\,$


$\,$

$\,$

$\,$



[[!redirects hamiltonian action]]

[[!redirects Hamiltonian actions]]
[[!redirects hamiltonian actions]]

[[!redirects Hamiltonian G-action]]
[[!redirects Hamiltonian G-actions]]
