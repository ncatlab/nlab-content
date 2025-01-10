
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


\tableofcontents


## Idea

A mathematically precise and successful form of [[quantization]]: all compact symplectic manifolds can be quantized using Berezin quantization, as shown in [BorthwickUribe](#BorthwickUribe), and Toeplitz quantization is a special case. It is equivalent to path integral quantization. When the Kostant–Souriau operator is defined it agrees with Berezin quantization, except that Berezin quantization is defined on all observables, whereas on a generic Kahler manifold the Kostant–Souriau prequantum operators are trivial (generically, a genus $g\ge 3$ surface with the Kahler polarization has no automorphisms, so here the Kostant–Souriau maps are only defined on constants). 

## Ingredients

Let $(M^{2n},\omega)$ be a symplectic manifold. The basic ingredient of Berezin quantization is a map
$$q:M\to P(\mathcal{H})\subset B(\mathcal{H})$$
such that
$$1_{\mathcal{H}}=\int_M q\,d\mu\,,$$
with respect to some measure $d\mu$ which is approximately  equal to $\omega^n.$ Here, $P(\mathcal{H})$ is identified with rank–one projections and the integral should be interpreted weakly. There is a quantization map
$$Q_f=\int_M f\,q\,d\mu$$ 
and an expectation–value map $\langle\rangle,$
$$\langle A\rangle(x)=Tr(q(x)A)\;.$$ 
It follows that $\langle\rangle=Q^{\dagger},$ and that both $\langle\rangle$ and $Q$ preserve states. That is, if $f\ge 0$ and $\int_M f\,d\mu=1$ then $Q_f\ge 0$ and $Tr(Q_f)=1;$ if $A\ge 0$ and $Tr(A)=1$ then $\langle A\rangle\ge 0$ and $\int_M\langle A\rangle\,d\mu=1.$

##Relationship to Geometric Quantization
The prequantum line bundle of [[geometric quantization]] is the pullback of the canonical bundle over $P(\mathcal{H})$ by $q.$ If the Hamiltonian vector field of $\langle A\rangle\in C^{\infty}(P(\mathcal{H}))$ is tangent to $q$ (with respect to the Fubini–Study form) then $A$ is equal to the Kostant–Souriau operator. 
## Related entries

* [[geometrical formulation of quantum mechanics]]
* [[coherent state]]

## References

Named after [[Felix Berezin]].

* [[F. A. Berezin]], _Quantization_, Math. USSR Izv. 8 (1974) 1109--1163. MR 0395610 (52:16404) [doi](https://doi.org/10.1070/IM1974v008n05ABEH002140)

* {#BorthwickUribe} David Borthwick, Alejandro Uribe. Almost complex structures and geometric quantization (arXiv:dg-ga/9608006)

* {#Schlichenmaier2010} [[Martin Schlichenmaier]]: *Berezin-Toeplitz quantization for compact Kaehler manifolds -- A Review of Results*, Adv. Math. Phys. **2010** 927280 (2010) &lbrack;[arXiv:1003.2523](https://arxiv.org/abs/1003.2523), [doi:10.1155/2010/927280](https://doi.org/10.1155/2010/927280)&rbrack;


* V. F. Molchanov: *Berezin quantization and representation theory*, Indagationes Mathematicae (2024) &lbrack;[doi:10.1016/j.indag.2024.03.006](https://doi.org/10.1016/j.indag.2024.03.006)&rbrack;

Generalization to [[holomorphic symplectic manifolds]]:

* [[Joshua Lackman]]: *Quantization of Holomorphic Symplectic Manifolds: Analytic Continuation of Path Integrals and Coherent States* &lbrack;[arXiv:2501.05428](https://arxiv.org/abs/2501.05428)&rbrack;





