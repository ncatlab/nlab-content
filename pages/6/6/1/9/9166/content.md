
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Symplectic geometry
+-- {: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

For $V$ a [[symplectic vector space]], its __Lagrangian Grassmannian__ $LGrass(V)$ is the space of its [[Lagrangian subspace|Lagrangian]] (maximal [[isotropic subspace|isotropic]]) subspaces.


## Properties

### As a coset space

The [[symplectic group]] of $V$ naturally acts on $LGrass(V)$.

The unitary group $U_J(V)$ associated to any fixed compatible [[complex structure]] $J$ on $V$ [[transitive action|acts transitively]] on $LGrass(V)$.  In fact, $LGrass(V)$ is [[diffeomorphism|diffeomorphic]] to the [[coset space]] $U(n)/O(n)$ of the [[unitary group]] by the [[orthogonal group]], where $n$ is the complex [[dimension]] of $(V,J)$ (so the real dimension of $V$ is $2n$).

### Cohomology and Maslov index

The first [[ordinary cohomology]] of the stable Lagrangian Grassmannian 

$$ 
LGrass = \lim_{n \to \infty} LGrass(\mathbb{C}^n)
$$

with [[integer]] [[coefficients]] is isomorphic to the [[integers]]

$$
  H^1(LGrass, \mathbb{Z}) 
  \cong
  \mathbb{Z}
  \,.
$$

[[generalized the|The]] generator of this [[cohomology group]] is called the _[[Maslov index|universal Maslov index]]_

$$
  u \in H^1(LGrass, \mathbb{Z})
  \,.
$$

Given a [[Lagrangian submanifold]] $Y \hookrightarrow X$ of a [[symplectic manifold]] $(X,\omega)$, its [[tangent bundle]] is [[classifying space|classified]] by a function

$$
  i \;\colon\; Y \to LGrass
  \,.
$$

The [[Maslov index]] of $Y$ is the universal Maslov index pulled back along this map

$$
  i^\ast u \in H^1(Y,\mathbb{Z})
  \,.
$$

Unstably, a generator of 

$$ 
H^1(\LGrass(\mathbb{C}^n),\mathbb{Z}) \cong [U(n)/O(n), U(1)] 
$$

is given by the map

$$
\mathrm{det}^2 \colon U(n) \to U(1)
$$

This map passes to the quotient $U(n)/O(n)$ because the determinant of an element of $O(n)$ can only be $\pm 1$. 

  
## Related concepts

* [[Grassmannian]]

  * [[isotropic Grassmannian]]

  * **Lagrangian Grassmannian**

* [[Maslov index]]


## References

* Sean Bates, [[Alan Weinstein]], _Lectures on the geometry of quantization_, [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)

* [[Andrew Ranicki]], _The Maslov Index_ ([pdf](http://www.maths.ed.ac.uk/~aar/maslovnotes.pdf))

* Esteban Andruchow, Gabriel Larotonda, _Lagrangian Grassmannian in Infinite Dimension_ ([arXiv:0808.2270](http://arxiv.org/abs/0808.2270))

* J. Carrillo-Pacheco, F. Jarqu&#237;n-Z&#225;rate, M. Velasco-Fuentes, F. Zald&#237;var, _An explicit description in terms of Pl&#252;cker coordinates of the Langrangian-Grassmannian_, [arxiv/1601.07501](http://arxiv.org/abs/1601.07501)
 

[[!redirects Lagrangian Grassmannian]]
[[!redirects Lagrangian Grassmannians]]
[[!redirects Lagrangian grassmannian]]
[[!redirects Lagrangian grassmannians]]
[[!redirects Lagrangean Grassmannian]]
[[!redirects Lagrangean Grassmannians]]
[[!redirects Lagrangian Grassmanian]]
[[!redirects Lagrangian Grassmanians]]
[[!redirects lagrangian grassmanian]]
[[!redirects lagrangian grassmanians]]
[[!redirects Lagrangean Grassmanian]]
[[!redirects Lagrangean Grassmanians]]