
<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


## Idea

The [[quantum mechanics]] of a point particle in the _Schr&ouml;dinger picture_ is encoded in a [[Hilbert space]] [[bundle]] $\mathcal{H} \to \mathbb{R}$ [[connection on a bundle|with connection]] $\nabla$ over the real line -- the _worldline_ -- of the particle.

For $t \in \mathbb{R}$ the fiber $\mathcal{H}_t$ is the **space of quantum states** of the system, at given parameter time $t$. Since this bundle is necessarily trivial, we imagine fixing a trivialization $\mathcal{H} \simeq \mathcal{H}_0 \times \mathbb{R}$. Then the flat connection on the bundle is canonically a [[differential form|1-form]] on $\mathbb{R}$ with values in linear [[operator]]s on $\mathbf{H}$.

$$
  A = H \;d t \in \Omega^1(\mathbb{R}, End(\mathcal{H}))
  \,.
$$

The component $H \in End(\mathcal{H})$ of this canonical 1-form is the **Hamilton operator** of the system.

Its [[parallel transport]] is the **time evolution** of quantum states.
