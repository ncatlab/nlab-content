<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


# Hamiltonians
* table of contents
{: toc}


## In classical mechanics

The Hamiltonian of a [[dynamical system]] is the sum of the kinetic and potential energy:
\[ H = T + V. \]

Knowing only $H$ as a function on [[phase space]] (so as a function of [[position]] $q^i$ and [[momentum]] $p_i$), we can derive other quantities as functions on phase space.  In particular, we have:
*  [[velocity]], $v^i = \partial{H}/\partial{p_i}$,
*  [[force]], $f_i = -\partial{H}/\partial{q^i}$.

Setting $v^i = \mathrm{d}q^i/\mathrm{d}t$ and $f_i = \mathrm{d}p_i/\mathrm{d}t$, we derive the [[equations of motion]] in [[Hamiltonian mechanics]].


## In quantum mechanics


The [[quantum mechanics]] of a point particle in the _Schr&#246;dinger picture_ is encoded in a [[Hilbert space]] [[bundle]] $\mathcal{H} \to \mathbb{R}$ [[connection on a bundle|with connection]] $\nabla$ over the real line -- the _worldline_ -- of the particle.

For $t \in \mathbb{R}$ the fiber $\mathcal{H}_t$ is the **space of quantum [[state]]s** of the system, at given parameter time $t$. Since this bundle is necessarily trivial, we imagine fixing a trivialization $\mathcal{H} \simeq \mathcal{H}_0 \times \mathbb{R}$. Then the flat connection on the bundle is canonically a [[differential form|1-form]] on $\mathbb{R}$ with values in linear [[operator]]s on $\mathbf{H}$.

$$
  A = H \;d t \in \Omega^1(\mathbb{R}, End(\mathcal{H}))
  \,.
$$

The component $H \in End(\mathcal{H})$ of this canonical 1-form is the **Hamilton operator** of the system.

Its [[parallel transport]] is the **time evolution** of quantum states.


[[!redirects Hamiltonian]]
[[!redirects hamiltonian]]
[[!redirects Hamiltonians]]
[[!redirects hamiltonians]]
[[!redirects Hamiltonian function]]
[[!redirects hamiltonian function]]
[[!redirects Hamiltonian functions]]
[[!redirects hamiltonian functions]]
[[!redirects Hamiltonian operator]]
[[!redirects hamiltonian operator]]
[[!redirects Hamiltonian operators]]
[[!redirects hamiltonian operators]]
[[!redirects Hamilton operator]]
[[!redirects hamilton operator]]
[[!redirects Hamilton operators]]
[[!redirects hamilton operators]]
