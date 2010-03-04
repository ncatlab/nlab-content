<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

_under construction_

#Content
{:toc}

#Idea

In [[perturbation theory]], the Dyson series is a perturbative expansion of a [[unitary]] time evolution operator, $U(t,t_{0})$, primarily employed in quantum field theory.  While it is asymptotically divergent, the second-order deviation from experimental data is on the order of $10^{-10}$ paradoxically making it the most empirically accurate prediction in all of physics.  It is a starting point for the use of [[Feynman diagrams]].

#The Dyson series

The Dyson series is given as

$U(t,t_{0})=\sum_{n=0}^{\infty} U_{n}(t,t_{0}) = \mathcal{T}e^{-i\int_{t_{0}}^{t}d\tau V(\tau)}$

where $\mathcal{T}$ is a time-ordering operator and $V$ is the interaction portion of the Hamiltonian.

#Use as an operator

Applying $U(t,t_{0})$ to some initial [[quantum state]] $|\psi(t_{0})\rangle$, we have

$|\psi(t)\rangle = U(t,t_{0})|\psi(t_{0})\rangle = \sum_{n=0}^{\inty}\frac{(-i)^{n}}{n!}\left(\prod_{k=1}^{n}\int_{t_{0}}^{t}dt_{k}\right)\mathcal{T}\left\{\prod_{k=1}^{n}e^{iH_{0}t_{k}}Ve^{-iH_{0}t_{k}}\right\}|\psi(t_{0})\rangle$.

[[!redirects Dyson series]]