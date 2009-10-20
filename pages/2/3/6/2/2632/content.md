
#Contents#
* automatic table of contents goes here
{:toc}

#Point particle quantum mechanics#

 _Quantum mechanics_ is usually understood to be the part of [[quantum field theory]] that studies the quantum analog of the [[classical mechanics]] of point particles. 

One may usefully think of the quantum mechanics of a point particle propagating on a [[manifold]] $X$ as being $(0+1)$-dimensional [[quantum field theory]]:

the fields of this system are maps $\Sigma \to X$ where $\Sigma \in Riem Bord_1$ are 1-dimensional [[Riemannian manifold]] [[cobordism]]s. These are the _trajectories_ of the particle. 

After [[quantization]] this yields a 1-dimensional [[FQFT]] given by a [[functor]]

$$
  U(-) : Riem Bord_1 \to Hilb
$$

from [[cobordism]]s to [[Hilbert space]]s (or some other flavor of [[vector space]]s) that assigns

* to the point the _space of states_ $\mathcal{H}$, typically the space of $L_2$-sections (with respect to a [[Riemannian metric]] on $X$) of the background [[gauge field]] on $X$ under which the particle in question is charged 

* to the cobordism of Riemannian length $t$ the operator

  $$
    U(t) := \exp\left(\frac{t}{i \hbar } H \right)
    : \mathcal{H} \to \mathcal{H}
    \,,
  $$

  where $H$ is the [[Hamiltonian operator]], typically of the form $H = \nabla^\dagger \circ \nabla $ for $\nabla$ the [[covariant derivative]] of the given background [[gauge field]].

Such a setup describes the quantum mechanics of a particle that feels forces of backgound [[gravity]] encoded in the [[Riemannian metric]] on $X$ and forces of background gauge fields (such as the [[electromagnetic field]]) encoded in the covariant derivative $\nabla$.

#Quantum mechanics in general #

More generally, _quantum mechanics_ may be used as a term that subsumes [[quantum field theory]] and all of physics that is not [[classical mechanics]]. 

